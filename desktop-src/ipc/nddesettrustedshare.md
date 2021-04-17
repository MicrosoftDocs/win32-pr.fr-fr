---
description: Octroie l’état de confiance du partage DDE spécifié dans le contexte de l’utilisateur actuel.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: NDdeSetTrustedShare, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524952"
---
# <a name="nddesettrustedshare-function"></a><span data-ttu-id="afd7b-103">NDdeSetTrustedShare fonction)</span><span class="sxs-lookup"><span data-stu-id="afd7b-103">NDdeSetTrustedShare function</span></span>

<span data-ttu-id="afd7b-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="afd7b-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="afd7b-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="afd7b-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="afd7b-106">Octroie l’état de confiance du partage DDE spécifié dans le contexte de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="afd7b-106">Grants the specified DDE share trusted status within the current user's context.</span></span>

## <a name="syntax"></a><span data-ttu-id="afd7b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afd7b-107">Syntax</span></span>


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a><span data-ttu-id="afd7b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="afd7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd7b-109">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="afd7b-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd7b-110">Nom du serveur dont le DSDM doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="afd7b-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="afd7b-111">*lpszShareName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="afd7b-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd7b-112">Nom du partage auquel attribuer l’État approuvé.</span><span class="sxs-lookup"><span data-stu-id="afd7b-112">The name of the share to be granted trusted status.</span></span> <span data-ttu-id="afd7b-113">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="afd7b-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="afd7b-114">*dwTrustOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="afd7b-114">*dwTrustOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd7b-115">Options affectant l’État approuvé du partage DDE.</span><span class="sxs-lookup"><span data-stu-id="afd7b-115">The options affecting the trusted status of the DDE share.</span></span> <span data-ttu-id="afd7b-116">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="afd7b-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="afd7b-117">Option</span><span class="sxs-lookup"><span data-stu-id="afd7b-117">Option</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="afd7b-118">Signification</span><span class="sxs-lookup"><span data-stu-id="afd7b-118">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="afd7b-119"><dt>**NDDE \_ CMD \_ afficher le \_ masque**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-119"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="afd7b-120">Masque utilisé pour obtenir la valeur utilisée pour remplacer l’état d’affichage du partage DDE, si NDDE \_ Trust \_ cmd \_ Show est défini.</span><span class="sxs-lookup"><span data-stu-id="afd7b-120">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="afd7b-121"><dt>**NDDE \_ APPROUVER \_ cmd \_ Show**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-121"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="afd7b-122">Remplacez l’état d’affichage spécifié dans le DSDM de partage DDE.</span><span class="sxs-lookup"><span data-stu-id="afd7b-122">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="afd7b-123"><dt>**NDDE \_ TRUST \_ share \_ del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-123"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="afd7b-124">Supprimez l’état de confiance du partage.</span><span class="sxs-lookup"><span data-stu-id="afd7b-124">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="afd7b-125"><dt>**NDDE \_ TRUST \_ share \_ init**</dt> <dt>0x40000000L</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-125"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="afd7b-126">Autoriser un client à lancer l’application s’il est déjà en cours d’exécution dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afd7b-126">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="afd7b-127"><dt>**NDDE \_ AUTORISER \_ le \_ démarrage du partage**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-127"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="afd7b-128">Autorisez le démarrage de l’application dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afd7b-128">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afd7b-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="afd7b-129">Return value</span></span>

<span data-ttu-id="afd7b-130">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="afd7b-130">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="afd7b-131">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="afd7b-131">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="afd7b-132">Notes</span><span class="sxs-lookup"><span data-stu-id="afd7b-132">Remarks</span></span>

<span data-ttu-id="afd7b-133">Le partage DDE doit d’abord être créé avec [**NDdeShareAdd**](nddeshareadd.md).</span><span class="sxs-lookup"><span data-stu-id="afd7b-133">The DDE share must first be created with [**NDdeShareAdd**](nddeshareadd.md).</span></span>

<span data-ttu-id="afd7b-134">Si **NDdeSetTrustedShare** est appelé avec *dwTrustOptions* défini à zéro, le partage approuvé perd son état approuvé.</span><span class="sxs-lookup"><span data-stu-id="afd7b-134">If **NDdeSetTrustedShare** is called with *dwTrustOptions* set to zero, the trusted share loses its trusted status.</span></span>

## <a name="requirements"></a><span data-ttu-id="afd7b-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afd7b-135">Requirements</span></span>



| <span data-ttu-id="afd7b-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afd7b-136">Requirement</span></span> | <span data-ttu-id="afd7b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="afd7b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afd7b-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afd7b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="afd7b-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afd7b-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="afd7b-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afd7b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="afd7b-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afd7b-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="afd7b-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="afd7b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="afd7b-143"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="afd7b-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="afd7b-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="afd7b-145"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="afd7b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="afd7b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afd7b-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afd7b-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="afd7b-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="afd7b-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="afd7b-149">**NDdeSetTrustedShareW** (Unicode) et **NDdeSetTrustedShareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="afd7b-149">**NDdeSetTrustedShareW** (Unicode) and **NDdeSetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="afd7b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afd7b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd7b-151">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="afd7b-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="afd7b-152">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="afd7b-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="afd7b-153">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="afd7b-153">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




