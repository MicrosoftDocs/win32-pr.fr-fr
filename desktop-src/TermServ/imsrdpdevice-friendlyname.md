---
title: IMsRdpDevice FriendlyName, propriété
description: Récupère le nom complet de l’appareil.
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- FriendlyName, propriété Services Bureau à distance
- FriendlyName, propriété Services Bureau à distance, interface IMsRdpDevice
- Services Bureau à distance de l’interface IMsRdpDevice, propriété FriendlyName
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf7963cf49945b886d72a622b517438e24d148f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740541"
---
# <a name="imsrdpdevicefriendlyname-property"></a><span data-ttu-id="2e1b5-106">IMsRdpDevice :: FriendlyName, propriété</span><span class="sxs-lookup"><span data-stu-id="2e1b5-106">IMsRdpDevice::FriendlyName property</span></span>

<span data-ttu-id="2e1b5-107">Récupère le nom complet de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2e1b5-107">Retrieves the display name for the device.</span></span>

<span data-ttu-id="2e1b5-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2e1b5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1b5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e1b5-109">Syntax</span></span>


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a><span data-ttu-id="2e1b5-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2e1b5-110">Property value</span></span>

<span data-ttu-id="2e1b5-111">Le nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2e1b5-111">The display name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2e1b5-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2e1b5-112">Error codes</span></span>

<span data-ttu-id="2e1b5-113">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="2e1b5-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="2e1b5-114">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="2e1b5-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e1b5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e1b5-115">Requirements</span></span>



| <span data-ttu-id="2e1b5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e1b5-116">Requirement</span></span> | <span data-ttu-id="2e1b5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e1b5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e1b5-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e1b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2e1b5-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e1b5-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2e1b5-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e1b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2e1b5-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e1b5-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2e1b5-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2e1b5-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e1b5-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e1b5-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2e1b5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2e1b5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e1b5-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e1b5-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2e1b5-126">IID</span><span class="sxs-lookup"><span data-stu-id="2e1b5-126">IID</span></span><br/>                      | <span data-ttu-id="2e1b5-127">IID \_ IMsRdpDevice est défini en tant que 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="2e1b5-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2e1b5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e1b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e1b5-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="2e1b5-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





