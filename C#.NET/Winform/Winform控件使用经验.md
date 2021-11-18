1. 编译带有用户组件（component）的程序集要使用 AnyCpu，否则设计器不显示
2. 在背景上绘制文字

    ```csharp
    private void panel_top_PaintClient(object sender, PaintEventArgs e)
    {
        var drawString = "药事安全管理系统";
        var drawFont = new Font("黑体", 14);
        var drawBrush = new SolidBrush(Color.White);
        var x = 10F;
        var y = 10F;
        var drawFormat = new StringFormat();
        e.Graphics.DrawString(drawString, drawFont, drawBrush, x, y, drawFormat);
    }
    ```
3. 关系RadioButton

    a. 处于同一个容器（panel，groupbox，form）中的RadioButton自动归为一组，没有显示设置的属性；

    b. AutoCheck属性设置为false后，点击控件是没有反应的，可以在click事件中设置其选中状态；

4. 关于数据绑定

    为控件的DataSource赋值的时候，不适用DataTable的情况下建议使用BindingSource或者BindingList<T>，此时实体类如果实现INotifyPropertyChanged接口后，实体类实例的属性值被修改可以直接反映到控件界面。

5. 窗体的Location属性要在Show()方法之后设置才能生效

6. 获取屏幕Size，不包括任务栏

    ```csharp
    var screenWidth = Screen.PrimaryScreen.WorkingArea.Width;
    var screenHeight = Screen.PrimaryScreen.WorkingArea.Height;

    var screenWidthWithoutTaskBar = BarSystem.Windows.Forms.Screen.PrimaryScreen.Bounds.Width
    var screenHeightWithoutTaskBar = System.Windows.Forms.Screen.PrimaryScreen.Bounds.Height
    ```

7. 如果datarow的rowstate是added, 那么在调用datarow.delect()方法后会直接删除该行, 不是改变rowstate为delete

8. treeview控件
    + treeview属性方法
        - nodes：子节点集合
        - nodes[i]：index为i的子节点
        - count：该集合节点的数目
        - clear()：从该集合中删除所有几点
        - Add()：添加节点
        - SelectedNode：当前左键选择的节点
        - ExpandAll()：展开所有节点
        - CollapseAll()：折叠所有节点
        - GetNodeAt()：检索位于指定点的树节点
        - GetNodeCount(boolean)：检索树节点数（是否包括所有子节点）
        
    + 节点属性方法
        - nodes：所有子节点的集合
        - name：节点名
        - text：节点所显示的文本
        - parent：父节点
        - selectednode：所选的节点
        - text：节点的文本
        - remove()：删除该节点
        - expand()：展开该节点（不包括子节点的子节点）
        - collapse()：折叠该节点
    + 事件
    - mouseclick事件与click事件只在treeview的节点处及节点的左右空白处触发，下方的空白处不触发
    - mouseup和mousedown可以在空白处触发














