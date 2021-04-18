---
description: Définit les informations de partage DDE. Cela s’effectue généralement après la modification.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: NDdeShareSetInfo, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512925"
---
# <a name="nddesharesetinfo-function"></a><span data-ttu-id="b8356-104">NDdeShareSetInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="b8356-104">NDdeShareSetInfo function</span></span>

<span data-ttu-id="b8356-105">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b8356-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="b8356-106">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="b8356-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="b8356-107">Définit les informations de partage DDE.</span><span class="sxs-lookup"><span data-stu-id="b8356-107">Sets DDE share information.</span></span> <span data-ttu-id="b8356-108">Cela s’effectue généralement après la modification.</span><span class="sxs-lookup"><span data-stu-id="b8356-108">This is usually done after editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8356-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8356-109">Syntax</span></span>


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a><span data-ttu-id="b8356-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8356-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8356-111">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8356-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8356-112">Nom du serveur dont le DSDM doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="b8356-112">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="b8356-113">*lpszShareName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8356-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8356-114">Nom du partage dont les informations doivent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="b8356-114">The name of the share name whose information is to be modified.</span></span> <span data-ttu-id="b8356-115">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="b8356-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8356-116">*nLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8356-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8356-117">Niveau d’information.</span><span class="sxs-lookup"><span data-stu-id="b8356-117">The information level.</span></span> <span data-ttu-id="b8356-118">Ce paramètre doit être 2.</span><span class="sxs-lookup"><span data-stu-id="b8356-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="b8356-119">*lpBuffer* \[entrée\]</span><span class="sxs-lookup"><span data-stu-id="b8356-119">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8356-120">Pointeur vers la structure [**NDDESHAREINFO**](nddeshareinfo-str.md) qui spécifie les informations de partage DDE à stocker dans le DSDM.</span><span class="sxs-lookup"><span data-stu-id="b8356-120">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that specifies the DDE share information to be stored in the DSDM.</span></span> <span data-ttu-id="b8356-121">Actuellement, les informations de partage DDE sont modifiées dans son ensemble, c’est-à-dire qu’aucune modification partielle n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="b8356-121">Currently the DDE share information is modified as a whole, that is, no partial edits are made.</span></span> <span data-ttu-id="b8356-122">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="b8356-122">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8356-123">*cBufSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8356-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8356-124">Taille de la mémoire tampon *lpBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="b8356-124">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b8356-125">*sParmNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8356-125">*sParmNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8356-126">Index de paramètre à modifier.</span><span class="sxs-lookup"><span data-stu-id="b8356-126">The parameter index to be modified.</span></span> <span data-ttu-id="b8356-127">L’implémentation actuelle ne prend pas en charge la modification partielle. par conséquent, ce paramètre doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b8356-127">The current implementation does not support partial modification; therefore, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8356-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8356-128">Return value</span></span>

<span data-ttu-id="b8356-129">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="b8356-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="b8356-130">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="b8356-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8356-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8356-131">Requirements</span></span>



| <span data-ttu-id="b8356-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8356-132">Requirement</span></span> | <span data-ttu-id="b8356-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8356-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8356-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8356-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b8356-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8356-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b8356-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8356-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b8356-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8356-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b8356-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8356-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8356-139"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8356-139"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8356-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8356-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8356-141"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8356-141"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8356-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b8356-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8356-143"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8356-143"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="b8356-144">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="b8356-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8356-145">**NDdeShareSetInfoW** (Unicode) et **NDdeShareSetInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b8356-145">**NDdeShareSetInfoW** (Unicode) and **NDdeShareSetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b8356-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8356-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8356-147">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="b8356-147">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="b8356-148">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="b8356-148">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="b8356-149">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="b8356-149">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="b8356-150">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="b8356-150">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)
</dt> </dl>

 

 




