# ���Y�x���[�p�C

## ���o�C���z�b�g�X�|�b�g
���O: mobilehot
�p�X���[�h: mobilehot
�o���h: 2.4GHz

## ���Y�p�C���O�C��
Username: pi
Password: pi

## config.txt�ɒǋL��������
dtoverlay=disable-bt //primaty UART��mini UART����UART0�ɕύX
�Q�lurl  https://www.ingenious.jp/articles/howto/raspberry-pi-howto/gpio-uart/#toc8

## ���P�H���ׂ��_
�g�����Y�x���[�p�C�ɂ���āAprimary UART���قȂ�B���̂��ߍŏI�I�Ɏg�����Y�p�C�ɐݒ�����킹�āA�ݒ��ۑ�����
臒l�̒����i�ϐ���Threshold�j
inRange()�֐��ł́A�F�����͈͂̒���
imshow()���̃R�����g�A�E�g
�f�[�^���L�^����t�@�C���̏󋵂��m�F����i�����������܂�Ă��Ȃ� or ���݂��Ȃ��j

## ���邱��
/etc/systemd/system/�f�B���N�g���ɁARedVideo.service�Ƃ������O�̐V�����T�[�r�X�t�@�C�����쐬����
�T�[�r�X��L��������
$ sudo systemctl enable sample.service
�v���O�����̓���󋵂̊�
$ sudo systemctl status sample.service
�T�[�r�X���N�����Ă�����"active (running)"�ƕ\�������

