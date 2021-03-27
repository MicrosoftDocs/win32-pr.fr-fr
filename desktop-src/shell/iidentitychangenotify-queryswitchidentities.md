---
description: Appelé lorsque l’utilisateur actuel a demandé que son identité d’utilisateur soit basculée, mais avant que le commutateur ne se produise.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'IIdentityChangeNotify :: QuerySwitchIdentities, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864901"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a><span data-ttu-id="9e743-103">IIdentityChangeNotify :: QuerySwitchIdentities, méthode</span><span class="sxs-lookup"><span data-stu-id="9e743-103">IIdentityChangeNotify::QuerySwitchIdentities method</span></span>

<span data-ttu-id="9e743-104">\[**QuerySwitchIdentities** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="9e743-104">\[**QuerySwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9e743-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="9e743-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="9e743-106">Appelé lorsque l’utilisateur actuel a demandé que son identité d’utilisateur soit basculée, mais avant que le commutateur ne se produise.</span><span class="sxs-lookup"><span data-stu-id="9e743-106">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e743-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e743-107">Syntax</span></span>


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="9e743-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e743-108">Parameters</span></span>

<span data-ttu-id="9e743-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9e743-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e743-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e743-110">Return value</span></span>

<span data-ttu-id="9e743-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9e743-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9e743-112">Résultat de la requête de commutateur.</span><span class="sxs-lookup"><span data-stu-id="9e743-112">Result of the switch query.</span></span> <span data-ttu-id="9e743-113">Si le commutateur doit se poursuivre, renvoyez \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e743-113">If the switch should proceed, return S\_OK.</span></span> <span data-ttu-id="9e743-114">Dans le cas contraire, retournez \_ \_ le commutateur E processus annulé \_ pour indiquer que le changement d’identité de l’utilisateur doit être abandonné.</span><span class="sxs-lookup"><span data-stu-id="9e743-114">Otherwise, return E\_PROCESS\_CANCELLED\_SWITCH to indicate that the user identity switch should be aborted.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e743-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9e743-115">Remarks</span></span>

<span data-ttu-id="9e743-116">Vous pouvez implémenter cette méthode pour fournir un comportement personnalisé pour votre application lorsqu’un utilisateur demande que les identités soient basculées.</span><span class="sxs-lookup"><span data-stu-id="9e743-116">You may implement this method to provide custom behavior for your application when a user requests that identities be switched.</span></span> <span data-ttu-id="9e743-117">Vous pouvez arrêter le commutateur d’identité en attente en retournant la valeur du \_ commutateur E process \_ Cancelled \_ .</span><span class="sxs-lookup"><span data-stu-id="9e743-117">You can stop the pending identity switch by returning the value E\_PROCESS\_CANCELLED\_SWITCH.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e743-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9e743-118">Requirements</span></span>



| <span data-ttu-id="9e743-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e743-119">Requirement</span></span> | <span data-ttu-id="9e743-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e743-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e743-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e743-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e743-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e743-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9e743-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e743-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e743-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e743-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e743-125">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9e743-125">End of client support</span></span><br/>    | <span data-ttu-id="9e743-126">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="9e743-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="9e743-127">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9e743-127">End of server support</span></span><br/>    | <span data-ttu-id="9e743-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e743-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="9e743-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e743-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e743-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e743-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e743-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="9e743-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e743-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e743-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="9e743-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9e743-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e743-134"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e743-134"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9e743-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e743-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e743-136">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="9e743-136">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="9e743-137">**IIdentityChangeNotify::SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="9e743-137">**IIdentityChangeNotify::SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




