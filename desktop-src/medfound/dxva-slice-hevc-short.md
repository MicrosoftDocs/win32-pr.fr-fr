---
description: Spécifie les données de contrôle de la tranche.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: Structure DXVA_Slice_HEVC_Short (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033803"
---
# <a name="dxva_slice_hevc_short-structure"></a><span data-ttu-id="9f869-103">\_ \_ \_ Structure abrégée HEVC de la tranche DXVA</span><span class="sxs-lookup"><span data-stu-id="9f869-103">DXVA\_Slice\_HEVC\_Short structure</span></span>

<span data-ttu-id="9f869-104">Spécifie les données de contrôle de la tranche.</span><span class="sxs-lookup"><span data-stu-id="9f869-104">Specifies slice control data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f869-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f869-105">Syntax</span></span>


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a><span data-ttu-id="9f869-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9f869-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f869-107">**BSNALunitDataLocation**</span><span class="sxs-lookup"><span data-stu-id="9f869-107">**BSNALunitDataLocation**</span></span>
</dt> <dd>

<span data-ttu-id="9f869-108">Spécifie l’emplacement de l’unité NAL.</span><span class="sxs-lookup"><span data-stu-id="9f869-108">Specifies the location of the NAL unit.</span></span>

</dd> <dt>

<span data-ttu-id="9f869-109">**SliceBytesInBuffer**</span><span class="sxs-lookup"><span data-stu-id="9f869-109">**SliceBytesInBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="9f869-110">Nombre d’octets dans la mémoire tampon de données de flux binaire associés à cette structure de données de contrôle de la tranche.</span><span class="sxs-lookup"><span data-stu-id="9f869-110">The number of bytes in the bitstream data buffer that are associated with this slice control data structure.</span></span>

</dd> <dt>

<span data-ttu-id="9f869-111">**wBadSliceChopping**</span><span class="sxs-lookup"><span data-stu-id="9f869-111">**wBadSliceChopping**</span></span>
</dt> <dd>

<span data-ttu-id="9f869-112">Si l’analyse de flux binaire hors hôte est utilisée, cette valeur indique le découpage de la tranche incorrecte et contient l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9f869-112">If off-host bitstream parsing is used, this value indicates the bad slice chopping and contains one of the following values:</span></span>



| <span data-ttu-id="9f869-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f869-113">Requirement</span></span> | <span data-ttu-id="9f869-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f869-114">Value</span></span> |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f869-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f869-115">Value</span></span> | <span data-ttu-id="9f869-116">Description</span><span class="sxs-lookup"><span data-stu-id="9f869-116">Description</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="9f869-117">0</span><span class="sxs-lookup"><span data-stu-id="9f869-117">0</span></span>     | <span data-ttu-id="9f869-118">Tous les bits de la tranche sont situés dans le tampon de données de flux binaire correspondant.</span><span class="sxs-lookup"><span data-stu-id="9f869-118">All bits for the slice are located within the corresponding bitstream data buffer.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="9f869-119">1</span><span class="sxs-lookup"><span data-stu-id="9f869-119">1</span></span>     | <span data-ttu-id="9f869-120">La mémoire tampon de données de flux binaire contient le début de la tranche, mais pas la tranche entière, car la mémoire tampon est pleine.</span><span class="sxs-lookup"><span data-stu-id="9f869-120">The bitstream data buffer contains the start of the slice, but not the entire slice, because the buffer is full.</span></span>                                                                                                                                        |
| <span data-ttu-id="9f869-121">2</span><span class="sxs-lookup"><span data-stu-id="9f869-121">2</span></span>     | <span data-ttu-id="9f869-122">La mémoire tampon de données de flux binaire contient la fin de la tranche.</span><span class="sxs-lookup"><span data-stu-id="9f869-122">The bitstream data buffer contains the end of the slice.</span></span> <span data-ttu-id="9f869-123">Elle ne contient pas le début de la tranche, car le début de la tranche a été localisé dans la mémoire tampon de données de flux binaire précédente.</span><span class="sxs-lookup"><span data-stu-id="9f869-123">It does not contain the start of the slice, because the start of the slice was located in the previous bitstream data buffer.</span></span>                                                                  |
| <span data-ttu-id="9f869-124">3</span><span class="sxs-lookup"><span data-stu-id="9f869-124">3</span></span>     | <span data-ttu-id="9f869-125">La mémoire tampon de données de flux binaire ne contient pas le début de la tranche, car le début de la tranche a été localisé dans la mémoire tampon de données de flux binaire précédente et ne contient pas la fin de la tranche, car la mémoire tampon de données de flux de données actuelle est également pleine.</span><span class="sxs-lookup"><span data-stu-id="9f869-125">The bitstream data buffer does not contain the start of the slice because the start of the slice was located in the previous bitstream data buffer and it does not contain the end of the slice becuase the current bitstream data buffer is also full.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f869-126">Notes</span><span class="sxs-lookup"><span data-stu-id="9f869-126">Remarks</span></span>

<span data-ttu-id="9f869-127">**DXVA \_ Slice \_ HEVC \_ short** contient des données de contrôle de tranche qui sont transmises à l’accélérateur matériel à partir du décodeur logiciel hôte.</span><span class="sxs-lookup"><span data-stu-id="9f869-127">**DXVA\_Slice\_HEVC\_Short** contains slice control data which is passed to the hardware accelerator from the host software decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f869-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f869-128">Requirements</span></span>



| <span data-ttu-id="9f869-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f869-129">Requirement</span></span> | <span data-ttu-id="9f869-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f869-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9f869-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f869-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9f869-132">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f869-132">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9f869-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f869-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9f869-134">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f869-134">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9f869-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f869-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f869-136"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f869-136"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f869-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f869-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f869-138">Structures de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9f869-138">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




