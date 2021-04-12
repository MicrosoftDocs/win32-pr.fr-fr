---
description: Récupère les noms de tous les partages DDE réseau approuvés dans le contexte du processus appelant.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: NDdeTrustedShareEnum, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320274"
---
# <a name="nddetrustedshareenum-function"></a><span data-ttu-id="6df66-103">NDdeTrustedShareEnum fonction)</span><span class="sxs-lookup"><span data-stu-id="6df66-103">NDdeTrustedShareEnum function</span></span>

<span data-ttu-id="6df66-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6df66-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="6df66-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="6df66-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="6df66-106">Récupère les noms de tous les partages DDE réseau approuvés dans le contexte du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="6df66-106">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df66-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6df66-107">Syntax</span></span>


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="6df66-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6df66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df66-109">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6df66-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df66-110">Nom du serveur sur lequel le DSDM réside.</span><span class="sxs-lookup"><span data-stu-id="6df66-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="6df66-111">*nLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6df66-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df66-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="6df66-112">Reserved.</span></span> <span data-ttu-id="6df66-113">Ce paramètre doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6df66-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6df66-114">*lpBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6df66-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6df66-115">Pointeur vers une mémoire tampon qui reçoit la liste des partages DDE approuvés.</span><span class="sxs-lookup"><span data-stu-id="6df66-115">A pointer to a buffer that receives the list of trusted DDE shares.</span></span> <span data-ttu-id="6df66-116">La liste des partages DDE approuvés est retournée sous la forme d’une séquence de chaînes séparées par des valeurs NULL qui se terminent par un caractère double null à la fin.</span><span class="sxs-lookup"><span data-stu-id="6df66-116">The list of trusted DDE shares is returned as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="6df66-117">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6df66-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="6df66-118">Si *lpBuffer* a la **valeur null**, le DSDM retourne la taille de la mémoire tampon requise pour contenir la liste des partages dans le champ *lpcbTotalAvailable* .</span><span class="sxs-lookup"><span data-stu-id="6df66-118">If the *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* field.</span></span>

</dd> <dt>

<span data-ttu-id="6df66-119">*cBufSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6df66-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df66-120">Taille de la mémoire tampon *lpBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="6df66-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="6df66-121">Ce paramètre doit être égal à zéro si *lpBuffer* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6df66-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6df66-122">*lpnEntriesRead* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6df66-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6df66-123">Pointeur vers une variable qui reçoit le nombre total de partages approuvés en cours d’énumération.</span><span class="sxs-lookup"><span data-stu-id="6df66-123">A pointer to a variable that receives the total number of trusted shares being enumerated.</span></span> <span data-ttu-id="6df66-124">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="6df66-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6df66-125">*lpcbTotalAvailable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6df66-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6df66-126">Pointeur vers une variable qui reçoit le nombre total d’octets nécessaires pour stocker la liste des partages DDE approuvés.</span><span class="sxs-lookup"><span data-stu-id="6df66-126">A pointer to a variable that receives the total number of bytes needed to store the list of trusted DDE shares.</span></span> <span data-ttu-id="6df66-127">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="6df66-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df66-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6df66-128">Return value</span></span>

<span data-ttu-id="6df66-129">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="6df66-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="6df66-130">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="6df66-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="6df66-131">Si le paramètre *lpBuffer* a la **valeur null**, il retourne NDDE \_ buf \_ trop \_ petit.</span><span class="sxs-lookup"><span data-stu-id="6df66-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df66-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6df66-132">Requirements</span></span>



| <span data-ttu-id="6df66-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6df66-133">Requirement</span></span> | <span data-ttu-id="6df66-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="6df66-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6df66-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6df66-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6df66-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6df66-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6df66-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6df66-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6df66-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6df66-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6df66-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="6df66-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6df66-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6df66-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="6df66-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6df66-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="6df66-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6df66-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6df66-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6df66-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6df66-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6df66-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="6df66-145">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="6df66-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6df66-146">**NDdeTrustedShareEnumW** (Unicode) et **NDdeTrustedShareEnumA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6df66-146">**NDdeTrustedShareEnumW** (Unicode) and **NDdeTrustedShareEnumA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="6df66-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6df66-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df66-148">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="6df66-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="6df66-149">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="6df66-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




