# Lab10-Indexation.py
import numpy as np

A = np.array([10, 20, 30, 40, 50])
M = np.array([[ 1,  2,  3,  4],
              [ 5,  6,  7,  8],
              [ 9, 10, 11, 12]])

element_3 = A[2]
element_fin = A[-1]

valeur_12 = M[1, 2]
valeur_dernier = M[-1, -1]

segment = A[1:4]

sous_bloc = M[0:2, 1:]
ligne_2 = M[1, :]
colonne_3 = M[:, 2]

bloc_central = M[0:3, 1:3]
colonnes_alternees = M[:, ::2]

vue = M[0:2, 1:3]
vue[0, 0] = 999

M = np.array([[ 1,  2,  3,  4],
              [ 5,  6,  7,  8],
              [ 9, 10, 11, 12]])

sous_copie = M[0:2, 1:3].copy()
sous_copie[0, 0] = 999

M[:, -1] *= 10

M = np.array([[ 1,  2,  3,  4], [ 5,  6,  7,  8], [ 9, 10, 11, 12]])
bloc_vue = M[1:, :2]
bloc_vue[:] = -1

M = np.array([[ 1,  2,  3,  4], [ 5,  6,  7,  8], [ 9, 10, 11, 12]])
bloc_copy = M[1:, :2].copy()
bloc_copy[:] = -1

A_original = A.copy()
A[1:-1] = 0
A = A_original
