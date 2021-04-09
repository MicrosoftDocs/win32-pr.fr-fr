---
title: IMsRdpDevice propriété DeviceDescription
description: Récupère la description de l’appareil à afficher à l’utilisateur si le nom complet n’est pas disponible.
ms.assetid: 969f96c6-5655-4cac-9e91-059114dc3815
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceDescription
- Services Bureau à distance de la propriété DeviceDescription, interface IMsRdpDevice
- Services Bureau à distance de l’interface IMsRdpDevice, propriété DeviceDescription
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceDescription
- IMsRdpDevice.get_DeviceDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e352acef945c09c6be592174dd86a46cd8689aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104614"
---
# <a name="imsrdpdevicedevicedescription-property"></a><span data-ttu-id="ec613-106">IMsRdpDevice ::D propriété eviceDescription</span><span class="sxs-lookup"><span data-stu-id="ec613-106">IMsRdpDevice::DeviceDescription property</span></span>

<span data-ttu-id="ec613-107">Récupère la description de l’appareil à afficher à l’utilisateur si le nom complet n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="ec613-107">Retrieves the device description to be displayed to the user if the display name is not available.</span></span>

<span data-ttu-id="ec613-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ec613-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec613-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec613-109">Syntax</span></span>


```C++
HRESULT get_DeviceDescription(
  [out] BSTR *pDeviceDescription
);
```



## <a name="property-value"></a><span data-ttu-id="ec613-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ec613-110">Property value</span></span>

<span data-ttu-id="ec613-111">Description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ec613-111">The device description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ec613-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ec613-112">Error codes</span></span>

<span data-ttu-id="ec613-113">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="ec613-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ec613-114">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="ec613-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec613-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec613-115">Requirements</span></span>



| <span data-ttu-id="ec613-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec613-116">Requirement</span></span> | <span data-ttu-id="ec613-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec613-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec613-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec613-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ec613-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec613-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ec613-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec613-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ec613-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec613-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ec613-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ec613-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec613-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec613-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec613-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ec613-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec613-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec613-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec613-126">IID</span><span class="sxs-lookup"><span data-stu-id="ec613-126">IID</span></span><br/>                      | <span data-ttu-id="ec613-127">IID \_ IMsRdpDevice est défini en tant que 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="ec613-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ec613-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec613-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec613-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="ec613-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





