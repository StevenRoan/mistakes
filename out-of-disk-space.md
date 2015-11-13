# Out of Disk Space Mistake

## Cause:
 * [Log is not compressed](#log)
 * [Auto update of operating system gradually occupied more and more memory](#osAutoUpdate)

#### Detail
 * <a name="log"></a> Log Size
  * Just add **logrotate** for server maintenance
 * <a name="osAutoUpdate"></a>  OS auto update
  * The root cause might be varied. Following are the root case I met so far:
   * The old Ubuntu kernel library used several hundreds of MB per version. It can use more than several GBs space. [more detail](https://github.com/StevenRoan/mistakes/issues/2)
