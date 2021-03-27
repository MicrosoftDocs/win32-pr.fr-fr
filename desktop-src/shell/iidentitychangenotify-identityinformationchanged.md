---
description: IdentityInformationChanged n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'IIdentityChangeNotify :: IdentityInformationChanged, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864902"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a><span data-ttu-id="8ebde-104">IIdentityChangeNotify :: IdentityInformationChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="8ebde-104">IIdentityChangeNotify::IdentityInformationChanged method</span></span>

<span data-ttu-id="8ebde-105">\[**IdentityInformationChanged** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="8ebde-105">\[**IdentityInformationChanged** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="8ebde-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="8ebde-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="8ebde-107">Appelée lorsque les informations relatives à l’identité d’un utilisateur ont changé ou lorsqu’une identité d’utilisateur a été ajoutée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="8ebde-107">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ebde-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ebde-108">Syntax</span></span>


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a><span data-ttu-id="8ebde-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ebde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ebde-110">*dwType*</span><span class="sxs-lookup"><span data-stu-id="8ebde-110">*dwType*</span></span> 
</dt> <dd>

<span data-ttu-id="8ebde-111">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8ebde-111">Type: **DWORD**</span></span>

<span data-ttu-id="8ebde-112">Valeur qui spécifie le type d’informations modifiées ou l’opération effectuée sur une identité.</span><span class="sxs-lookup"><span data-stu-id="8ebde-112">A value that specifies the type of information changed, or the operation performed on an identity.</span></span> <span data-ttu-id="8ebde-113">Peut être une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8ebde-113">Can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="8ebde-114">(IIC \_ \_identité actuelle \_ modifiée)</span><span class="sxs-lookup"><span data-stu-id="8ebde-114">(IIC\_CURRENT\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="8ebde-115">L’identité actuelle a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="8ebde-115">The current identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="8ebde-116">(IIC \_ IDENTITÉ \_ modifiée)</span><span class="sxs-lookup"><span data-stu-id="8ebde-116">(IIC\_IDENTITY\_CHANGED)</span></span>


</dt> <dd>

<span data-ttu-id="8ebde-117">Une identité a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="8ebde-117">An identity has been modified.</span></span>

</dd> <dt>



 <span data-ttu-id="8ebde-118">(IIC \_ IDENTITÉ \_ supprimée)</span><span class="sxs-lookup"><span data-stu-id="8ebde-118">(IIC\_IDENTITY\_DELETED)</span></span>


</dt> <dd>

<span data-ttu-id="8ebde-119">Une identité a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="8ebde-119">An identity has been deleted.</span></span>

</dd> <dt>



 <span data-ttu-id="8ebde-120">(IIC \_ IDENTITÉ \_ ajoutée)</span><span class="sxs-lookup"><span data-stu-id="8ebde-120">(IIC\_IDENTITY\_ADDED)</span></span>


</dt> <dd>

<span data-ttu-id="8ebde-121">Une nouvelle identité a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="8ebde-121">A new identity has been added.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ebde-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ebde-122">Return value</span></span>

<span data-ttu-id="8ebde-123">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8ebde-123">Type: **HRESULT**</span></span>

<span data-ttu-id="8ebde-124">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8ebde-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ebde-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ebde-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ebde-126">Notes</span><span class="sxs-lookup"><span data-stu-id="8ebde-126">Remarks</span></span>

<span data-ttu-id="8ebde-127">Vous pouvez implémenter cette méthode pour fournir un comportement personnalisé pour votre application lorsque la liste des identités utilisateur sur le système a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="8ebde-127">You may implement this method to provide custom behavior for your application when the list of user identities on the system has been modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ebde-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8ebde-128">Requirements</span></span>



| <span data-ttu-id="8ebde-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ebde-129">Requirement</span></span> | <span data-ttu-id="8ebde-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ebde-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebde-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ebde-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8ebde-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ebde-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8ebde-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ebde-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8ebde-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ebde-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8ebde-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8ebde-135">End of client support</span></span><br/>    | <span data-ttu-id="8ebde-136">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="8ebde-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="8ebde-137">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8ebde-137">End of server support</span></span><br/>    | <span data-ttu-id="8ebde-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8ebde-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="8ebde-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ebde-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ebde-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ebde-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ebde-141">MIDL</span><span class="sxs-lookup"><span data-stu-id="8ebde-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ebde-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ebde-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="8ebde-143">DLL</span><span class="sxs-lookup"><span data-stu-id="8ebde-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ebde-144"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ebde-144"><dt>Msoe.dll</dt></span></span> </dl>    |



 

 




