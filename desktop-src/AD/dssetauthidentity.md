---
title: DsSetAuthIdentity, fonction (ntdsbcli. h)
description: Définit le contexte de sécurité dans lequel les API de sauvegarde d’annuaire sont appelées.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsSetAuthIdentity
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465726"
---
# <a name="dssetauthidentity-function"></a><span data-ttu-id="a3f7b-104">DsSetAuthIdentity fonction)</span><span class="sxs-lookup"><span data-stu-id="a3f7b-104">DsSetAuthIdentity function</span></span>

<span data-ttu-id="a3f7b-105">\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a3f7b-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a3f7b-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a3f7b-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a3f7b-107">À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="a3f7b-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="a3f7b-108">La fonction **DsSetAuthIdentity** définit le contexte de sécurité sous lequel les API de sauvegarde d’annuaire sont appelées.</span><span class="sxs-lookup"><span data-stu-id="a3f7b-108">The **DsSetAuthIdentity** function sets the security context under which the directory backup APIs are called.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f7b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3f7b-109">Syntax</span></span>


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a><span data-ttu-id="a3f7b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3f7b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f7b-111">*szUserName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3f7b-111">*szUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f7b-112">Chaîne terminée par le caractère null qui spécifie le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3f7b-112">The null-terminated string that specifies the user name.</span></span>

</dd> <dt>

<span data-ttu-id="a3f7b-113">*szDomainName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3f7b-113">*szDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f7b-114">Chaîne terminée par le caractère null qui spécifie le nom du domaine auquel l’utilisateur appartient.</span><span class="sxs-lookup"><span data-stu-id="a3f7b-114">The null-terminated string that specifies the name of the domain that the user belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="a3f7b-115">*szPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3f7b-115">*szPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3f7b-116">Chaîne terminée par le caractère null qui spécifie le mot de passe de l’utilisateur dans le domaine spécifié.</span><span class="sxs-lookup"><span data-stu-id="a3f7b-116">The null-terminated string that specifies the password of the user in the specified domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f7b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3f7b-117">Return value</span></span>

<span data-ttu-id="a3f7b-118">En cas de réussite, retourne un code de réussite **HRESULT** standard ; dans le cas contraire, un code d’échec est retourné.</span><span class="sxs-lookup"><span data-stu-id="a3f7b-118">If successful, returns a standard **HRESULT** success codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f7b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a3f7b-119">Remarks</span></span>

<span data-ttu-id="a3f7b-120">Si **DsSetAuthIdentity** n’est pas appelé, le contexte de sécurité du processus actuel est supposé.</span><span class="sxs-lookup"><span data-stu-id="a3f7b-120">If **DsSetAuthIdentity** is not called, security context of the current process is assumed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f7b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3f7b-121">Requirements</span></span>



| <span data-ttu-id="a3f7b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3f7b-122">Requirement</span></span> | <span data-ttu-id="a3f7b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3f7b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f7b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3f7b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f7b-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3f7b-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3f7b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3f7b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f7b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3f7b-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3f7b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3f7b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3f7b-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f7b-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3f7b-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a3f7b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3f7b-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3f7b-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3f7b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a3f7b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3f7b-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3f7b-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="a3f7b-134">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a3f7b-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a3f7b-135">**DsSetAuthIdentityW** (Unicode) et **DsSetAuthIdentityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a3f7b-135">**DsSetAuthIdentityW** (Unicode) and **DsSetAuthIdentityA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a3f7b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3f7b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f7b-137">Sauvegarde et restauration d’un serveur Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3f7b-137">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="a3f7b-138">Fonctions de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="a3f7b-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

