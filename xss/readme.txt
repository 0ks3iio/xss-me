��ܰ���ѣ�
�����м��������վĿ¼����Ϊwww/xss/������ֱ��ͨ��localhost���ʵ���½ҳ�棬������localhost/xss/����Ȼ�����Ҫ����/xss/Ŀ¼����֮�����еĲ���·��ǰ�棬�붼����/xss/����Ȼ���׳���


1���޸�config.php��������ݿ������ֶΣ������û��������룬���ݿ���������URL��ʼ��α��̬�����á� 

2����web��Ŀ¼����һ��xss.sql���������ݿ⡣

3���������ݿ�ִ������޸�����Ϊ�Լ��ġ� 
UPDATE oc_module SET 
code=REPLACE(code,'http://xsser.me','http://localhost');
ͬʱ�滻authtest.php�е���ַ����

4������.htaccess�ļ�д�����´��룺

<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /
RewriteRule ^([0-9a-zA-Z]{6})$ /index.php?do=code&urlKey=$1 [L] 
RewriteRule ^do/auth/(\w+?)(/domain/([\w\.]+?))?$  /index.php?do=do&auth=$1&domain=$3 [L] 
RewriteRule ^register/(.*?)$ /index.php?do=register&key=$1 [L] 
RewriteRule ^register-validate/(.*?)$ /index.php?do=register&act=validate&key=$1 [L]
</IfModule>

��ע��ע��ɹ��û����޸Ĺ���Ա���е�adminlevelΪ1ʱ �ɶ�������Ϊ��߹���Ա�ɷ���������
