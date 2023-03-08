	.text
	.attribute	4, 16
	.attribute	5, "rv32i2p0"
	.file	"matrizes.c"
	.globl	matrix_multiply                 # -- Begin function matrix_multiply
	.p2align	2
	.type	matrix_multiply,@function
matrix_multiply:                        # @matrix_multiply
	.cfi_startproc
# %bb.0:
	addi	sp, sp, -64
	.cfi_def_cfa_offset 64
	sw	ra, 60(sp)                      # 4-byte Folded Spill
	sw	s0, 56(sp)                      # 4-byte Folded Spill
	sw	s1, 52(sp)                      # 4-byte Folded Spill
	sw	s2, 48(sp)                      # 4-byte Folded Spill
	sw	s3, 44(sp)                      # 4-byte Folded Spill
	sw	s4, 40(sp)                      # 4-byte Folded Spill
	.cfi_offset ra, -4
	.cfi_offset s0, -8
	.cfi_offset s1, -12
	.cfi_offset s2, -16
	.cfi_offset s3, -20
	.cfi_offset s4, -24
	addi	s0, sp, 64
	.cfi_def_cfa s0, 0
	sw	a0, -32(s0)
	sw	a1, -40(s0)
	sw	a2, -48(s0)
	sw	zero, -52(s0)
	li	s3, 2
	j	.LBB0_2
.LBB0_1:                                #   in Loop: Header=BB0_2 Depth=1
	lw	a0, -52(s0)
	addi	a0, a0, 1
	sw	a0, -52(s0)
.LBB0_2:                                # =>This Loop Header: Depth=1
                                        #     Child Loop BB0_5 Depth 2
                                        #       Child Loop BB0_7 Depth 3
	lw	a0, -52(s0)
	blt	s3, a0, .LBB0_8
# %bb.3:                                #   in Loop: Header=BB0_2 Depth=1
	sw	zero, -56(s0)
	j	.LBB0_5
.LBB0_4:                                #   in Loop: Header=BB0_5 Depth=2
	lw	a0, -56(s0)
	addi	a0, a0, 1
	sw	a0, -56(s0)
.LBB0_5:                                #   Parent Loop BB0_2 Depth=1
                                        # =>  This Loop Header: Depth=2
                                        #       Child Loop BB0_7 Depth 3
	lw	a0, -56(s0)
	blt	s3, a0, .LBB0_1
# %bb.6:                                #   in Loop: Header=BB0_5 Depth=2
	lw	s1, -48(s0)
	lw	a0, -52(s0)
	li	a1, 12
	call	__mulsi3@plt
	lw	a1, -56(s0)
	add	a0, s1, a0
	slli	a1, a1, 2
	add	a0, a0, a1
	sw	zero, 0(a0)
	sw	zero, -60(s0)
	lw	a0, -60(s0)
	blt	s3, a0, .LBB0_4
.LBB0_7:                                #   Parent Loop BB0_2 Depth=1
                                        #     Parent Loop BB0_5 Depth=2
                                        # =>    This Inner Loop Header: Depth=3
	lw	s2, -32(s0)
	lw	a0, -52(s0)
	li	a1, 12
	call	__mulsi3@plt
	lw	a2, -60(s0)
	mv	s1, a0
	add	a0, s2, a0
	slli	a1, a2, 2
	add	a0, a0, a1
	lw	s2, 0(a0)
	lw	s4, -40(s0)
	li	a1, 12
	mv	a0, a2
	call	__mulsi3@plt
	lw	a1, -56(s0)
	add	a0, s4, a0
	slli	s4, a1, 2
	add	a0, a0, s4
	lw	a1, 0(a0)
	mv	a0, s2
	call	__mulsi3@plt
	lw	a1, -48(s0)
	add	a1, a1, s1
	add	a1, a1, s4
	lw	a2, 0(a1)
	add	a0, a2, a0
	sw	a0, 0(a1)
	lw	a0, -60(s0)
	addi	a0, a0, 1
	sw	a0, -60(s0)
	lw	a0, -60(s0)
	bge	s3, a0, .LBB0_7
	j	.LBB0_4
