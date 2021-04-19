---
description: Récupère les informations de partage DDE. Cette opération est généralement effectuée pour la modification.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: NDdeShareGetInfo, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536955"
---
# <a name="nddesharegetinfo-function"></a><span data-ttu-id="6e871-104">NDdeShareGetInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="6e871-104">NDdeShareGetInfo function</span></span>

<span data-ttu-id="6e871-105">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6e871-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="6e871-106">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="6e871-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="6e871-107">Récupère les informations de partage DDE.</span><span class="sxs-lookup"><span data-stu-id="6e871-107">Retrieves DDE share information.</span></span> <span data-ttu-id="6e871-108">Cette opération est généralement effectuée pour la modification.</span><span class="sxs-lookup"><span data-stu-id="6e871-108">This is usually done for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e871-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e871-109">Syntax</span></span>


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a><span data-ttu-id="6e871-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e871-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e871-111">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e871-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e871-112">Nom du serveur sur lequel le DSDM réside.</span><span class="sxs-lookup"><span data-stu-id="6e871-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="6e871-113">*lpszShareName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e871-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e871-114">Nom du partage dont les informations doivent être récupérées à partir du DSDM.</span><span class="sxs-lookup"><span data-stu-id="6e871-114">The share name whose information is to be retrieved from the DSDM.</span></span> <span data-ttu-id="6e871-115">Ce paramètre ne doit pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6e871-115">This parameter must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e871-116">*nLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e871-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e871-117">Niveau d’information.</span><span class="sxs-lookup"><span data-stu-id="6e871-117">The information level.</span></span> <span data-ttu-id="6e871-118">Ce paramètre doit être 2.</span><span class="sxs-lookup"><span data-stu-id="6e871-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="6e871-119">*lpBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e871-119">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e871-120">Pointeur vers une mémoire tampon qui reçoit la structure [**NDDESHAREINFO**](nddeshareinfo-str.md) et les données associées pointées par ses membres.</span><span class="sxs-lookup"><span data-stu-id="6e871-120">A pointer to a buffer that receives the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure and associated data pointed to by its members.</span></span> <span data-ttu-id="6e871-121">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6e871-121">This parameter can be **NULL**.</span></span> <span data-ttu-id="6e871-122">Si *lpBuffer* a la valeur **null**, le DSDM calcule le nombre d’octets nécessaires pour stocker les informations de partage demandées et retourne cette valeur dans le champ *lpnTotalAvailable* avec l' \_ erreur NDDE buf \_ insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="6e871-122">If *lpBuffer* is **NULL**, then the DSDM calculates the number of bytes required to store the requested share information and returns that value in the *lpnTotalAvailable* field along with the NDDE\_BUF\_TOO\_SMALL error.</span></span>

</dd> <dt>

<span data-ttu-id="6e871-123">*cBufSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e871-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e871-124">Taille de la mémoire tampon *lpBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="6e871-124">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="6e871-125">Si *lpBuffer* a la **valeur null**, *cBufSize* doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6e871-125">If *lpBuffer* is **NULL**, then *cBufSize* should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6e871-126">*lpnTotalAvailable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e871-126">*lpnTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e871-127">Pointeur vers une variable qui reçoit le nombre total d’octets nécessaires pour stocker les informations de partage demandées.</span><span class="sxs-lookup"><span data-stu-id="6e871-127">A pointer to a variable that receives the total number of bytes needed to store the requested share information.</span></span> <span data-ttu-id="6e871-128">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="6e871-128">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e871-129">*lpnItems* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e871-129">*lpnItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e871-130">Pointeur vers un masque de sélection d’élément pour la récupération d’informations de partage partielles.</span><span class="sxs-lookup"><span data-stu-id="6e871-130">A pointer to an item selection mask for partial share information retrieval.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e871-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e871-131">Return value</span></span>

<span data-ttu-id="6e871-132">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="6e871-132">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="6e871-133">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="6e871-133">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="6e871-134">Si le paramètre *lpBuffer* a la **valeur null**, il retourne NDDE \_ buf \_ trop \_ petit.</span><span class="sxs-lookup"><span data-stu-id="6e871-134">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e871-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e871-135">Requirements</span></span>



| <span data-ttu-id="6e871-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e871-136">Requirement</span></span> | <span data-ttu-id="6e871-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e871-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e871-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e871-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6e871-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e871-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6e871-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e871-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6e871-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e871-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6e871-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e871-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e871-143"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e871-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e871-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6e871-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e871-145"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e871-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e871-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6e871-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e871-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e871-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e871-148">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="6e871-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6e871-149">**NDdeShareGetInfoW** (Unicode) et **NDdeShareGetInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6e871-149">**NDdeShareGetInfoW** (Unicode) and **NDdeShareGetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6e871-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e871-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e871-151">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="6e871-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="6e871-152">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="6e871-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="6e871-153">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="6e871-153">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="6e871-154">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="6e871-154">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> </dl>

 

 




