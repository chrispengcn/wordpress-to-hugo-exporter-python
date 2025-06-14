### WordPress to Hugo Export Tool (Python Version)  

This script automatically connects to a WordPress database, reads content, and exports it as Hugo-compatible Markdown files.  


### Script Functionality Overview  

This Python script replicates the functionality of the original WordPress plugin but runs as a command-line tool. Key features include:  

1. **Automatic Configuration Reading**: The script reads the `wp-config.php` file from the WordPress root directory to extract database connection information.  
2. **Flexible Export Options**: Supports exporting posts, pages, products, or all content types.  
3. **Intelligent File Organization**: Saves files to a directory structure based on content type.  
4. **Complete Metadata Export**: Includes titles, dates, categories, tags, featured images, and other metadata.  
5. **Product Support**: Exports additional metadata for WooCommerce products.  


### Usage Instructions  

1. Ensure the required Python libraries are installed:  
   ```bash
   pip install pymysql
   ```  

2. Run the script with the WordPress root directory and content type specified:  
   ```bash
   python3 wp_to_hugo_exporter.py --wp-root /wwwroot/youdomain.com/html --type any
   ```  

3. The script will automatically:  
   - Read WordPress configuration.  
   - Connect to the database.  
   - Export content to the `wp-content/md/content` directory.  
   - Display export progress and result statistics.  


### Exported Result Structure  

Markdown files are organized in the following structure:  

```
wp-content/
  └── md/
      └── content/
          ├── posts/
          │   ├── 2023-01-01-post-title.md
          │   └── 2023-01-02-another-post.md
          ├── pages/
          │   ├── 2023-01-03-page-title.md
          │   └── ...
          └── products/
              ├── 2023-01-04-product-title.md
              └── ...
```  

Each Markdown file includes complete YAML front matter and content compatible with Hugo.





### WordPress到Hugo导出工具（Python版）

这个脚本会自动连接到WordPress数据库，读取内容并导出为Hugo兼容的Markdown文件。





### 脚本功能说明

这个Python脚本实现了与原WordPress插件相同的功能，但以命令行工具的形式运行。主要特点包括：

1. **自动配置读取**：脚本会自动从WordPress根目录读取wp-config.php文件，提取数据库连接信息
2. **灵活的导出选项**：支持导出文章(post)、页面(page)、产品(product)或全部内容
3. **智能文件组织**：根据内容类型将文件保存到对应的目录结构中
4. **完整的元数据导出**：包括标题、日期、分类、标签、特色图片等信息
5. **产品支持**：针对WooCommerce产品导出额外的元数据

### 使用方法

1. 确保安装了必要的Python库：
   ```
   pip install pymysql
   ```

2. 运行脚本，指定WordPress根目录和要导出的内容类型：
   ```
   python3 wp_to_hugo_exporter.py --wp-root /wwwroot/youdomain.com/html --type any
   ```

3. 脚本会自动：
   - 读取WordPress配置
   - 连接数据库
   - 导出内容到wp-content/md/content目录
   - 显示导出进度和结果统计

### 导出结果结构

导出的Markdown文件将按照以下结构组织：

```
wp-content/
  └── md/
      └── content/
          ├── posts/
          │   ├── 2023-01-01-post-title.md
          │   └── 2023-01-02-another-post.md
          ├── pages/
          │   ├── 2023-01-03-page-title.md
          │   └── ...
          └── products/
              ├── 2023-01-04-product-title.md
              └── ...
```

每个Markdown文件都包含完整的YAML front matter和内容，与Hugo兼容。


