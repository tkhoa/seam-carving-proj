## MY REPOSITORY
* https://github.com/tkhoa/seam-carving-proj

## THƯ VIỆN ĐÃ SỬ DỤNGDỤNG
* OpenCV
* scipy
* numba
* numpy
* copy
* argparse

## HƯỚNG DẪN SỬ DỤNG
```
python seam_carving.py (-resize | -remove) -im <IM_PATH> -out <OUTPUT_IM_NAME> 
                       [-mask <MASK_PATH>] [-rmask <REMOVAL_MASK_CHECKED_KEY>] [-dy <DY>] [-dx <DX>] 
                       [-vis] [-hremove] [-backward_energy]
```

Chọn chế độ: -resize hoặc -remove
Các tùy chọn khác:
* `-im`: Dường dẫn đến ảnh cần xử lý.
* `-out`: Đường dẫn đến tên ảnh đã xử lý. Nếu ảnh đã tồn tại sẽ tiến hành ghi đè.
* `-mask`: Đường dẫn đến 1 "mask" có kích thước bằng với kích thước của ảnh, dùng để "bảo vệ" (hạn chế tối đa các ảnh hưởng trên pixel của vùng này). Ảnh này là ảnh trắng đen, các pixel trong vùng mask màu trắng sẽ được bảo vệ.
* `-vis`: Hiển thị quá trình cắt đường seam.
* `-backward_energy`: Tính năng lượng của ảnh dựa trên Backward_energy, nếu người dùng không nhập lện này thì năng lượng của ảnh sẽ được tính theo Forward_ennergy (default).

Chế độ resize:
* `-dy`: số lượng đường seam (theo chiều ngang) thêm vào ảnh nếu dy dương| cắt đường seam nếu dy âm. 
* `-dx`: số lượng đường seam (theo chiều dọc) thêm vào ảnh nếu dy dương| cắt đường seam nếu dy âm.

Chế độ remove:
* `-rmask`: "True" or anykey. Tùy chọn này sẽ show hình ảnh trong đường dẫn đã nhập ở "-im". Dùng chuột chọn vật thể cần xóa sau có nhấn phím "s" trên bàn phím để lưu vùng chọn thành 1 mask (ảnh trắng đen). 
Tắt cửa sổ hiển thị mask rồi nhấn ESC để chế độ REMOVE bắt đầu họat động.
Các pixel trên ảnh tương ứng với vùng trắng của mask sẽ bị xóa.
* `-hremove`: Loại bỏ vật thể theo chiều ngang (cắt đường seam theo chiều ngang) trong một vài trường hợp cắt theo chiều dọc ảnh sẽ xấu, răng cưa hay biến dạng nhiều...

## Kết quả
* https://github.com/tkhoa/seam-carving-proj/blob/main/Result_imgs/DaLat_forward_y40_x50.png
* https://github.com/tkhoa/seam-carving-proj/blob/main/Result_imgs/DaLat_backward_y40_x50.png
* https://github.com/tkhoa/seam-carving-proj/blob/main/Result_imgs/DaLat_forward_y50_x150.png
* https://github.com/tkhoa/seam-carving-proj/blob/main/Result_imgs/bench_forward_y50_x100.png
* https://github.com/tkhoa/seam-carving-proj/blob/main/Result_imgs/bench_forward_y40_x50.png
* https://github.com/tkhoa/seam-carving-proj/blob/main/Result_imgs/bench_backward_y40_x50.png
* https://github.com/tkhoa/seam-carving-proj/blob/main/Result_imgs/Yoona_forward_y10_x10.jpg
* https://github.com/tkhoa/seam-carving-proj/blob/main/Result_imgs/gotcast_remove.jpg

## Nguồn tham khảo
* https://github.com/axu2/improved-seam-carving
* https://karthikkaranth.me/blog/implementing-seam-carving-with-python/
* https://blog.csdn.net/imwaters/article/details/80808491?utm_medium=distribute.pc_relevant_download.none-task-blog-baidujs-1.nonecase&depth_1-utm_source=distribute.pc_relevant_download.none-task-blog-baidujs-1.nonecase