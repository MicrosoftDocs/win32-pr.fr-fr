---
description: Récupère les options associées à un partage DDE figurant dans la liste des utilisateurs du serveur de partages approuvés.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: NDdeGetTrustedShare, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516409"
---
# <a name="nddegettrustedshare-function"></a><span data-ttu-id="6cc86-103">NDdeGetTrustedShare fonction)</span><span class="sxs-lookup"><span data-stu-id="6cc86-103">NDdeGetTrustedShare function</span></span>

<span data-ttu-id="6cc86-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6cc86-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="6cc86-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="6cc86-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="6cc86-106">Récupère les options associées à un partage DDE figurant dans la liste des partages approuvés de l’utilisateur du serveur.</span><span class="sxs-lookup"><span data-stu-id="6cc86-106">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc86-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cc86-107">Syntax</span></span>


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a><span data-ttu-id="6cc86-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cc86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc86-109">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cc86-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc86-110">Nom du serveur sur lequel le DSDM réside.</span><span class="sxs-lookup"><span data-stu-id="6cc86-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="6cc86-111">*lpszShareName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cc86-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc86-112">Nom de partage dont l’État approuvé est en cours d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="6cc86-112">The share name whose trusted status is being queried.</span></span> <span data-ttu-id="6cc86-113">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="6cc86-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6cc86-114">*lpdwTrustOptions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6cc86-114">*lpdwTrustOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc86-115">Pointeur vers une variable qui reçoit les options d’approbation.</span><span class="sxs-lookup"><span data-stu-id="6cc86-115">A pointer to a variable that receives the trust options.</span></span> <span data-ttu-id="6cc86-116">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="6cc86-116">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="6cc86-117">Les options d’approbation suivantes sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="6cc86-117">The following trust options are available.</span></span>



| <span data-ttu-id="6cc86-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cc86-118">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="6cc86-119">Signification</span><span class="sxs-lookup"><span data-stu-id="6cc86-119">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="6cc86-120"><dt>**NDDE \_ CMD \_ afficher le \_ masque**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="6cc86-120"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="6cc86-121">Masque utilisé pour obtenir la valeur utilisée pour remplacer l’état d’affichage du partage DDE, si NDDE \_ Trust \_ cmd \_ Show est défini.</span><span class="sxs-lookup"><span data-stu-id="6cc86-121">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="6cc86-122"><dt>**NDDE \_ APPROUVER \_ cmd \_ Show**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="6cc86-122"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="6cc86-123">Remplacez l’état d’affichage spécifié dans le DSDM de partage DDE.</span><span class="sxs-lookup"><span data-stu-id="6cc86-123">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="6cc86-124"><dt>**NDDE \_ TRUST \_ share \_ del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="6cc86-124"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="6cc86-125">Supprimez l’état de confiance du partage.</span><span class="sxs-lookup"><span data-stu-id="6cc86-125">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="6cc86-126"><dt>**NDDE \_ TRUST \_ share \_ init**</dt> <dt>0x40000000L</dt></span><span class="sxs-lookup"><span data-stu-id="6cc86-126"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="6cc86-127">Autoriser un client à lancer l’application s’il est déjà en cours d’exécution dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6cc86-127">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="6cc86-128"><dt>**NDDE \_ AUTORISER \_ le \_ démarrage du partage**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="6cc86-128"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="6cc86-129">Autorisez le démarrage de l’application dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6cc86-129">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="6cc86-130">*lpdwShareModId0* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6cc86-130">*lpdwShareModId0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc86-131">Pointeur vers une variable qui reçoit la première partie de l’identificateur de modification du partage approuvé.</span><span class="sxs-lookup"><span data-stu-id="6cc86-131">A pointer to a variable that receives the first part of the trusted share modify identifier.</span></span> <span data-ttu-id="6cc86-132">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="6cc86-132">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6cc86-133">*lpdwShareModId1* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6cc86-133">*lpdwShareModId1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc86-134">Pointeur vers une variable qui reçoit la deuxième partie de l’identificateur de modification du partage approuvé.</span><span class="sxs-lookup"><span data-stu-id="6cc86-134">A pointer to a variable that receives the second part of the trusted share modify identifier.</span></span> <span data-ttu-id="6cc86-135">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="6cc86-135">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc86-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cc86-136">Return value</span></span>

<span data-ttu-id="6cc86-137">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="6cc86-137">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="6cc86-138">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="6cc86-138">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6cc86-139">Notes</span><span class="sxs-lookup"><span data-stu-id="6cc86-139">Remarks</span></span>

<span data-ttu-id="6cc86-140">L’identificateur de modification de partage approuvé reflète la version du partage DDE dans le DSDM au moment où l’État approuvé a été initialement attribué au partage DDE.</span><span class="sxs-lookup"><span data-stu-id="6cc86-140">The trusted share modify identifier reflects the version of the DDE share in the DSDM at the time the DDE share was initially granted trusted status.</span></span> <span data-ttu-id="6cc86-141">L’identificateur de modification de partage approuvé est principalement utilisé pour supprimer les partages approuvés obsolètes.</span><span class="sxs-lookup"><span data-stu-id="6cc86-141">The trusted share modify identifier is primarily used to remove obsolete trusted shares.</span></span> <span data-ttu-id="6cc86-142">Toutefois, l’utilisateur n’a pas besoin de supprimer les partages approuvés obsolètes.</span><span class="sxs-lookup"><span data-stu-id="6cc86-142">However, the user does not need to remove obsolete trusted shares.</span></span> <span data-ttu-id="6cc86-143">L’agent DDE réseau supprime les partages obsolètes au nom de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6cc86-143">The network DDE agent removes obsolete shares on the user's behalf.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc86-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cc86-144">Requirements</span></span>



| <span data-ttu-id="6cc86-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cc86-145">Requirement</span></span> | <span data-ttu-id="6cc86-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cc86-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc86-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cc86-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc86-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cc86-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6cc86-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cc86-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc86-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6cc86-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6cc86-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cc86-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cc86-152"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cc86-152"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="6cc86-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cc86-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="6cc86-154"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cc86-154"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6cc86-155">DLL</span><span class="sxs-lookup"><span data-stu-id="6cc86-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cc86-156"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cc86-156"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="6cc86-157">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="6cc86-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6cc86-158">**NDdeGetTrustedShareW** (Unicode) et **NDdeGetTrustedShareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6cc86-158">**NDdeGetTrustedShareW** (Unicode) and **NDdeGetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="6cc86-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cc86-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cc86-160">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="6cc86-160">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="6cc86-161">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="6cc86-161">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="6cc86-162">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="6cc86-162">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

 




