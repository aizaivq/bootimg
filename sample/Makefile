all:unpack pack
unpack:
	@mkdir unpack
	@make -C ../unpackbootimg
	@../unpackbootimg/unpackbootimg -i boot.img -o unpack
pack:
	@mkdir pack
	@./mkbootimg --cmdline unpack/boot.img-cmdline --kernel unpack/boot.img-zImage --ramdisk unpack/boot.img-ramdisk.gz  -o pack/boot.img --base 02e00000
clean:
	@rm -rf pack
	@rm -rf unpack
	@make clean -C ../unpackbootimg
