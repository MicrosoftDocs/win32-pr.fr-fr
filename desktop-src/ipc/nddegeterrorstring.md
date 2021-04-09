---
description: Convertit un code d’erreur retourné par une fonction DDE réseau en une chaîne d’erreur qui explique le code d’erreur retourné.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: NDdeGetErrorString, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033843"
---
# <a name="nddegeterrorstring-function"></a><span data-ttu-id="41bf0-103">NDdeGetErrorString fonction)</span><span class="sxs-lookup"><span data-stu-id="41bf0-103">NDdeGetErrorString function</span></span>

<span data-ttu-id="41bf0-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="41bf0-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="41bf0-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="41bf0-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="41bf0-106">Convertit un code d’erreur retourné par une fonction DDE réseau en une chaîne d’erreur qui explique le code d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="41bf0-106">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="41bf0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41bf0-107">Syntax</span></span>


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="41bf0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41bf0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41bf0-109">*uErrorCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41bf0-109">*uErrorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41bf0-110">Code d’erreur à convertir en une chaîne d’erreur.</span><span class="sxs-lookup"><span data-stu-id="41bf0-110">The error code to be converted into an error string.</span></span>

</dd> <dt>

<span data-ttu-id="41bf0-111">*lpszErrorString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="41bf0-111">*lpszErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41bf0-112">Pointeur vers une mémoire tampon qui reçoit la chaîne d’erreur traduite.</span><span class="sxs-lookup"><span data-stu-id="41bf0-112">A pointer to a buffer that receives the translated error string.</span></span> <span data-ttu-id="41bf0-113">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="41bf0-113">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="41bf0-114">Si la mémoire tampon n’est pas assez grande pour stocker la chaîne d’erreur complète, la chaîne est tronquée.</span><span class="sxs-lookup"><span data-stu-id="41bf0-114">If the buffer is not large enough to store the complete error string, the string is truncated.</span></span>

</dd> <dt>

<span data-ttu-id="41bf0-115">*cBufSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41bf0-115">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41bf0-116">Taille de la mémoire tampon pour recevoir la chaîne d’erreur, en **TCHARs**.</span><span class="sxs-lookup"><span data-stu-id="41bf0-116">The size of the buffer to receive the error string, in **TCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41bf0-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41bf0-117">Return value</span></span>

<span data-ttu-id="41bf0-118">Si la fonction aboutit, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="41bf0-118">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="41bf0-119">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="41bf0-119">If the function fails, the return value is a nonzero error code.</span></span> <span data-ttu-id="41bf0-120">Si la mémoire tampon *lpszErrorString* n’est pas assez grande pour accepter la chaîne d’erreur complète et que la chaîne est tronquée, la fonction retourne la valeur NDDE \_ \_ erreur interne.</span><span class="sxs-lookup"><span data-stu-id="41bf0-120">If the *lpszErrorString* buffer is not large enough to accept the complete error string, and the string is truncated, the function returns the value NDDE\_INTERNAL\_ERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="41bf0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41bf0-121">Requirements</span></span>



| <span data-ttu-id="41bf0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41bf0-122">Requirement</span></span> | <span data-ttu-id="41bf0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="41bf0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41bf0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41bf0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="41bf0-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41bf0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="41bf0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41bf0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="41bf0-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41bf0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="41bf0-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="41bf0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="41bf0-129"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="41bf0-129"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="41bf0-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41bf0-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="41bf0-131"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41bf0-131"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="41bf0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="41bf0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41bf0-133"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41bf0-133"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="41bf0-134">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="41bf0-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="41bf0-135">**NDdeGetErrorStringW** (Unicode) et **NDdeGetErrorStringA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="41bf0-135">**NDdeGetErrorStringW** (Unicode) and **NDdeGetErrorStringA** (ANSI)</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="41bf0-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41bf0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41bf0-137">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="41bf0-137">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="41bf0-138">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="41bf0-138">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




