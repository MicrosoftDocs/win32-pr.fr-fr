---
description: Définit le descripteur de sécurité associé au partage DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: NDdeSetShareSecurity, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522103"
---
# <a name="nddesetsharesecurity-function"></a><span data-ttu-id="87c4d-103">NDdeSetShareSecurity fonction)</span><span class="sxs-lookup"><span data-stu-id="87c4d-103">NDdeSetShareSecurity function</span></span>

<span data-ttu-id="87c4d-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="87c4d-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="87c4d-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="87c4d-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="87c4d-106">Définit le descripteur de sécurité associé au partage DDE.</span><span class="sxs-lookup"><span data-stu-id="87c4d-106">Sets the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="87c4d-107">Cela s’effectue généralement après la modification du DACL affecté au partage DDE.</span><span class="sxs-lookup"><span data-stu-id="87c4d-107">This is done usually after editing the DACL assigned to the DDE share.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c4d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87c4d-108">Syntax</span></span>


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a><span data-ttu-id="87c4d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87c4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87c4d-110">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87c4d-110">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c4d-111">Nom du serveur dont le DSDM doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="87c4d-111">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="87c4d-112">*lpszShareName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87c4d-112">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c4d-113">Nom du partage dont le descripteur de sécurité doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="87c4d-113">The name of the share whose security descriptor is to be modified.</span></span> <span data-ttu-id="87c4d-114">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="87c4d-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87c4d-115">*si* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87c4d-115">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c4d-116">Valeur [**d' \_ information de sécurité**](/windows/desktop/SecAuthZ/security-information) qui identifie les informations de sécurité à récupérer.</span><span class="sxs-lookup"><span data-stu-id="87c4d-116">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that identifies the security information to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="87c4d-117">*pSD* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87c4d-117">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c4d-118">Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) qui contient des informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="87c4d-118">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains security information.</span></span> <span data-ttu-id="87c4d-119">Ce paramètre ne peut pas être **null** et doit pointer vers un descripteur de sécurité valide.</span><span class="sxs-lookup"><span data-stu-id="87c4d-119">This parameter cannot be **NULL** and should point to a valid security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87c4d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87c4d-120">Return value</span></span>

<span data-ttu-id="87c4d-121">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="87c4d-121">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="87c4d-122">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="87c4d-122">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87c4d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="87c4d-123">Remarks</span></span>

<span data-ttu-id="87c4d-124">Pour modifier le [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associé à un partage DDE dans le DSDM, l’utilisateur doit disposer du privilège approprié ; le créateur du partage dispose de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="87c4d-124">To modify the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with a DDE share in the DSDM, the user must have appropriate privilege; the share creator has this privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="87c4d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87c4d-125">Requirements</span></span>



| <span data-ttu-id="87c4d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87c4d-126">Requirement</span></span> | <span data-ttu-id="87c4d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="87c4d-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87c4d-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c4d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="87c4d-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87c4d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="87c4d-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c4d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="87c4d-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87c4d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="87c4d-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="87c4d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="87c4d-133"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="87c4d-133"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="87c4d-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="87c4d-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="87c4d-135"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87c4d-135"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="87c4d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="87c4d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87c4d-137"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87c4d-137"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="87c4d-138">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="87c4d-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="87c4d-139">**NDdeSetShareSecurityW** (Unicode) et **NDdeSetShareSecurityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="87c4d-139">**NDdeSetShareSecurityW** (Unicode) and **NDdeSetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="87c4d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87c4d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c4d-141">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="87c4d-141">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="87c4d-142">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="87c4d-142">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="87c4d-143">**informations de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="87c4d-143">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="87c4d-144">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="87c4d-144">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)
</dt> </dl>

 

