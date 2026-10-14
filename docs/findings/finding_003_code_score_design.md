CODE Score v1 queda obsoleto y será reemplazado por una versión basada en diferencias circulares.
Revision
The initial direction calculation used:

dir.diff().abs()
Revision 2
Path efficiency initially produced values greater than 1.

Root cause:

The official tracking variable dis did not match the true geometric distance reconstructed from x-y coordinates.

Correction:

Path length is now computed using Euclidean distances between consecutive tracking positions.

Current implementation:

path_length = sqrt(dx² + dy²).sum()

Status:

✅ Validated
