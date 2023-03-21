close all
clc
clear

output_folder = "G:\Xiaomi camera\";

v = VideoReader('4.mp4');

counter = 43643;
for i = 1:100:v.NumFrames
    video = read(v, [i, i + 100]);

    for n = 1:101
        if counter == 15295
            break;
        end
        frame = video(:,:,:,n);
        frame = frame(100:1999, 1600:3499, 1)';
        imshow(frame);
        %roi = images.roi.Rectangle(gca,'Position',[80,45,80,100]);
        imwrite(frame, output_folder + int2str(counter) + ".bmp");
        disp(int2str(counter) + ".bmp");
        counter = counter + 1;        
    end
end
disp('Done!')
