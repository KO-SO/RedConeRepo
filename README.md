# �U��

## ���Y�p�C�̊�{�ݒ�

### ���o�C���z�b�g�X�|�b�g
- ���O: mobilehot
- �p�X���[�h: mobilehot
- �o���h: 2.4GHz

### ���Y�p�C���O�C��
- Username: pi
- Password: pi

### �R���p�C�����@
- ���Y�p�C�N����A���������
- $ export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib/arm-linux-gnueabihf
- videoX�̏�������������
-$ ++ -Wall videoX.cpp -o videoX.out -I /usr/local/include/opencv4 -L /usr/local/lib -lopencv_core -lopencv_objdetect -lopencv_highgui -lopencv_imgproc -lopencv_videoio -lopencv_imgcodecs -l wiringPi


### config.txt�ɒǋL��������
- dtoverlay=disable-bt //primaty UART��mini UART����UART0�ɕύX
- �Q�lurl  https://www.ingenious.jp/articles/howto/raspberry-pi-howto/gpio-uart/#toc8)

## ���̑�

### ���ӓ_
- ���݂́AvideoX.cpp���R���p�C������AvideoX.out���o���Ă���B
- sample.txt�Ƀ��O���������܂��
- imshow()�֐����R�����g�A�E�g���Ȃ��ƁA�����Ŏ��s���邱�Ƃ��ł��Ȃ��i�^�[�~�i������A$./videoX.out�Ŏ��s���镪�ɂ͖��Ȃ��j
- ���s����t�@�C����ύX����ꍇ��.service�t�@�C��������������

### ���P�H���ׂ��_
- �g�����Y�x���[�p�C�ɂ���āAprimary UART���قȂ�B���̂��ߍŏI�I�Ɏg�����Y�p�C�ɐݒ�����킹�āA�ݒ��ۑ����A�R�[�h������
- 臒l�̒����i�ϐ���Threshold�j
- inRange()�֐��ł́A�F�����͈͂̒���
- �f�[�^���L�^����t�@�C���̏󋵂��m�F����i�����������܂�Ă��Ȃ� or ���݂��Ȃ��j

### �֗��H�ȃR�}���h

#### �������s�Ɋ֘A����
- sudo nano /etc/systemd/system/sample.service  //.service�t�@�C���ɏ�������
- sudo systemctl daemon-reload
- sudo systemctl restart sample.service 
- sudo systemctl status sample.service  
- sudo systemctl stop sample.service
- sudo systemctl enable sample.servic   //.service��L��������

- vcgencmd get_camera   //�J�����̐ڑ��m�F

