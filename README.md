* hive UDF ʹ��˵�����ݾ�γ��,��γ�ȳɶԳ��֣����ص�GeoHashֵ��'|'�ָ�
 * 
 * latitude1 longitude1 latitude2 longitude2 
 * 
 * hive ��ʹ��
 * # �����ר��Ϊĳ���ӿ��õ�
 * add jar /var/lib/hadoop-hdfs/GetGeohash.jar;
 * create temporary function getgeohash as 'com.pateo.udf.GetGeohash';
 * #���ͨ���ԱȽ�ǿ ���ܹ���������γ�ȶ� �����صĽ����'|'�ָ�
 * add jar /var/lib/hadoop-hdfs/GetGeohash.jar;
 * create temporary function getgeohashs as 'com.pateo.udf.GetMultiGeohash';
 * 
 * #�÷����������õ�udf����
 * create function  get_geo as 'com.pateo.udf.GetGeohash' USING JAR 'hdfs:///script/java/udf/GetGeohash.jar'
 * # ɾ�����õĺ���
 * DROP FUNCTION [IF EXISTS] function_name;
