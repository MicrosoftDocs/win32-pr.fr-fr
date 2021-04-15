---
description: Définit une matrice de quantification.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: Structure DXVA_Qmatrix_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524548"
---
# <a name="dxva_qmatrix_hevc-structure"></a><span data-ttu-id="7b9b1-103">DXVA \_ Qmatrix \_ HEVC, structure</span><span class="sxs-lookup"><span data-stu-id="7b9b1-103">DXVA\_Qmatrix\_HEVC structure</span></span>

<span data-ttu-id="7b9b1-104">Définit une matrice de quantification.</span><span class="sxs-lookup"><span data-stu-id="7b9b1-104">Defines a quantization matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b9b1-105">Syntax</span></span>


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a><span data-ttu-id="7b9b1-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7b9b1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b9b1-107">**ucScalingLists0 \[ 6 \] \[ 16\]**</span><span class="sxs-lookup"><span data-stu-id="7b9b1-107">**ucScalingLists0\[6\]\[16\]**</span></span>
</dt> <dd>

<span data-ttu-id="7b9b1-108">Contient les listes de mise à l’échelle pour le processus de mise à l’échelle 4x4, correspondant à ScalingList \[ 0 \] \[ MatrixID \] \[ i \] dans la spécification HEVC, où MatrixID est compris entre 0 et 5 inclus, et dont la plage est comprise entre 0 et 15 inclus.</span><span class="sxs-lookup"><span data-stu-id="7b9b1-108">Contains the scaling lists for the 4x4 scaling process, corresponding to ScalingList\[ 0 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 15, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="7b9b1-109">**ucScalingLists1 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="7b9b1-109">**ucScalingLists1\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="7b9b1-110">Contient les listes de mise à l’échelle pour le processus de mise à l’échelle de l’extension de page, correspondant à ScalingList \[ 1 \] \[ MatrixID \] \[ i \] dans la spécification HEVC, où MatrixID est compris entre 0 et 5 inclus et que la plage est comprise entre 0 et 63 inclus.</span><span class="sxs-lookup"><span data-stu-id="7b9b1-110">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 1 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="7b9b1-111">**ucScalingLists2 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="7b9b1-111">**ucScalingLists2\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="7b9b1-112">Contient les listes de mise à l’échelle pour le processus de mise à l’échelle de l’extension de page, correspondant à ScalingList \[ 2 \] \[ MatrixID \] \[ i \] dans la spécification HEVC, où MatrixID est compris entre 0 et 5 inclus, et que la plage est comprise entre 0 et 63 inclus.</span><span class="sxs-lookup"><span data-stu-id="7b9b1-112">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 2 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="7b9b1-113">**ucScalingLists3 \[ 2 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="7b9b1-113">**ucScalingLists3\[2\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="7b9b1-114">Contient les listes de mise à l’échelle pour le processus de mise à l’échelle de l’extension de page, correspondant à ScalingList \[ 3 \] \[ MatrixID \] \[ i \] dans la spécification HEVC, où MatrixID est compris entre 0 et 1 (inclus) et que je se trouve dans la plage comprise entre 0 et 63 inclus.</span><span class="sxs-lookup"><span data-stu-id="7b9b1-114">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 3 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 1, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="7b9b1-115">**ucScalingListDCCoefSizeID2**</span><span class="sxs-lookup"><span data-stu-id="7b9b1-115">**ucScalingListDCCoefSizeID2**</span></span>
</dt> <dd>

<span data-ttu-id="7b9b1-116">Contient la valeur DC de la liste de mise à l’échelle pour 16x16 size avec sizeID égal à 2 et correspondant à la mise à l’échelle \_ \_ DC \_ coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 avec sizeID égal à 2 et matrixID dans la plage comprise entre 0 et 5 inclus, dans la spécification HEVC.</span><span class="sxs-lookup"><span data-stu-id="7b9b1-116">Contains the DC value of the scaling list for 16x16 size with sizeID equal to 2 and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 2 and matrixID in the range of 0 to 5, inclusive, in HEVC specification.</span></span>

</dd> <dt>

<span data-ttu-id="7b9b1-117">**ucScalingListDCCoefSizeID3**</span><span class="sxs-lookup"><span data-stu-id="7b9b1-117">**ucScalingListDCCoefSizeID3**</span></span>
</dt> <dd>

<span data-ttu-id="7b9b1-118">Contient la valeur DC de la liste de mise à l’échelle pour une taille de 32x32 avec sizeID égal à 3, et correspondant à la mise à l’échelle \_ \_ DC \_ coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 avec sizeID égal à 3 et matrixID dans la plage comprise entre 0 et 1 inclus, dans la spécification HEVC.</span><span class="sxs-lookup"><span data-stu-id="7b9b1-118">Contains the DC value of the scaling list for 32x32 size with sizeID equal to 3, and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 3 and matrixID in the range of 0 to 1, inclusive, in HEVC specification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b9b1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b9b1-119">Requirements</span></span>



| <span data-ttu-id="7b9b1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b9b1-120">Requirement</span></span> | <span data-ttu-id="7b9b1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b9b1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7b9b1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b9b1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9b1-123">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b9b1-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7b9b1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b9b1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9b1-125">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b9b1-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7b9b1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b9b1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b9b1-127"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b9b1-127"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b9b1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b9b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9b1-129">Structures de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b9b1-129">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




