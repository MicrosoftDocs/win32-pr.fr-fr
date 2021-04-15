---
description: Appelé lorsque les identités des utilisateurs sont basculées.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'IIdentityChangeNotify :: SwitchIdentities, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991521"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a><span data-ttu-id="a8f69-103">IIdentityChangeNotify :: SwitchIdentities, méthode</span><span class="sxs-lookup"><span data-stu-id="a8f69-103">IIdentityChangeNotify::SwitchIdentities method</span></span>

<span data-ttu-id="a8f69-104">\[**SwitchIdentities** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a8f69-104">\[**SwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a8f69-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="a8f69-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="a8f69-106">Appelé lorsque les identités des utilisateurs sont basculées.</span><span class="sxs-lookup"><span data-stu-id="a8f69-106">Called when user identities are switched.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f69-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8f69-107">Syntax</span></span>


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="a8f69-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8f69-108">Parameters</span></span>

<span data-ttu-id="a8f69-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a8f69-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8f69-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8f69-110">Return value</span></span>

<span data-ttu-id="a8f69-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a8f69-111">Type: **HRESULT**</span></span>

<span data-ttu-id="a8f69-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a8f69-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8f69-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8f69-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f69-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a8f69-114">Remarks</span></span>

<span data-ttu-id="a8f69-115">Vous pouvez implémenter cette méthode pour fournir un comportement personnalisé pour votre application lorsqu’un utilisateur a correctement basculé les identités.</span><span class="sxs-lookup"><span data-stu-id="a8f69-115">You may implement this method to provide custom behavior for your application when a user has successfully switched identities.</span></span> <span data-ttu-id="a8f69-116">Pour fournir un comportement personnalisé avant qu’un changement d’identité d’utilisateur se produise, implémentez la méthode [**IIdentityChangeNotify :: QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) .</span><span class="sxs-lookup"><span data-stu-id="a8f69-116">To provide custom behavior before a user identity switch occurs, implement the [**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f69-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a8f69-117">Requirements</span></span>



| <span data-ttu-id="a8f69-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8f69-118">Requirement</span></span> | <span data-ttu-id="a8f69-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8f69-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f69-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8f69-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f69-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8f69-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a8f69-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8f69-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f69-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8f69-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a8f69-124">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a8f69-124">End of client support</span></span><br/>    | <span data-ttu-id="a8f69-125">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="a8f69-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a8f69-126">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a8f69-126">End of server support</span></span><br/>    | <span data-ttu-id="a8f69-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a8f69-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a8f69-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8f69-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8f69-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f69-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8f69-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="a8f69-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8f69-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8f69-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8f69-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a8f69-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8f69-133"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f69-133"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a8f69-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8f69-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f69-135">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="a8f69-135">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="a8f69-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="a8f69-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