.LBB0_8:
	lw	ra, 60(sp)                      # 4-byte Folded Reload
	lw	s0, 56(sp)                      # 4-byte Folded Reload
	lw	s1, 52(sp)                      # 4-byte Folded Reload
	lw	s2, 48(sp)                      # 4-byte Folded Reload
	lw	s3, 44(sp)                      # 4-byte Folded Reload
	lw	s4, 40(sp)                      # 4-byte Folded Reload
	addi	sp, sp, 64
	ret
.Lfunc_end0:
	.size	matrix_multiply, .Lfunc_end0-matrix_multiply
	.cfi_endproc
                                        # -- End function
	.globl	print_matrix                    # -- Begin function print_matrix
	.p2align	2
	.type	print_matrix,@function
print_matrix:                           # @print_matrix
	.cfi_startproc
# %bb.0:
	addi	sp, sp, -48
	.cfi_def_cfa_offset 48
	sw	ra, 44(sp)                      # 4-byte Folded Spill
	sw	s0, 40(sp)                      # 4-byte Folded Spill
	sw	s1, 36(sp)                      # 4-byte Folded Spill
	sw	s2, 32(sp)                      # 4-byte Folded Spill
	sw	s3, 28(sp)                      # 4-byte Folded Spill
	sw	s4, 24(sp)                      # 4-byte Folded Spill
	.cfi_offset ra, -4
	.cfi_offset s0, -8
	.cfi_offset s1, -12
	.cfi_offset s2, -16
	.cfi_offset s3, -20
	.cfi_offset s4, -24
	addi	s0, sp, 48
	.cfi_def_cfa s0, 0
	sw	a0, -32(s0)
	sw	zero, -36(s0)
	li	s3, 2
	lui	a0, %hi(.L.str)
	addi	s1, a0, %lo(.L.str)
	lui	a0, %hi(.L.str.1)
	addi	s2, a0, %lo(.L.str.1)
	j	.LBB1_2
.LBB1_1:                                #   in Loop: Header=BB1_2 Depth=1
	mv	a0, s2
	call	printf@plt
	lw	a0, -36(s0)
	addi	a0, a0, 1
	sw	a0, -36(s0)
.LBB1_2:                                # =>This Loop Header: Depth=1
                                        #     Child Loop BB1_4 Depth 2
	lw	a0, -36(s0)
	blt	s3, a0, .LBB1_5
# %bb.3:                                #   in Loop: Header=BB1_2 Depth=1
	sw	zero, -40(s0)
	lw	a0, -40(s0)
	blt	s3, a0, .LBB1_1
.LBB1_4:                                #   Parent Loop BB1_2 Depth=1
                                        # =>  This Inner Loop Header: Depth=2
	lw	s4, -32(s0)
	lw	a0, -36(s0)
	li	a1, 12
	call	__mulsi3@plt
	lw	a1, -40(s0)
	add	a0, s4, a0
	slli	a1, a1, 2
	add	a0, a0, a1
	lw	a1, 0(a0)
	mv	a0, s1
	call	printf@plt
	lw	a0, -40(s0)
	addi	a0, a0, 1
	sw	a0, -40(s0)
	lw	a0, -40(s0)
	bge	s3, a0, .LBB1_4
	j	.LBB1_1
.LBB1_5:
	lw	ra, 44(sp)                      # 4-byte Folded Reload
	lw	s0, 40(sp)                      # 4-byte Folded Reload
	lw	s1, 36(sp)                      # 4-byte Folded Reload
	lw	s2, 32(sp)                      # 4-byte Folded Reload
	lw	s3, 28(sp)                      # 4-byte Folded Reload
	lw	s4, 24(sp)                      # 4-byte Folded Reload
	addi	sp, sp, 48
	ret
