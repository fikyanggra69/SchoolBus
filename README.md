# SchoolBus
error in line 370 saying "reach end of file while parsing"

package visual.bususer;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;
import java.util.ArrayList;
import java.util.logging.Level;
import java.util.logging.Logger;
import javax.swing.JComboBox;
import javax.swing.JFrame;
import javax.swing.JOptionPane;
import javax.swing.JTable;
import javax.swing.table.DefaultTableModel;
import javax.swing.table.TableModel;
import sun.font.SunFontManager;
import visual.HomePage;

public class BusUser extends javax.swing.JFrame {

    public BusUser() {
        initComponents();
        this.dispose();
        this.pack();
        this.setExtendedState(MAXIMIZED_BOTH);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        showtable();
    }


    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jPanel1 = new javax.swing.JPanel();
        jLabel8 = new javax.swing.JLabel();
        jLabel9 = new javax.swing.JLabel();
        jLabel2 = new javax.swing.JLabel();
        Eedit = new javax.swing.JLabel();
        Add = new javax.swing.JLabel();
        jScrollPane2 = new javax.swing.JScrollPane();
        BusUserTable = new javax.swing.JTable();
        Delete = new javax.swing.JLabel();
        Dashboard = new javax.swing.JLabel();
        SetRoute = new javax.swing.JLabel();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);
        setName("BusUser"); // NOI18N
        setUndecorated(true);
        getContentPane().setLayout(new org.netbeans.lib.awtextra.AbsoluteLayout());

        jPanel1.setBackground(new java.awt.Color(255, 255, 255));
        jPanel1.setLayout(new org.netbeans.lib.awtextra.AbsoluteLayout());

        jLabel8.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        jLabel8.setForeground(new java.awt.Color(255, 255, 255));
        jLabel8.setText("-");
        jLabel8.addMouseListener(new java.awt.event.MouseAdapter() {
            public void mouseClicked(java.awt.event.MouseEvent evt) {
                jLabel8MouseClicked(evt);
            }
        });
        jPanel1.add(jLabel8, new org.netbeans.lib.awtextra.AbsoluteConstraints(1330, 10, 10, 10));

        jLabel9.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        jLabel9.setForeground(new java.awt.Color(255, 255, 255));
        jLabel9.setText("X");
        jLabel9.addMouseListener(new java.awt.event.MouseAdapter() {
            public void mouseClicked(java.awt.event.MouseEvent evt) {
                jLabel9MouseClicked(evt);
            }
        });
        jPanel1.add(jLabel9, new org.netbeans.lib.awtextra.AbsoluteConstraints(1350, 0, 20, -1));

        jLabel2.setIcon(new javax.swing.ImageIcon("C:\\Users\\Anna Karenina\\Documents\\NetBeansProjects\\Visual\\Images\\Dashboard\\bus user.png")); // NOI18N
        jLabel2.setText("jLabel2");
        jPanel1.add(jLabel2, new org.netbeans.lib.awtextra.AbsoluteConstraints(0, 0, 1380, 100));

        Eedit.setIcon(new javax.swing.ImageIcon("C:\\Users\\Anna Karenina\\Documents\\NetBeansProjects\\Visual\\Images\\Button\\Edit.png")); // NOI18N
        Eedit.addMouseListener(new java.awt.event.MouseAdapter() {
            public void mouseClicked(java.awt.event.MouseEvent evt) {
                EeditMouseClicked(evt);
            }
        });
        jPanel1.add(Eedit, new org.netbeans.lib.awtextra.AbsoluteConstraints(20, 220, -1, 30));

        Add.setIcon(new javax.swing.ImageIcon("C:\\Users\\Anna Karenina\\Documents\\NetBeansProjects\\Visual\\Images\\Button\\Add.png")); // NOI18N
        Add.addMouseListener(new java.awt.event.MouseAdapter() {
            public void mouseClicked(java.awt.event.MouseEvent evt) {
                AddMouseClicked(evt);
            }
        });
        jPanel1.add(Add, new org.netbeans.lib.awtextra.AbsoluteConstraints(20, 180, -1, 30));

        BusUserTable.setModel(new javax.swing.table.DefaultTableModel(
            new Object [][] {

            },
            new String [] {
                "User number", "First name", "Middle name", "Last name", "Gender", "Class", "Address", "Activity", "Emergency number"
            }
        ) {
            Class[] types = new Class [] {
                java.lang.Integer.class, java.lang.String.class, java.lang.String.class, java.lang.String.class, java.lang.String.class, java.lang.String.class, java.lang.String.class, java.lang.String.class, java.lang.Integer.class
            };
            boolean[] canEdit = new boolean [] {
                false, false, false, false, false, false, false, false, false
            };

            public Class getColumnClass(int columnIndex) {
                return types [columnIndex];
            }

            public boolean isCellEditable(int rowIndex, int columnIndex) {
                return canEdit [columnIndex];
            }
        });
        BusUserTable.setName("BusUserTable"); // NOI18N
        BusUserTable.addMouseListener(new java.awt.event.MouseAdapter() {
            public void mouseClicked(java.awt.event.MouseEvent evt) {
                BusUserTableMouseClicked(evt);
            }
            public void mouseEntered(java.awt.event.MouseEvent evt) {
                BusUserTableMouseEntered(evt);
            }
        });
        jScrollPane2.setViewportView(BusUserTable);
        if (BusUserTable.getColumnModel().getColumnCount() > 0) {
            BusUserTable.getColumnModel().getColumn(8).setResizable(false);
        }

        jPanel1.add(jScrollPane2, new org.netbeans.lib.awtextra.AbsoluteConstraints(240, 150, 1090, 537));

        Delete.setIcon(new javax.swing.ImageIcon("C:\\Users\\Anna Karenina\\Documents\\NetBeansProjects\\Visual\\Images\\Button\\Delete.png")); // NOI18N
        Delete.addMouseListener(new java.awt.event.MouseAdapter() {
            public void mouseClicked(java.awt.event.MouseEvent evt) {
                DeleteMouseClicked(evt);
            }
        });
        jPanel1.add(Delete, new org.netbeans.lib.awtextra.AbsoluteConstraints(20, 260, -1, 30));

        Dashboard.setIcon(new javax.swing.ImageIcon("C:\\Users\\Anna Karenina\\Documents\\NetBeansProjects\\Visual\\Images\\Button\\dashboard.png")); // NOI18N
        Dashboard.addMouseListener(new java.awt.event.MouseAdapter() {
            public void mouseClicked(java.awt.event.MouseEvent evt) {
                DashboardMouseClicked(evt);
            }
        });
        jPanel1.add(Dashboard, new org.netbeans.lib.awtextra.AbsoluteConstraints(20, 340, -1, 30));

        SetRoute.setIcon(new javax.swing.ImageIcon("C:\\Users\\Anna Karenina\\Documents\\NetBeansProjects\\Visual\\Images\\Button\\Set route.png")); // NOI18N
        SetRoute.addMouseListener(new java.awt.event.MouseAdapter() {
            public void mouseClicked(java.awt.event.MouseEvent evt) {
                SetRouteMouseClicked(evt);
            }
        });
        jPanel1.add(SetRoute, new org.netbeans.lib.awtextra.AbsoluteConstraints(20, 300, -1, 30));

        getContentPane().add(jPanel1, new org.netbeans.lib.awtextra.AbsoluteConstraints(0, 0, 1380, 790));

        pack();
    }// </editor-fold>                        

    private void BusUserTableMouseEntered(java.awt.event.MouseEvent evt) {                                          
        // TODO add your handling code here:
    }                                         

    private void BusUserTableMouseClicked(java.awt.event.MouseEvent evt) {                                          

    }                                         
    public Connection getConnection(){
        Connection con;
        
        try {
            con = DriverManager.getConnection("jdbc:mysql://localhost:3306/coba", "root", "");
            return con;
        } catch (SQLException ex) {
            ex.printStackTrace();
        }
        return null;
    }
    private void jLabel8MouseClicked(java.awt.event.MouseEvent evt) {                                     
        setState(JFrame.ICONIFIED);
    }                                    

    private void jLabel9MouseClicked(java.awt.event.MouseEvent evt) {                                     
        this.dispose();
    }                                    

    private void AddMouseClicked(java.awt.event.MouseEvent evt) {                                 
        addUser adduser = new addUser();
        adduser.setVisible(true);
    }                                

    private void EeditMouseClicked(java.awt.event.MouseEvent evt) {                                   
        int i = BusUserTable.getSelectedRow();
        TableModel mode = BusUserTable.getModel();
        String gender = mode.getValueAt(i, 4).toString();
        EditUser edit = new EditUser();
        edit.setVisible(true);
        
        edit.editFN.setText(mode.getValueAt(i, 1).toString());
        edit.editMD.setText(mode.getValueAt(i, 2).toString());
        edit.editLN.setText(mode.getValueAt(i,3).toString());
        edit.editClass.setText(mode.getValueAt(i,5).toString());
        edit.editAddress.setText(mode.getValueAt(i, 6).toString());
        edit.jComboBoxActivity.setSelectedItem(mode.getValueAt(i,7).toString());
        edit.editEN.setText(mode.getValueAt(i,8).toString());
        edit.UN.setText(mode.getValueAt(i, 0).toString());
        if ( gender == "Female"){
        edit.jRadioButtonFemale.setSelected(true);
    } else {
            edit.jRadioButtonMale.setSelected(true);
        }
    }                                  

    private void DeleteMouseClicked(java.awt.event.MouseEvent evt) {                                    
         int i = BusUserTable.getSelectedRow();
            TableModel mode = BusUserTable.getModel();
            Connection connection = getConnection();
            String sql = "DELETE FROM bus_user WHERE user_number="+mode.getValueAt(i, 0).toString();
            PreparedStatement ps;
        try {
            int yn = JOptionPane.showConfirmDialog(null, "Delete user ?", "Delete user", JOptionPane.YES_NO_OPTION);
            if (yn == 0){
                ps = connection.prepareStatement(sql);
            updt(sql, "deleted");
            } else {
                
            }
            
        } catch(Exception e ){
            JOptionPane.showMessageDialog(null, "Something went wrong");
        }
    }                                   

    private void SetRouteMouseClicked(java.awt.event.MouseEvent evt) {                                      
       int i = BusUserTable.getSelectedRow();
        TableModel mode = BusUserTable.getModel();
        SetRouteUser route = new SetRouteUser();
        route.setVisible(true);
        
        route.UserId.setText(mode.getValueAt(i, 0).toString());
        route.Name.setText(mode.getValueAt(i, 1).toString()+" " +mode.getValueAt(i, 2).toString()+ " "+mode.getValueAt(i,3).toString());
        route.Class.setText(mode.getValueAt(i,5).toString());
        route.Address.setText(mode.getValueAt(i,6).toString());
        route.jComboBoxActivity.setSelectedItem(mode.getValueAt(i,7).toString());
    }                                     

    private void DashboardMouseClicked(java.awt.event.MouseEvent evt) {                                       
        HomePage hp = new HomePage();
        hp.setVisible(true);
        this.dispose();
    }                                      

    public ArrayList<user> getuserList() {
          ArrayList<user> usersList = new ArrayList<user>();
              Connection connection = getConnection();
              String sql = "select * from bus_user";
              PreparedStatement ps;
              
        try {
            ps = connection.prepareStatement(sql);
            ResultSet rs = ps.executeQuery();
            user user1;
            while(rs.next()){
                user1 = new user(rs.getString("First_Name"),rs.getString("Middle_Name"),rs.getString("Last_Name"),rs.getString("Gender"),rs.getString("Class"),rs.getString("Address"),rs.getString("Activity"),rs.getString("EmergencyNum"),rs.getString("user_number"));
                usersList.add(user1);
            }
        } catch (SQLException ex) {
            ex.printStackTrace();
        }
        return usersList;
        }
        
