---
description: Crée et ajoute un nouveau partage DDE au gestionnaire de base de données du partage DDE (DSDM).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: NDdeShareAdd, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532148"
---
# <a name="nddeshareadd-function"></a><span data-ttu-id="b2572-103">NDdeShareAdd fonction)</span><span class="sxs-lookup"><span data-stu-id="b2572-103">NDdeShareAdd function</span></span>

<span data-ttu-id="b2572-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b2572-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="b2572-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="b2572-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="b2572-106">Crée et ajoute un nouveau partage DDE au gestionnaire de base de données du partage DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="b2572-106">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2572-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2572-107">Syntax</span></span>


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="b2572-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2572-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2572-109">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2572-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2572-110">Nom du serveur dont le DSDM doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="b2572-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="b2572-111">*nLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2572-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2572-112">Niveau d’information.</span><span class="sxs-lookup"><span data-stu-id="b2572-112">The information level.</span></span> <span data-ttu-id="b2572-113">Ce paramètre doit être 2.</span><span class="sxs-lookup"><span data-stu-id="b2572-113">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="b2572-114">*pSD* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2572-114">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2572-115">Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) à associer à ce partage et sur lequel les vérifications d’accès seront effectuées sur les initiaux suivants sur ce partage.</span><span class="sxs-lookup"><span data-stu-id="b2572-115">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure to be associated with this share and against which access checks will be performed on subsequent initiates to this share.</span></span> <span data-ttu-id="b2572-116">Ce paramètre peut avoir la **valeur null**, auquel cas le DSDM crée un descripteur de sécurité par défaut qui accorde le « contrôle total » au propriétaire et le « lire et lier » à tout le monde.</span><span class="sxs-lookup"><span data-stu-id="b2572-116">This parameter can be **NULL**, in which case the DSDM creates a default security descriptor that grants "Full Control" to the owner and "Read and Link" to everyone.</span></span>

</dd> <dt>

<span data-ttu-id="b2572-117">*lpBuffer* \[entrée\]</span><span class="sxs-lookup"><span data-stu-id="b2572-117">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2572-118">Pointeur vers la structure [**NDDESHAREINFO**](nddeshareinfo-str.md) qui définit la liste ApplicationTopic associée au partage DDE créé, ainsi que d’autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="b2572-118">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that defines the ApplicationTopic list associated with the DDE share being created as well as other parameters.</span></span> <span data-ttu-id="b2572-119">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="b2572-119">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b2572-120">*cBufSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2572-120">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2572-121">Taille de la structure *lpBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="b2572-121">The size of the *lpBuffer* structure, in bytes.</span></span> <span data-ttu-id="b2572-122">Ce paramètre ne peut pas être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="b2572-122">This parameter cannot be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2572-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2572-123">Return value</span></span>

<span data-ttu-id="b2572-124">Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="b2572-124">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="b2572-125">Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="b2572-125">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2572-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b2572-126">Remarks</span></span>

<span data-ttu-id="b2572-127">Pour qu’un client puisse se connecter au partage DDE, il doit être approuvé avec [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span><span class="sxs-lookup"><span data-stu-id="b2572-127">Before a client can connect to the DDE share, it must be trusted with [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2572-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2572-128">Requirements</span></span>



| <span data-ttu-id="b2572-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2572-129">Requirement</span></span> | <span data-ttu-id="b2572-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2572-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2572-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2572-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b2572-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2572-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b2572-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2572-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b2572-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2572-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b2572-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2572-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2572-136"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2572-136"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2572-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b2572-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2572-138"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2572-138"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b2572-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b2572-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2572-140"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2572-140"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2572-141">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="b2572-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b2572-142">**NDdeShareAddW** (Unicode) et **NDdeShareAddA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b2572-142">**NDdeShareAddW** (Unicode) and **NDdeShareAddA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="b2572-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2572-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2572-144">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="b2572-144">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="b2572-145">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="b2572-145">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="b2572-146">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="b2572-146">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="b2572-147">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="b2572-147">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

