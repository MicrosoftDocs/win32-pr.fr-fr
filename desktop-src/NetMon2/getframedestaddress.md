---
description: Récupère l’adresse de destination d’un frame.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: GetFrameDestAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950969"
---
# <a name="getframedestaddress-function"></a><span data-ttu-id="727f3-103">GetFrameDestAddress fonction)</span><span class="sxs-lookup"><span data-stu-id="727f3-103">GetFrameDestAddress function</span></span>

<span data-ttu-id="727f3-104">La fonction **GetFrameDestAddress** récupère l’adresse de destination d’un frame.</span><span class="sxs-lookup"><span data-stu-id="727f3-104">The **GetFrameDestAddress** function retrieves the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="727f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="727f3-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="727f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="727f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="727f3-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="727f3-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="727f3-108">Handle du frame vers lequel obtenir un pointeur.</span><span class="sxs-lookup"><span data-stu-id="727f3-108">A handle of the frame to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="727f3-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="727f3-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="727f3-110">Mémoire tampon de retour qui stocke l’adresse de destination du frame.</span><span class="sxs-lookup"><span data-stu-id="727f3-110">A return buffer that stores the frame destination address.</span></span>

</dd> <dt>

<span data-ttu-id="727f3-111">*Typedadresse*</span><span class="sxs-lookup"><span data-stu-id="727f3-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="727f3-112">Type d’adresse (par exemple, type d’adresse \_ \_ Ethernet ou adresse IP de type d’adresse) \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="727f3-112">A type of address, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="727f3-113">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="727f3-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="727f3-114">Indicateurs utilisés pour modifier les données d’adresse de destination retournées.</span><span class="sxs-lookup"><span data-stu-id="727f3-114">The flags used to modify returned destination address data.</span></span>



| <span data-ttu-id="727f3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="727f3-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="727f3-116">Signification</span><span class="sxs-lookup"><span data-stu-id="727f3-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="727f3-117"><dt>**\_normaliser les indicateurs ADDRESSTYPE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="727f3-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="727f3-118">Annule les BITs de routage et de groupe.</span><span class="sxs-lookup"><span data-stu-id="727f3-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="727f3-119"><dt>**\_bit des indicateurs ADDRESSTYPE \_ \_ inversé**</dt></span><span class="sxs-lookup"><span data-stu-id="727f3-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="727f3-120">Rétablit la valeur normale des adresses réseau Token Ring.</span><span class="sxs-lookup"><span data-stu-id="727f3-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="727f3-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="727f3-121">Return value</span></span>

<span data-ttu-id="727f3-122">Si la fonction réussit, la valeur *lpAddress* est valide et la valeur de retour est BHERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="727f3-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="727f3-123">Si la fonction échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="727f3-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="727f3-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="727f3-124">Return code</span></span>                                                                                                | <span data-ttu-id="727f3-125">Description</span><span class="sxs-lookup"><span data-stu-id="727f3-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="727f3-126"><dt>**\_protocole BHERR \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="727f3-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="727f3-127">Le protocole spécifié dans le paramètre *AddressType* n’est pas valide pour le frame.</span><span class="sxs-lookup"><span data-stu-id="727f3-127">The specified protocol in the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="727f3-128"><dt>**BHERR \_ non valide \_ HFRAME**</dt></span><span class="sxs-lookup"><span data-stu-id="727f3-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="727f3-129">La valeur *hFrame* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="727f3-129">The *hFrame* value is invalid.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="727f3-130">Notes</span><span class="sxs-lookup"><span data-stu-id="727f3-130">Remarks</span></span>

<span data-ttu-id="727f3-131">Le type d’adresse Rechercher le type d’adresse le **\_ \_ \_ plus élevé** est autorisé.</span><span class="sxs-lookup"><span data-stu-id="727f3-131">The **ADDRESS\_TYPE\_FIND\_HIGHEST** address type is allowed.</span></span> <span data-ttu-id="727f3-132">Lorsque ce type d’adresse est utilisé, la fonction recherche l’adresse IP IPX, XNS, IP ou VINEs avant de renvoyer l’adresse ETHERNET, TOKENRING ou FDDI.</span><span class="sxs-lookup"><span data-stu-id="727f3-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="727f3-133">Cette approche est utile pour les protocoles et dans les environnements où deux cartes réseau peuvent être multiplexées sous une seule adresse de serveur.</span><span class="sxs-lookup"><span data-stu-id="727f3-133">This approach is useful for protocols and in environments where two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="727f3-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="727f3-134">Requirements</span></span>



| <span data-ttu-id="727f3-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="727f3-135">Requirement</span></span> | <span data-ttu-id="727f3-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="727f3-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="727f3-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="727f3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="727f3-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="727f3-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="727f3-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="727f3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="727f3-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="727f3-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="727f3-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="727f3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="727f3-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="727f3-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="727f3-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="727f3-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="727f3-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="727f3-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="727f3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="727f3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="727f3-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="727f3-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




