---
description: Récupère l’adresse source d’un frame.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: GetFrameSourceAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514390"
---
# <a name="getframesourceaddress-function"></a><span data-ttu-id="66ec1-103">GetFrameSourceAddress fonction)</span><span class="sxs-lookup"><span data-stu-id="66ec1-103">GetFrameSourceAddress function</span></span>

<span data-ttu-id="66ec1-104">La fonction **GetFrameSourceAddress** récupère l’adresse source d’un frame.</span><span class="sxs-lookup"><span data-stu-id="66ec1-104">The **GetFrameSourceAddress** function retrieves the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ec1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66ec1-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="66ec1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66ec1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ec1-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="66ec1-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="66ec1-108">Handle vers le frame auquel un pointeur doit être obtenu.</span><span class="sxs-lookup"><span data-stu-id="66ec1-108">A handle to the frame for which to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="66ec1-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="66ec1-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="66ec1-110">Mémoire tampon de retour qui stocke l’adresse de la source du frame.</span><span class="sxs-lookup"><span data-stu-id="66ec1-110">A return buffer that stores the frame source address.</span></span>

</dd> <dt>

<span data-ttu-id="66ec1-111">*Typedadresse*</span><span class="sxs-lookup"><span data-stu-id="66ec1-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="66ec1-112">Type d’adresse recherchée, par exemple, \_ type d’adresse \_ Ethernet ou adresse IP du type d’adresse \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="66ec1-112">The type of address searched for, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="66ec1-113">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="66ec1-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="66ec1-114">Indicateurs utilisés pour modifier les données d’adresse source retournées.</span><span class="sxs-lookup"><span data-stu-id="66ec1-114">The flags used to modify returned source address data.</span></span>



| <span data-ttu-id="66ec1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="66ec1-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="66ec1-116">Signification</span><span class="sxs-lookup"><span data-stu-id="66ec1-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="66ec1-117"><dt>**\_normaliser les indicateurs ADDRESSTYPE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66ec1-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="66ec1-118">Annule les BITs de routage et de groupe.</span><span class="sxs-lookup"><span data-stu-id="66ec1-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="66ec1-119"><dt>**\_bit des indicateurs ADDRESSTYPE \_ \_ inversé**</dt></span><span class="sxs-lookup"><span data-stu-id="66ec1-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="66ec1-120">Rétablit la valeur normale des adresses réseau Token Ring.</span><span class="sxs-lookup"><span data-stu-id="66ec1-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ec1-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66ec1-121">Return value</span></span>

<span data-ttu-id="66ec1-122">Si la fonction réussit, la valeur *lpAddress* est valide et la valeur de retour est BHERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="66ec1-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="66ec1-123">Si la fonction échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="66ec1-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="66ec1-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="66ec1-124">Return code</span></span>                                                                                                | <span data-ttu-id="66ec1-125">Description</span><span class="sxs-lookup"><span data-stu-id="66ec1-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66ec1-126"><dt>**\_protocole BHERR \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="66ec1-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="66ec1-127">Le protocole spécifié par le paramètre *AddressType* n’est pas valide pour le frame.</span><span class="sxs-lookup"><span data-stu-id="66ec1-127">The protocol specified by the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="66ec1-128"><dt>**BHERR \_ non valide \_ HFRAME**</dt></span><span class="sxs-lookup"><span data-stu-id="66ec1-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="66ec1-129">La valeur du paramètre *hFrame* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="66ec1-129">The *hFrame* parameter value is invalid.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="66ec1-130">Notes</span><span class="sxs-lookup"><span data-stu-id="66ec1-130">Remarks</span></span>

<span data-ttu-id="66ec1-131">Le type d’adresse **\_ \_ \_ le plus élevé** est autorisé.</span><span class="sxs-lookup"><span data-stu-id="66ec1-131">An address type of **ADDRESS\_TYPE\_FIND\_HIGHEST** is allowed.</span></span> <span data-ttu-id="66ec1-132">Lorsque ce type d’adresse est utilisé, la fonction recherche l’adresse IP IPX, XNS, IP ou VINEs avant de renvoyer l’adresse ETHERNET, TOKENRING ou FDDI.</span><span class="sxs-lookup"><span data-stu-id="66ec1-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="66ec1-133">Cette approche est utile pour les protocoles et les environnements dans lesquels deux cartes réseau peuvent être multiplexées sous une seule adresse de serveur.</span><span class="sxs-lookup"><span data-stu-id="66ec1-133">This approach is useful for protocols and environments in which two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ec1-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66ec1-134">Requirements</span></span>



| <span data-ttu-id="66ec1-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66ec1-135">Requirement</span></span> | <span data-ttu-id="66ec1-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="66ec1-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66ec1-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66ec1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="66ec1-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66ec1-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="66ec1-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66ec1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="66ec1-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66ec1-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="66ec1-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="66ec1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="66ec1-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="66ec1-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="66ec1-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66ec1-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="66ec1-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66ec1-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="66ec1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="66ec1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66ec1-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66ec1-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




