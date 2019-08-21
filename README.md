```
### Each time login
module purge; module load python esslurm
salloc -C gpu -N 1 -A m1759 -t 04:00:00 --gres=gpu:1 -c 10
source /usr/common/software/python/2.7-anaconda-2019.07/etc/profile.d/conda.sh
conda activate proj2col
export WORK=/project/projectdirs/lcls/proj-2col_iris
cd $WORK
export LS49_BIG_DATA=${WORK}/ls49_big_data
export OMP_NUM_THREADS=24
source build/setpaths.sh
module load gcc/7.3.0 cuda mvapich2
```
