---
description: Récupère le descripteur de sécurité associé au partage DDE. Cela s’effectue généralement pour la modification.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: NDdeGetShareSecurity, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868353"
---
# <a name="nddegetsharesecurity-function"></a><span data-ttu-id="16271-104">NDdeGetShareSecurity fonction)</span><span class="sxs-lookup"><span data-stu-id="16271-104">NDdeGetShareSecurity function</span></span>

<span data-ttu-id="16271-105">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="16271-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="16271-106">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="16271-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="16271-107">Récupère le descripteur de sécurité associé au partage DDE.</span><span class="sxs-lookup"><span data-stu-id="16271-107">Retrieves the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="16271-108">Cela s’effectue généralement pour la modification.</span><span class="sxs-lookup"><span data-stu-id="16271-108">This is done usually for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="16271-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16271-109">Syntax</span></span>


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a><span data-ttu-id="16271-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16271-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16271-111">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16271-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16271-112">Nom du serveur sur lequel le DSDM réside.</span><span class="sxs-lookup"><span data-stu-id="16271-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="16271-113">*lpszShareName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16271-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16271-114">Nom du partage dont le descripteur de sécurité doit être récupéré à partir du DSDM.</span><span class="sxs-lookup"><span data-stu-id="16271-114">The name of the share whose security descriptor is to be retrieved from the DSDM.</span></span> <span data-ttu-id="16271-115">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="16271-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="16271-116">*si* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16271-116">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16271-117">Valeur [**des \_ informations de sécurité**](/windows/desktop/SecAuthZ/security-information) qui spécifie les informations de sécurité à récupérer du descripteur de sécurité associé au partage.</span><span class="sxs-lookup"><span data-stu-id="16271-117">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that specifies the security information to be retrieved from the security descriptor associated with the share.</span></span>

</dd> <dt>

<span data-ttu-id="16271-118">*pSD* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="16271-118">*pSD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16271-119">Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) qui reçoit le descripteur de sécurité auto-relatif.</span><span class="sxs-lookup"><span data-stu-id="16271-119">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that receives the self-relative security descriptor.</span></span> <span data-ttu-id="16271-120">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="16271-120">This parameter can be **NULL**.</span></span> <span data-ttu-id="16271-121">Si ce paramètre a la **valeur null**, le DSDM détermine la taille des informations de sécurité demandées et retourne le nombre d’octets nécessaires dans le paramètre *lpcbsdRequired* avec le code d' \_ erreur NDDE buf \_ trop \_ petit.</span><span class="sxs-lookup"><span data-stu-id="16271-121">If this parameter is **NULL**, the DSDM determines the size of the requested security information and returns the number of bytes needed in the *lpcbsdRequired* parameter along with the NDDE\_BUF\_TOO\_SMALL error code.</span></span>

</dd> <dt>

<span data-ttu-id="16271-122">*cbSD* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16271-122">*cbSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16271-123">Taille de la mémoire tampon *pSD* .</span><span class="sxs-lookup"><span data-stu-id="16271-123">The size of the *pSD* buffer.</span></span> <span data-ttu-id="16271-124">Ce paramètre doit être égal à zéro si *pSD* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="16271-124">This parameter must be zero if *pSD* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="16271-125">*lpcbsdRequired* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="16271-125">*lpcbsdRequired* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16271-126">Pointeur vers la variable qui reçoit la taille réelle du descripteur de sécurité récupéré.</span><span class="sxs-lookup"><span data-stu-id="16271-126">A pointer to the variable that receives the actual size of the retrieved security descriptor.</span></span> <span data-ttu-id="16271-127">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="16271-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16271-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16271-128">Return value</span></span>

<span data-ttu-id="16271-129">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="16271-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="16271-130">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="16271-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="16271-131">Si le paramètre *pSD* était **null**, il retourne NDDE \_ buf \_ trop \_ petit.</span><span class="sxs-lookup"><span data-stu-id="16271-131">If the *pSD* parameter was **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="16271-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16271-132">Requirements</span></span>



| <span data-ttu-id="16271-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16271-133">Requirement</span></span> | <span data-ttu-id="16271-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="16271-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16271-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16271-135">Minimum supported client</span></span><br/> | <span data-ttu-id="16271-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16271-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="16271-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16271-137">Minimum supported server</span></span><br/> | <span data-ttu-id="16271-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16271-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="16271-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="16271-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="16271-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="16271-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="16271-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16271-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="16271-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16271-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="16271-143">DLL</span><span class="sxs-lookup"><span data-stu-id="16271-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16271-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16271-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="16271-145">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="16271-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="16271-146">**NDdeGetShareSecurityW** (Unicode) et **NDdeGetShareSecurityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="16271-146">**NDdeGetShareSecurityW** (Unicode) and **NDdeGetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="16271-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16271-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16271-148">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="16271-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="16271-149">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="16271-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="16271-150">**informations de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="16271-150">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="16271-151">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="16271-151">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> </dl>

 

