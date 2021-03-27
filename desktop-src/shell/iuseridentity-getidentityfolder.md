---
description: GetIdentityFolder n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'IUserIdentity :: GetIdentityFolder, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972323"
---
# <a name="iuseridentitygetidentityfolder-method"></a><span data-ttu-id="ccf8e-104">IUserIdentity :: GetIdentityFolder, méthode</span><span class="sxs-lookup"><span data-stu-id="ccf8e-104">IUserIdentity::GetIdentityFolder method</span></span>

<span data-ttu-id="ccf8e-105">\[**GetIdentityFolder** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-105">\[**GetIdentityFolder** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ccf8e-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="ccf8e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="ccf8e-107">Obtient le dossier de fichiers associé à cette identité.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-107">Gets the file folder associated with this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf8e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccf8e-108">Syntax</span></span>


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="ccf8e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccf8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf8e-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccf8e-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf8e-111">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ccf8e-111">Type: **DWORD**</span></span>

<span data-ttu-id="ccf8e-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-112">Required.</span></span> <span data-ttu-id="ccf8e-113">Valeur qui spécifie si le dossier associé à cette identité est itinérant.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-113">A value that specifies whether the folder associated with this identity is roaming.</span></span> <span data-ttu-id="ccf8e-114">Doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-114">Must be one of the following values.</span></span>

<dt>



 <span data-ttu-id="ccf8e-115">(GIF \_ dossier d’itinérance \_ )</span><span class="sxs-lookup"><span data-stu-id="ccf8e-115">(GIF\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="ccf8e-116">Le dossier est itinérant.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-116">The folder is roaming.</span></span>

</dd> <dt>



 <span data-ttu-id="ccf8e-117">(GIF \_ \_dossier non itinérant \_ )</span><span class="sxs-lookup"><span data-stu-id="ccf8e-117">(GIF\_NON\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="ccf8e-118">Le dossier est local.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-118">The folder is local.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ccf8e-119">*pszPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccf8e-119">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf8e-120">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="ccf8e-120">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="ccf8e-121">Pointeur vers une chaîne de caractères larges qui reçoit le chemin d’accès au dossier.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-121">A pointer to a wide-character string that receives the folder path.</span></span>

</dd> <dt>

<span data-ttu-id="ccf8e-122">_ulBuffSize \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccf8e-122">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf8e-123">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="ccf8e-123">Type: **ULONG**</span></span>

<span data-ttu-id="ccf8e-124">Valeur qui spécifie la taille de *pszPath*.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-124">A value that specifies the size of *pszPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf8e-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ccf8e-125">Return value</span></span>

<span data-ttu-id="ccf8e-126">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ccf8e-126">Type: **HRESULT**</span></span>

<span data-ttu-id="ccf8e-127">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ccf8e-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ccf8e-128">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ccf8e-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf8e-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ccf8e-129">Requirements</span></span>



| <span data-ttu-id="ccf8e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccf8e-130">Requirement</span></span> | <span data-ttu-id="ccf8e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccf8e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf8e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccf8e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf8e-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccf8e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ccf8e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccf8e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf8e-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccf8e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ccf8e-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ccf8e-136">End of client support</span></span><br/>    | <span data-ttu-id="ccf8e-137">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="ccf8e-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="ccf8e-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ccf8e-138">End of server support</span></span><br/>    | <span data-ttu-id="ccf8e-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ccf8e-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="ccf8e-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccf8e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccf8e-141"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf8e-141"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccf8e-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="ccf8e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ccf8e-143"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ccf8e-143"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="ccf8e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf8e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccf8e-145"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf8e-145"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf8e-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccf8e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf8e-147">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="ccf8e-147">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="ccf8e-148">**IUserIdentity::OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="ccf8e-148">**IUserIdentity::OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




