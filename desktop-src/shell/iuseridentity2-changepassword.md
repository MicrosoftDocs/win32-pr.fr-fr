---
description: ChangePassword n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'IUserIdentity2 :: ChangePassword, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972318"
---
# <a name="iuseridentity2changepassword-method"></a><span data-ttu-id="71e1a-104">IUserIdentity2 :: ChangePassword, méthode</span><span class="sxs-lookup"><span data-stu-id="71e1a-104">IUserIdentity2::ChangePassword method</span></span>

<span data-ttu-id="71e1a-105">\[**ChangePassword** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="71e1a-105">\[**ChangePassword** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="71e1a-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="71e1a-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="71e1a-107">Définit un nouveau mot de passe pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="71e1a-107">Sets a new password for the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e1a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71e1a-108">Syntax</span></span>


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a><span data-ttu-id="71e1a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71e1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e1a-110">*szOldPass* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71e1a-110">*szOldPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e1a-111">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="71e1a-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="71e1a-112">Chaîne de caractères larges qui contient le mot de passe actuellement associé à l’identité.</span><span class="sxs-lookup"><span data-stu-id="71e1a-112">The wide-character string that contains the password currently associated with the identity.</span></span>

</dd> <dt>

<span data-ttu-id="71e1a-113">_szNewPass \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71e1a-113">_szNewPass\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e1a-114">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="71e1a-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="71e1a-115">Chaîne de caractères larges qui contient le nouveau mot de passe à associer à l’identité.</span><span class="sxs-lookup"><span data-stu-id="71e1a-115">The wide-character string that contains the new password to be associated with the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e1a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71e1a-116">Return value</span></span>

<span data-ttu-id="71e1a-117">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="71e1a-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="71e1a-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="71e1a-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71e1a-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71e1a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="71e1a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="71e1a-120">Remarks</span></span>

<span data-ttu-id="71e1a-121">La valeur de *szOldPass* doit correspondre au mot de passe actuel de l’identité pour *szNewPass* à appliquer.</span><span class="sxs-lookup"><span data-stu-id="71e1a-121">The value of *szOldPass* must match the current password of the identity for *szNewPass* to be applied.</span></span> <span data-ttu-id="71e1a-122">Une valeur incorrecte de *szOldPass* entraînera l’échec de la valeur de retour E \_ .</span><span class="sxs-lookup"><span data-stu-id="71e1a-122">An incorrect value of *szOldPass* will result in a return value of E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="71e1a-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="71e1a-123">Requirements</span></span>



| <span data-ttu-id="71e1a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71e1a-124">Requirement</span></span> | <span data-ttu-id="71e1a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="71e1a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71e1a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71e1a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="71e1a-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71e1a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="71e1a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71e1a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="71e1a-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71e1a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="71e1a-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="71e1a-130">End of client support</span></span><br/>    | <span data-ttu-id="71e1a-131">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="71e1a-131">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="71e1a-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="71e1a-132">End of server support</span></span><br/>    | <span data-ttu-id="71e1a-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71e1a-133">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="71e1a-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="71e1a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="71e1a-135"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="71e1a-135"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="71e1a-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="71e1a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71e1a-137"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71e1a-137"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="71e1a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="71e1a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71e1a-139"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71e1a-139"><dt>Msident.dll</dt></span></span> </dl> |



 

 




