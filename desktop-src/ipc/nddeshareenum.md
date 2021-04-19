---
description: Récupère la liste des partages DDE disponibles.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: NDdeShareEnum, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519442"
---
# <a name="nddeshareenum-function"></a><span data-ttu-id="e4308-103">NDdeShareEnum fonction)</span><span class="sxs-lookup"><span data-stu-id="e4308-103">NDdeShareEnum function</span></span>

<span data-ttu-id="e4308-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e4308-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="e4308-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="e4308-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="e4308-106">Récupère la liste des partages DDE disponibles.</span><span class="sxs-lookup"><span data-stu-id="e4308-106">Retrieves the list of available DDE shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4308-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4308-107">Syntax</span></span>


```C++
UINT NDdeShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="e4308-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4308-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4308-109">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4308-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4308-110">Nom du serveur sur lequel le DSDM réside.</span><span class="sxs-lookup"><span data-stu-id="e4308-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="e4308-111">*nLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4308-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4308-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e4308-112">Reserved.</span></span> <span data-ttu-id="e4308-113">Ce paramètre doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e4308-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e4308-114">*lpBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e4308-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4308-115">Pointeur vers une mémoire tampon qui reçoit la liste des partages DDE.</span><span class="sxs-lookup"><span data-stu-id="e4308-115">A pointer to a buffer that receives the list of DDE shares.</span></span> <span data-ttu-id="e4308-116">La liste des partages DDE est stockée sous la forme d’une séquence de chaînes séparées par des valeurs NULL qui se terminent par un caractère null double à la fin.</span><span class="sxs-lookup"><span data-stu-id="e4308-116">The list of DDE shares is stored as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="e4308-117">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e4308-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="e4308-118">Si *lpBuffer* a la **valeur null**, le DSDM retourne la taille de la mémoire tampon requise pour contenir la liste de partages dans le paramètre *lpcbTotalAvailable* .</span><span class="sxs-lookup"><span data-stu-id="e4308-118">If *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e4308-119">*cBufSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4308-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4308-120">Taille de la mémoire tampon *lpBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="e4308-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="e4308-121">Ce paramètre doit être égal à zéro si *lpBuffer* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e4308-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e4308-122">*lpnEntriesRead* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e4308-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4308-123">Pointeur vers une variable qui reçoit le nombre total de partages qui sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="e4308-123">A pointer to a variable that receives the total number of shares being enumerated.</span></span> <span data-ttu-id="e4308-124">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="e4308-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e4308-125">*lpcbTotalAvailable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e4308-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4308-126">Pointeur vers une variable qui reçoit le nombre total d’octets nécessaires dans la mémoire tampon pour stocker la liste des partages DDE.</span><span class="sxs-lookup"><span data-stu-id="e4308-126">A pointer to a variable that receives the total number of bytes needed in the buffer to store the list of DDE shares.</span></span> <span data-ttu-id="e4308-127">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="e4308-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4308-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4308-128">Return value</span></span>

<span data-ttu-id="e4308-129">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="e4308-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="e4308-130">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="e4308-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="e4308-131">Si le paramètre *lpBuffer* a la **valeur null**, il retourne NDDE \_ buf \_ trop \_ petit.</span><span class="sxs-lookup"><span data-stu-id="e4308-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4308-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4308-132">Requirements</span></span>



| <span data-ttu-id="e4308-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4308-133">Requirement</span></span> | <span data-ttu-id="e4308-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4308-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4308-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4308-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e4308-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4308-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e4308-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4308-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e4308-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4308-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4308-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4308-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4308-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4308-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4308-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4308-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4308-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4308-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e4308-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e4308-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4308-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4308-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="e4308-145">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e4308-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e4308-146">**NDdeShareEnumW** (Unicode) et **NDdeShareEnumA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e4308-146">**NDdeShareEnumW** (Unicode) and **NDdeShareEnumA** (ANSI)</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="e4308-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4308-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4308-148">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="e4308-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="e4308-149">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="e4308-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




