1.ȫ�ְ�װvue-cli

2.��ʼ����Ŀ vue init webpack trnlsoft
	Project name :��Ŀ���� ���������Ҫ����ֱ�ӻس��Ϳ����ˡ�ע�⣺���ﲻ��ʹ�ô�д�������Ұ����Ƹĳ���vueclitest
	Project description:��Ŀ������Ĭ��ΪA Vue.js project,ֱ�ӻس������ñ�д��
	Author�����ߣ������������git�����ߣ������ȡ��
	Install  vue-router? �Ƿ�װvue��·�ɲ��������������Ҫ��װ������ѡ��Y
	Use ESLint to lint your code? �Ƿ���ESLint��������Ĵ������ͷ���������ﲻ��Ҫ����n��������Ǵ����Ŷӿ���������ǽ������á�
	setup unit tests with  Karma + Mocha? �Ƿ���Ҫ��װ��Ԫ���Թ���Karma+Mocha���������ﲻ��Ҫ����������n��
	Setup e2e tests with Nightwatch?�Ƿ�װe2e�������û���Ϊģ����ԣ��������ﲻ��Ҫ����������n��

3.cd trnlsoft  �������ǵ�vue��ĿĿ¼��

4.npm install  ��װ���ǵ���Ŀ��������Ҳ���ǰ�װpackage.json��İ�����������ٲ��ã���Ҳ����ʹ��cnpm����װ��

5.npm run dev ����ģʽ���������ǵĳ���

6.cnpm install element-ui --save װ��element-ui
	��main.js������
	import ElementUI from 'element-ui'
	import 'element-ui/lib/theme-chalk/index.css'
	Vue.use(ElementUI)

7.cnpm install less less-loader --save (Ŀǰ��û���������������� �б������Ҫ���)
�޸�webpack.base.conf.js
{  
	test: /\.css$/,  
	loader: 'style-loader!css-loader',
	include: [  
	  /src/,//��ʾ��srcĿ¼�µ�css��Ҫ����  
	  '/node_modules/element-ui/lib/'   //���Ӵ���  
	] 
}, 

8.npm install --save particles.js ��װ��� particles



��ĿĿ¼
|-- build                            // ��Ŀ����(webpack)��ش���
|   |-- build.js                     // ����������������
|   |-- check-version.js             // ���node��npm�Ȱ汾
|   |-- dev-client.js                // ���������
|   |-- dev-server.js                // �������ط�����
|   |-- utils.js                     // �����������
|   |-- webpack.base.conf.js         // webpack��������
|   |-- webpack.dev.conf.js          // webpack������������
|   |-- webpack.prod.conf.js         // webpack������������

|-- config                           // ��Ŀ������������
|   |-- dev.env.js                   // ������������
|   |-- index.js                     // ��ĿһЩ���ñ���
|   |-- prod.env.js                  // ������������
|   |-- test.env.js                  // ���Ի�������

|-- src                              // Դ��Ŀ¼
|   |-- components                   // vue�������
|   |-- store                        // vuex��״̬����
|   |-- App.vue                      // ҳ������ļ�
|   |-- main.js                      // ��������ļ������ظ��ֹ������

|-- static                           // ��̬�ļ�������һЩͼƬ��json���ݵ�
|   |-- data                         // Ⱥ�ķ����õ��������������ݿ��ӻ�

|-- .babelrc                         // ES6�﷨��������
|-- .editorconfig                    // ��������ʽ
|-- .gitignore                       // git�ϴ���Ҫ���Ե��ļ���ʽ
|-- README.md                        // ��Ŀ˵��
|-- favicon.ico 
|-- index.html                       // ���ҳ��
|-- package.json                     // ��Ŀ������Ϣ



dependencies�ֶ�ָ��Ŀ����ʱ��������ģ�飻
devDependencies�ֶ�ָ������Ŀ����ʱ��������ģ�飻