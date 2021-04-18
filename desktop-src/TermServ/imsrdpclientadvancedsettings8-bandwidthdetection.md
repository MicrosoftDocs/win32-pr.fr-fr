---
title: IMsRdpClientAdvancedSettings8 propriété BandwidthDetection
description: Spécifie si les modifications de bande passante sont détectées automatiquement.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BandwidthDetection
- Services Bureau à distance de la propriété BandwidthDetection, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété BandwidthDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f915aeff1159e675026cfc13906e69c96208f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512148"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a><span data-ttu-id="65bbe-106">IMsRdpClientAdvancedSettings8 :: BandwidthDetection, propriété</span><span class="sxs-lookup"><span data-stu-id="65bbe-106">IMsRdpClientAdvancedSettings8::BandwidthDetection property</span></span>

<span data-ttu-id="65bbe-107">Spécifie si les modifications de bande passante sont détectées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="65bbe-107">Specifies if bandwidth changes are automatically detected.</span></span>

<span data-ttu-id="65bbe-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="65bbe-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65bbe-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65bbe-109">Syntax</span></span>


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a><span data-ttu-id="65bbe-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="65bbe-110">Property value</span></span>

<span data-ttu-id="65bbe-111">**Variante \_ TRUE** si les modifications de bande passante sont détectées automatiquement ou la **\_ valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="65bbe-111">**VARIANT\_TRUE** if bandwidth changes are automatically detected or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="65bbe-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65bbe-112">Requirements</span></span>



| <span data-ttu-id="65bbe-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65bbe-113">Requirement</span></span> | <span data-ttu-id="65bbe-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="65bbe-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65bbe-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65bbe-115">Minimum supported client</span></span><br/> | <span data-ttu-id="65bbe-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="65bbe-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="65bbe-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65bbe-117">Minimum supported server</span></span><br/> | <span data-ttu-id="65bbe-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65bbe-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="65bbe-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="65bbe-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="65bbe-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65bbe-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="65bbe-121">DLL</span><span class="sxs-lookup"><span data-stu-id="65bbe-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65bbe-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65bbe-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65bbe-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65bbe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65bbe-124">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="65bbe-124">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





