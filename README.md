# makevideo

tic
video = VideoWriter('yourvideo.avi','Uncompressed AVI'); %create the video object
open(video); %open the file for writing
% figs=(dir('E:/Matlab_program_experiment/Experiment_data/Pic_files/*.jpg'));
figs=(dir('D:/IBM/Make video/hw_area_video/*.png'));

% figs=(dir('D:\IBM\2021.06.11 SDSS\my_pic\*.jpg'));
numbers = numel(figs);
for ii=1:numbers %where N is the number of image
%     I = imread('ani_%d_level_%s.png', ii); %read the next image
%     I=imread(['E:/Matlab_program_experiment/Experiment_data/1000 itr_/' num2str(ii*100,'%d') '.jpg']);
I=imread(['D:/IBM/Make video/hw_area_video/' num2str(ii,'%d') '.png']);
%     I = imread([num2str(ii),'.jpg']);
    writeVideo(video,I); %write the image to file
end
close(video); %close the file
toc

