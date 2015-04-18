PART A
===========

Use `nm` command check the two executive files.
One is same as the sample code, and another comment two function.
Use `diff` to check differences.


	d _DYNAMIC											d _DYNAMIC
	d _GLOBAL_OFFSET_TABLE_								d _GLOBAL_OFFSET_TABLE_
	t _GLOBAL__sub_I__Z7averagePdRd		      		|	t _GLOBAL__sub_I_main
	R _IO_stdin_used									R _IO_stdin_used
	w _Jv_RegisterClasses								w _Jv_RegisterClasses
	t _Z41__static_initialization_and_destruction_0ii	t _Z41__static_initialization_and_destruction_0ii
	T _Z7averagePdRd					     		 <
	T _Z7averageif						     		 <
	U _ZNSt8ios_base4InitC1Ev@@GLIBCXX_3.4				U _ZNSt8ios_base4InitC1Ev@@GLIBCXX_3.4
	U _ZNSt8ios_base4InitD1Ev@@GLIBCXX_3.4				U _ZNSt8ios_base4InitD1Ev@@GLIBCXX_3.4
	b _ZStL8__ioinit									b _ZStL8__ioinit
	d __CTOR_END__										d __CTOR_END__
	d __CTOR_LIST__										d __CTOR_LIST__
	D __DTOR_END__										D __DTOR_END__
	d __DTOR_LIST__										d __DTOR_LIST__
	r __FRAME_END__										r __FRAME_END__
	d __JCR_END__										d __JCR_END__
	d __JCR_LIST__										d __JCR_LIST__
	A __bss_start										A __bss_start
	U __cxa_atexit@@GLIBC_2.2.5							U __cxa_atexit@@GLIBC_2.2.5
	D __data_start										D __data_start
	t __do_global_ctors_aux								t __do_global_ctors_aux
	t __do_global_dtors_aux								t __do_global_dtors_aux
	D __dso_handle										D __dso_handle
	w __gmon_start__									w __gmon_start__
	t __init_array_end									t __init_array_end
	t __init_array_start								t __init_array_start
	T __libc_csu_fini									T __libc_csu_fini
	T __libc_csu_init									T __libc_csu_init
	U __libc_start_main@@GLIBC_2.2.5					U __libc_start_main@@GLIBC_2.2.5
	A _edata											A _edata
	A _end												A _end
	T _fini												T _fini
	T _init												T _init
	T _start											T _start
	t call_gmon_start									t call_gmon_start
	b completed.6531									b completed.6531
	W data_start										W data_start
	b dtor_idx.6533										b dtor_idx.6533
	t frame_dummy										t frame_dummy
	T main												T main

We can find first file has "T _Z7averagePdRd" and 	"T _Z7averageif".
"T" is the encoded identifiers used for the functions.
It mean the symbol is in the code section.

[code section](http://en.wikipedia.org/wiki/Code_segment)
[data section](http://en.wikipedia.org/wiki/Data_segment)



PART B
============================================================

The following is result.

	1 8
	4 8
	4 8
	8 8

The first one of each line is the size of value which depend on the type of it. And the latter is a pointer.<br />
In the 64bits computer, it use 8bytes to record address.
Hence, all pointer's size is 8bytes.  e.g sizeof(pa).<br />

The sizes of four types are showed bellow.<>

	char    =>  1
	int     =>  4
	float   =>  4
	double  =>  8
