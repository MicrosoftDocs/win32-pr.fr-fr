---
title: Méthode IMsRdpDeviceCollection RescanDevices
description: Actualise la liste des objets dans la collection. | Méthode IMsRdpDeviceCollection RescanDevices
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RescanDevices
- Méthode RescanDevices Services Bureau à distance, interface IMsRdpDeviceCollection
- Services Bureau à distance de l’interface IMsRdpDeviceCollection, méthode RescanDevices
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773231ffd89a0998f6073f844a3f974920625987
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524824"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a><span data-ttu-id="29c32-107">IMsRdpDeviceCollection :: RescanDevices, méthode</span><span class="sxs-lookup"><span data-stu-id="29c32-107">IMsRdpDeviceCollection::RescanDevices method</span></span>

<span data-ttu-id="29c32-108">Actualise la liste des objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="29c32-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="29c32-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29c32-109">Syntax</span></span>


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="29c32-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29c32-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29c32-111">*vboolDynRedir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29c32-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29c32-112">État de redirection par défaut qui sera appliqué aux périphériques ou lecteurs récemment découverts.</span><span class="sxs-lookup"><span data-stu-id="29c32-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29c32-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29c32-113">Return value</span></span>

<span data-ttu-id="29c32-114">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="29c32-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="29c32-115">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="29c32-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="29c32-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29c32-116">Requirements</span></span>



| <span data-ttu-id="29c32-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29c32-117">Requirement</span></span> | <span data-ttu-id="29c32-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="29c32-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c32-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29c32-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29c32-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29c32-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="29c32-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29c32-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29c32-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29c32-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="29c32-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="29c32-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="29c32-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29c32-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="29c32-125">DLL</span><span class="sxs-lookup"><span data-stu-id="29c32-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29c32-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29c32-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="29c32-127">IID</span><span class="sxs-lookup"><span data-stu-id="29c32-127">IID</span></span><br/>                      | <span data-ttu-id="29c32-128">IID \_ IMsRdpDeviceCollection est défini comme 56540617-D281-488C-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="29c32-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29c32-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29c32-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29c32-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="29c32-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





