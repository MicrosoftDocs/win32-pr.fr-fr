---
description: Contient des informations sur une signature numérique.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: Structure SIGNER_SIGNATURE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203041"
---
# <a name="signer_signature_info-structure"></a><span data-ttu-id="c7825-103">Structure des \_ informations de signature du signataire \_</span><span class="sxs-lookup"><span data-stu-id="c7825-103">SIGNER\_SIGNATURE\_INFO structure</span></span>

<span data-ttu-id="c7825-104">La structure d’informations sur la **\_ \_ signature du signataire** contient des informations sur une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="c7825-104">The **SIGNER\_SIGNATURE\_INFO** structure contains information about a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="c7825-105">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="c7825-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="c7825-106">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="c7825-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c7825-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7825-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a><span data-ttu-id="c7825-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c7825-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7825-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="c7825-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="c7825-110">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="c7825-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="c7825-111">**algidHash**</span><span class="sxs-lookup"><span data-stu-id="c7825-111">**algidHash**</span></span>
</dt> <dd>

<span data-ttu-id="c7825-112">Algorithme de hachage utilisé pour la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="c7825-112">The hash algorithm used for the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="c7825-113">**dwAttrChoice**</span><span class="sxs-lookup"><span data-stu-id="c7825-113">**dwAttrChoice**</span></span>
</dt> <dd>

<span data-ttu-id="c7825-114">Spécifie si la signature possède des attributs [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c7825-114">Specifies whether the signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span> <span data-ttu-id="c7825-115">Ce membre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7825-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="c7825-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7825-116">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="c7825-117">Signification</span><span class="sxs-lookup"><span data-stu-id="c7825-117">Meaning</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <span data-ttu-id="c7825-118"><dt>**Signataire \_ FACTEURS \_ attr**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c7825-118"><dt>**SIGNER\_AUTHCODE\_ATTR**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="c7825-119">La signature possède des attributs [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c7825-119">The signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <span data-ttu-id="c7825-120"><dt>**Signataire \_ AUCUN \_ attr**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c7825-120"><dt>**SIGNER\_NO\_ATTR**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="c7825-121">La signature n’a pas d’attributs [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c7825-121">The signature does not have [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c7825-122">**pAttrAuthcode**</span><span class="sxs-lookup"><span data-stu-id="c7825-122">**pAttrAuthcode**</span></span>
</dt> <dd>

<span data-ttu-id="c7825-123">Spécifie les attributs d’une signature [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c7825-123">Specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span> <span data-ttu-id="c7825-124">Ce membre est requis si la valeur du membre **dwAttrChoice** est **signer \_ facteurs \_ attr**.</span><span class="sxs-lookup"><span data-stu-id="c7825-124">This member is required if the value of the **dwAttrChoice** member is **SIGNER\_AUTHCODE\_ATTR**.</span></span>

</dd> <dt>

<span data-ttu-id="c7825-125">**psAuthenticated**</span><span class="sxs-lookup"><span data-stu-id="c7825-125">**psAuthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="c7825-126">Attributs authentifiés fournis par l’utilisateur et ajoutés à la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="c7825-126">Authenticated user-supplied attributes added to the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="c7825-127">**psUnauthenticated**</span><span class="sxs-lookup"><span data-stu-id="c7825-127">**psUnauthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="c7825-128">Attributs non authentifiés fournis par l’utilisateur ajoutés à la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="c7825-128">Unauthenticated user-supplied attributes added to the digital signature.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7825-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7825-129">Requirements</span></span>



| <span data-ttu-id="c7825-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7825-130">Requirement</span></span> | <span data-ttu-id="c7825-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7825-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c7825-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7825-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c7825-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7825-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c7825-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7825-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c7825-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7825-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7825-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7825-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7825-137">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="c7825-137">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="c7825-138">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="c7825-138">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
