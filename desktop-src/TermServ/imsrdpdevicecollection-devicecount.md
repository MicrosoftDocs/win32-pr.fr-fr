---
title: IMsRdpDeviceCollection propriété DeviceCount
description: Récupère le nombre d’objets dans la collection. | IMsRdpDeviceCollection propriété DeviceCount
ms.assetid: dc44f3b8-52c4-4e5f-a633-ea7555fd01dd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceCount
- Services Bureau à distance de la propriété DeviceCount, interface IMsRdpDeviceCollection
- Services Bureau à distance de l’interface IMsRdpDeviceCollection, propriété DeviceCount
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceCount
- IMsRdpDeviceCollection.get_DeviceCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a389cd89699eb383b9f235858f0cf4a052606a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523779"
---
# <a name="imsrdpdevicecollectiondevicecount-property"></a><span data-ttu-id="ec811-107">IMsRdpDeviceCollection ::D propriété eviceCount</span><span class="sxs-lookup"><span data-stu-id="ec811-107">IMsRdpDeviceCollection::DeviceCount property</span></span>

<span data-ttu-id="ec811-108">Récupère le nombre d’objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="ec811-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="ec811-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ec811-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec811-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec811-110">Syntax</span></span>


```C++
HRESULT get_DeviceCount(
  [out] ULONG *pDeviceCount
);
```



## <a name="property-value"></a><span data-ttu-id="ec811-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ec811-111">Property value</span></span>

<span data-ttu-id="ec811-112">Nombre d’objets.</span><span class="sxs-lookup"><span data-stu-id="ec811-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ec811-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ec811-113">Error codes</span></span>

<span data-ttu-id="ec811-114">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="ec811-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ec811-115">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="ec811-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec811-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec811-116">Requirements</span></span>



| <span data-ttu-id="ec811-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec811-117">Requirement</span></span> | <span data-ttu-id="ec811-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec811-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec811-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec811-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ec811-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec811-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="ec811-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec811-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ec811-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec811-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ec811-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ec811-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec811-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec811-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ec811-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ec811-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec811-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec811-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ec811-127">IID</span><span class="sxs-lookup"><span data-stu-id="ec811-127">IID</span></span><br/>                      | <span data-ttu-id="ec811-128">IID \_ IMsRdpDeviceCollection est défini comme 56540617-D281-488C-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="ec811-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec811-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec811-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec811-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="ec811-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