public void showtable(){
    ArrayList<user> list = getuserList();
    DefaultTableModel model = (DefaultTableModel) BusUserTable.getModel();
    Object [] row = new Object[9];
    for(int i = 0; i < list.size(); i++)
       {
           row[0] = list.get(i).getuser_number();
           row[1] = list.get(i).getFName();
           row[2] = list.get(i).getMidName();
           row[3] = list.get(i).getLname();
           row[4] = list.get(i).getgender();
           row[5] = list.get(i).getclass1();
           row[6] = list.get(i).getAddress();
           row[7] = list.get(i).getAct();
           row[8] = list.get(i).getEmergencynum();
           
           model.addRow(row);
           
       }
    BusUserTable.setModel(model);
}
  public static void Something (Object[] dataRow)
    {
        DefaultTableModel model = (DefaultTableModel)BusUserTable.getModel();
        model.addRow(dataRow);
    }         

    public void updt (String sql, String message) {
        Connection con = getConnection();
         Statement st;
       try{
           st = con.createStatement();
           if((st.executeUpdate(sql)) == 1)
           {
               DefaultTableModel model = (DefaultTableModel) BusUserTable.getModel();
               model.setRowCount(0);
               showtable(); 
               JOptionPane.showMessageDialog(null, "Data "+message+" Succefully");
           } else{
               JOptionPane.showMessageDialog(null, "Data not "+message);
           }
       } catch(Exception ex){
           ex.printStackTrace();
       }
  
    }
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(BusUser.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(BusUser.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(BusUser.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(BusUser.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new BusUser().setVisible(true);
            }
        });
    }


    // Variables declaration - do not modify                     
    private javax.swing.JLabel Add;
    public static javax.swing.JTable BusUserTable;
    private javax.swing.JLabel Dashboard;
    private javax.swing.JLabel Delete;
    private javax.swing.JLabel Eedit;
    private javax.swing.JLabel SetRoute;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JLabel jLabel8;
    private javax.swing.JLabel jLabel9;
    private javax.swing.JPanel jPanel1;
    private javax.swing.JScrollPane jScrollPane2; // disini error nya, "reach end of file while parsing"
    // End of variables declaration                   
