---
title: IMsRdpDeviceV2 propriété CmClassGuid
description: Contient le GUID de la classe d’installation de Configuration Manager pour l’appareil.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CmClassGuid
- Services Bureau à distance de la propriété CmClassGuid, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété CmClassGuid
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510729"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a><span data-ttu-id="3b5b2-106">IMsRdpDeviceV2 :: CmClassGuid, propriété</span><span class="sxs-lookup"><span data-stu-id="3b5b2-106">IMsRdpDeviceV2::CmClassGuid property</span></span>

<span data-ttu-id="3b5b2-107">Contient le GUID de la classe d’installation de Configuration Manager pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3b5b2-107">Contains the configuration manager setup class GUID for the device.</span></span>

<span data-ttu-id="3b5b2-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3b5b2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b5b2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b5b2-109">Syntax</span></span>


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a><span data-ttu-id="3b5b2-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3b5b2-110">Property value</span></span>

<span data-ttu-id="3b5b2-111">GUID de la classe d’installation de Configuration Manager pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3b5b2-111">The configuration manager setup class GUID for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5b2-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b5b2-112">Requirements</span></span>



| <span data-ttu-id="3b5b2-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b5b2-113">Requirement</span></span> | <span data-ttu-id="3b5b2-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b5b2-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5b2-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b5b2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3b5b2-116">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="3b5b2-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="3b5b2-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b5b2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3b5b2-118">Windows Server 2008 R2 avec SP1</span><span class="sxs-lookup"><span data-stu-id="3b5b2-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="3b5b2-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3b5b2-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b5b2-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b5b2-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b5b2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3b5b2-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b5b2-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b5b2-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b5b2-123">IID</span><span class="sxs-lookup"><span data-stu-id="3b5b2-123">IID</span></span><br/>                      | <span data-ttu-id="3b5b2-124">IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="3b5b2-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="3b5b2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b5b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b5b2-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="3b5b2-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





