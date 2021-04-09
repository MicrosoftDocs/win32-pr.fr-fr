---
title: IMsRdpDriveV2 propriété DriveLetterIndex
description: Contient l’index de la lettre du lecteur.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DriveLetterIndex
- Services Bureau à distance de la propriété DriveLetterIndex, interface IMsRdpDriveV2
- Services Bureau à distance de l’interface IMsRdpDriveV2, propriété DriveLetterIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942882"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a><span data-ttu-id="ca2e4-106">IMsRdpDriveV2 ::D propriété riveLetterIndex</span><span class="sxs-lookup"><span data-stu-id="ca2e4-106">IMsRdpDriveV2::DriveLetterIndex property</span></span>

<span data-ttu-id="ca2e4-107">Contient l’index de la lettre du lecteur.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-107">Contains the index of the letter for the drive.</span></span>

<span data-ttu-id="ca2e4-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2e4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca2e4-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a><span data-ttu-id="ca2e4-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ca2e4-110">Property value</span></span>

<span data-ttu-id="ca2e4-111">Index de la lettre du lecteur.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-111">The index of the letter for the drive.</span></span> <span data-ttu-id="ca2e4-112">0 = « A », 1 = « B », et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ca2e4-112">0 = "A", 1 = "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca2e4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca2e4-113">Requirements</span></span>



| <span data-ttu-id="ca2e4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca2e4-114">Requirement</span></span> | <span data-ttu-id="ca2e4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca2e4-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2e4-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca2e4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ca2e4-117">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="ca2e4-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="ca2e4-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca2e4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ca2e4-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca2e4-119">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="ca2e4-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ca2e4-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca2e4-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e4-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ca2e4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ca2e4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca2e4-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca2e4-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca2e4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca2e4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca2e4-125">**IMsRdpDriveV2**</span><span class="sxs-lookup"><span data-stu-id="ca2e4-125">**IMsRdpDriveV2**</span></span>](imsrdpdrivev2.md)
</dt> </dl>

 

 