.Lfunc_end1:
	.size	print_matrix, .Lfunc_end1-print_matrix
	.cfi_endproc
                                        # -- End function
	.globl	main                            # -- Begin function main
	.p2align	2
	.type	main,@function
main:                                   # @main
	.cfi_startproc
# %bb.0:
	addi	sp, sp, -144
	.cfi_def_cfa_offset 144
	sw	ra, 140(sp)                     # 4-byte Folded Spill
	sw	s0, 136(sp)                     # 4-byte Folded Spill
	.cfi_offset ra, -4
	.cfi_offset s0, -8
	addi	s0, sp, 144
	.cfi_def_cfa s0, 0
	sw	zero, -12(s0)
	lui	a0, %hi(.L__const.main.A)
	addi	a1, a0, %lo(.L__const.main.A)
	addi	a0, s0, -48
	li	a2, 36
	call	memcpy@plt
	lui	a0, %hi(.L__const.main.B)
	addi	a1, a0, %lo(.L__const.main.B)
	addi	a0, s0, -96
	li	a2, 36
	call	memcpy@plt
	addi	a0, s0, -48
	addi	a1, s0, -96
	addi	a2, s0, -144
	call	matrix_multiply
	lui	a0, %hi(.L.str.2)
	addi	a0, a0, %lo(.L.str.2)
	call	printf@plt
	addi	a0, s0, -48
	call	print_matrix
	lui	a0, %hi(.L.str.3)
	addi	a0, a0, %lo(.L.str.3)
	call	printf@plt
	addi	a0, s0, -96
	call	print_matrix
	lui	a0, %hi(.L.str.4)
	addi	a0, a0, %lo(.L.str.4)
	call	printf@plt
	addi	a0, s0, -144
	call	print_matrix
	li	a0, 0
	lw	ra, 140(sp)                     # 4-byte Folded Reload
	lw	s0, 136(sp)                     # 4-byte Folded Reload
	addi	sp, sp, 144
	ret
.Lfunc_end2:
	.size	main, .Lfunc_end2-main
	.cfi_endproc
                                        # -- End function
	.type	.L.str,@object                  # @.str
	.section	.rodata.str1.1,"aMS",@progbits,1
.L.str:
	.asciz	"%d "
	.size	.L.str, 4

	.type	.L.str.1,@object                # @.str.1
.L.str.1:
	.asciz	"\n"
	.size	.L.str.1, 2

	.type	.L__const.main.A,@object        # @__const.main.A
	.section	.rodata,"a",@progbits
	.p2align	4
.L__const.main.A:
	.word	1                               # 0x1
	.word	2                               # 0x2
	.word	3                               # 0x3
	.word	4                               # 0x4
	.word	5                               # 0x5
	.word	6                               # 0x6
	.word	7                               # 0x7
	.word	8                               # 0x8
	.word	9                               # 0x9
	.size	.L__const.main.A, 36

	.type	.L__const.main.B,@object        # @__const.main.B
	.p2align	4
.L__const.main.B:
	.word	9                               # 0x9
	.word	8                               # 0x8
	.word	7                               # 0x7
	.word	6                               # 0x6
	.word	5                               # 0x5
	.word	4                               # 0x4
	.word	3                               # 0x3
	.word	2                               # 0x2
	.word	1                               # 0x1
	.size	.L__const.main.B, 36

	.type	.L.str.2,@object                # @.str.2
	.section	.rodata.str1.1,"aMS",@progbits,1
.L.str.2:
	.asciz	"A:\n"
	.size	.L.str.2, 4

	.type	.L.str.3,@object                # @.str.3
.L.str.3:
	.asciz	"B:\n"
	.size	.L.str.3, 4

	.type	.L.str.4,@object                # @.str.4
.L.str.4:
	.asciz	"C = A*B:\n"
	.size	.L.str.4, 10

	.ident	"Debian clang version 14.0.6"
	.section	".note.GNU-stack","",@progbits
