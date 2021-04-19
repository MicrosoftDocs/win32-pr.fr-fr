---
description: Supprime un partage DDE du gestionnaire de base de données du partage DDE (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: NDdeShareDel, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536107"
---
# <a name="nddesharedel-function"></a><span data-ttu-id="6ec7e-103">NDdeShareDel fonction)</span><span class="sxs-lookup"><span data-stu-id="6ec7e-103">NDdeShareDel function</span></span>

<span data-ttu-id="6ec7e-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6ec7e-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="6ec7e-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="6ec7e-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="6ec7e-106">Supprime un partage DDE du gestionnaire de base de données du partage DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="6ec7e-106">Deletes a DDE share from the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec7e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ec7e-107">Syntax</span></span>


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a><span data-ttu-id="6ec7e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ec7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec7e-109">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ec7e-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec7e-110">Nom du serveur dont le DSDM doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="6ec7e-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="6ec7e-111">*lpszShareName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ec7e-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec7e-112">Nom du partage à supprimer du DSDM.</span><span class="sxs-lookup"><span data-stu-id="6ec7e-112">The name of the share to be deleted from the DSDM.</span></span> <span data-ttu-id="6ec7e-113">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="6ec7e-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6ec7e-114">*wReserved* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ec7e-114">*wReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec7e-115">Réservé.</span><span class="sxs-lookup"><span data-stu-id="6ec7e-115">Reserved.</span></span> <span data-ttu-id="6ec7e-116">Ce paramètre doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6ec7e-116">This parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec7e-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ec7e-117">Return value</span></span>

<span data-ttu-id="6ec7e-118">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="6ec7e-118">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="6ec7e-119">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en un message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="6ec7e-119">If the function fails, the return value is an error code which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec7e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="6ec7e-120">Remarks</span></span>

<span data-ttu-id="6ec7e-121">Pour supprimer un partage DDE du DSDM, vous devez disposer des privilèges appropriés.</span><span class="sxs-lookup"><span data-stu-id="6ec7e-121">To delete a DDE share from the DSDM, you must have the appropriate privilege.</span></span> <span data-ttu-id="6ec7e-122">Le créateur du partage a le privilège supprimer.</span><span class="sxs-lookup"><span data-stu-id="6ec7e-122">The share creator has delete privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec7e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ec7e-123">Requirements</span></span>



| <span data-ttu-id="6ec7e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ec7e-124">Requirement</span></span> | <span data-ttu-id="6ec7e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ec7e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec7e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ec7e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec7e-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ec7e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6ec7e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ec7e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec7e-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ec7e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6ec7e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ec7e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ec7e-131"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec7e-131"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ec7e-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ec7e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ec7e-133"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ec7e-133"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ec7e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6ec7e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec7e-135"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec7e-135"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ec7e-136">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="6ec7e-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6ec7e-137">**NDdeShareDelW** (Unicode) et **NDdeShareDelA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6ec7e-137">**NDdeShareDelW** (Unicode) and **NDdeShareDelA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="6ec7e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ec7e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec7e-139">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="6ec7e-139">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="6ec7e-140">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="6ec7e-140">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




