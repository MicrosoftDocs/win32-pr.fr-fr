---
title: IMsRdpDeviceV2 propriété DriveLetterBitmap
description: Contient un champ de binaire qui représente une carte des lettres de lecteur contenues dans l’appareil.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DriveLetterBitmap
- Services Bureau à distance de la propriété DriveLetterBitmap, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété DriveLetterBitmap
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739996"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a><span data-ttu-id="65dae-106">IMsRdpDeviceV2 ::D propriété riveLetterBitmap</span><span class="sxs-lookup"><span data-stu-id="65dae-106">IMsRdpDeviceV2::DriveLetterBitmap property</span></span>

<span data-ttu-id="65dae-107">Contient un champ de binaire qui représente une carte des lettres de lecteur contenues dans l’appareil.</span><span class="sxs-lookup"><span data-stu-id="65dae-107">Contains a bitfield that represents a map of drive letters contained within the device.</span></span>

<span data-ttu-id="65dae-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="65dae-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="65dae-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65dae-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="65dae-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="65dae-110">Property value</span></span>

<span data-ttu-id="65dae-111">Carte des lettres de lecteur contenues dans l’appareil.</span><span class="sxs-lookup"><span data-stu-id="65dae-111">A map of drive letters contained within the device.</span></span> <span data-ttu-id="65dae-112">Chaque bit de la valeur représente une lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="65dae-112">Each bit in the value represents a drive letter.</span></span> <span data-ttu-id="65dae-113">Le bit le moins significatif représente la lettre de lecteur « A », le bit suivant représente la lettre de lecteur « B », et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="65dae-113">The least significant bit represents drive letter "A", the next bit represents drive letter "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="65dae-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65dae-114">Requirements</span></span>



| <span data-ttu-id="65dae-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65dae-115">Requirement</span></span> | <span data-ttu-id="65dae-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="65dae-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65dae-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65dae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65dae-118">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="65dae-118">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="65dae-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65dae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65dae-120">Windows Server 2008 R2 avec SP1</span><span class="sxs-lookup"><span data-stu-id="65dae-120">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="65dae-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="65dae-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="65dae-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65dae-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="65dae-123">DLL</span><span class="sxs-lookup"><span data-stu-id="65dae-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65dae-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65dae-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="65dae-125">IID</span><span class="sxs-lookup"><span data-stu-id="65dae-125">IID</span></span><br/>                      | <span data-ttu-id="65dae-126">IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="65dae-126">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="65dae-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65dae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65dae-128">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="65dae-128">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





