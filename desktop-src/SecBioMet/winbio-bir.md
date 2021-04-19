---
title: Structure WINBIO_BIR ( \_ types WINBIO. h)
description: Représente un enregistrement d’informations biométriques (BIR).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BIR
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516500"
---
# <a name="winbio_bir-structure"></a><span data-ttu-id="054b5-104">WINBIO \_ Bir, structure</span><span class="sxs-lookup"><span data-stu-id="054b5-104">WINBIO\_BIR structure</span></span>

<span data-ttu-id="054b5-105">La structure **WINBIO \_ Bir** représente un enregistrement d’informations biométriques (Bir).</span><span class="sxs-lookup"><span data-stu-id="054b5-105">The **WINBIO\_BIR** structure represents a biometric information record (BIR).</span></span> <span data-ttu-id="054b5-106">L’enregistrement d’informations contient des blocs d’en-tête, de données et de signature.</span><span class="sxs-lookup"><span data-stu-id="054b5-106">The information record contains header, data, and signature blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="054b5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="054b5-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a><span data-ttu-id="054b5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="054b5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="054b5-109">**HeaderBlock**</span><span class="sxs-lookup"><span data-stu-id="054b5-109">**HeaderBlock**</span></span>
</dt> <dd>

<span data-ttu-id="054b5-110">Structure [**de \_ \_ données WINBIO Bir**](winbio-bir-data.md) qui contient la taille, en octets et le décalage de l’en-tête Bir.</span><span class="sxs-lookup"><span data-stu-id="054b5-110">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the BIR header.</span></span> <span data-ttu-id="054b5-111">L’en-tête contient des informations qui décrivent le contenu de l’enregistrement d’informations.</span><span class="sxs-lookup"><span data-stu-id="054b5-111">The header contains information that describes the contents of the information record.</span></span>

</dd> <dt>

<span data-ttu-id="054b5-112">**StandardDataBlock**</span><span class="sxs-lookup"><span data-stu-id="054b5-112">**StandardDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="054b5-113">Structure [**de \_ \_ données WINBIO Bir**](winbio-bir-data.md) qui contient la taille, en octets, et l’offset des informations biométriques traitées ou non traitées créées par le Windows Biometric Framework (WBF).</span><span class="sxs-lookup"><span data-stu-id="054b5-113">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information created by the Windows Biometric Framework (WBF).</span></span>

</dd> <dt>

<span data-ttu-id="054b5-114">**VendorDataBlock**</span><span class="sxs-lookup"><span data-stu-id="054b5-114">**VendorDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="054b5-115">Structure [**de \_ \_ données WINBIO Bir**](winbio-bir-data.md) qui contient la taille, en octets, et le décalage des informations biométriques traitées ou non traitées fournies par les capteurs et logiciels du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="054b5-115">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information provided by vendor sensors and software.</span></span>

</dd> <dt>

<span data-ttu-id="054b5-116">**SignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="054b5-116">**SignatureBlock**</span></span>
</dt> <dd>

<span data-ttu-id="054b5-117">Structure de [**\_ \_ données WINBIO Bir**](winbio-bir-data.md) facultative qui contient la taille, en octets, et le décalage du code d’authentification de message de signature numérique (Mac) qui peut être utilisé pour vérifier l’intégrité du Bir.</span><span class="sxs-lookup"><span data-stu-id="054b5-117">An optional [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the digital signature message authentication code (MAC) that can be used to verify the integrity of the BIR.</span></span> <span data-ttu-id="054b5-118">Si elle est présente, la signature ou le MAC doit couvrir les blocs d’en-tête et de données.</span><span class="sxs-lookup"><span data-stu-id="054b5-118">If present, the signature or MAC must cover the header and data blocks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="054b5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="054b5-119">Remarks</span></span>

<span data-ttu-id="054b5-120">L’utilisation de décalages plutôt que de pointeurs permet de faciliter la sérialisation du BIR et de la traduction moins compliquée entre les environnements 32 et 64 bits ou entre l’utilisateur et le mode noyau.</span><span class="sxs-lookup"><span data-stu-id="054b5-120">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

<span data-ttu-id="054b5-121">BIR est compatible avec la structure Common Exchange format (CBEFF) définie par le NIST 6529-A.</span><span class="sxs-lookup"><span data-stu-id="054b5-121">The BIR is compatible with the Common Biometric Exchange Format Framework (CBEFF) defined by NIST 6529-A.</span></span>

<span data-ttu-id="054b5-122">Si cette structure contient une valeur *StandardDataBlock* , le paramètre de *type* de l’en-tête spécifié par le paramètre *HeaderBlock* doit être défini sur le **\_ \_ \_ \_ type de format ANSI 381 WINBIO**.</span><span class="sxs-lookup"><span data-stu-id="054b5-122">If this structure contains a *StandardDataBlock* value, the *Type* parameter of the header specified by the *HeaderBlock* parameter must be set to **WINBIO\_ANSI\_381\_FORMAT\_TYPE**.</span></span> <span data-ttu-id="054b5-123">Il s’agit du seul format de données standard pris en charge par la version actuelle du Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="054b5-123">This is the only standard data format supported by the current version of the Windows Biometric Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="054b5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="054b5-124">Requirements</span></span>



| <span data-ttu-id="054b5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="054b5-125">Requirement</span></span> | <span data-ttu-id="054b5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="054b5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="054b5-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="054b5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="054b5-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="054b5-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="054b5-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="054b5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="054b5-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="054b5-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="054b5-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="054b5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="054b5-132"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="054b5-132"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="054b5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="054b5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="054b5-134">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="054b5-134">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="054b5-135">**WINBIO \_ Bir \_ données**</span><span class="sxs-lookup"><span data-stu-id="054b5-135">**WINBIO\_BIR\_DATA**</span></span>](winbio-bir-data.md)
</dt> <dt>

[<span data-ttu-id="054b5-136">**\_ \_ en-tête Bir WINBIO**</span><span class="sxs-lookup"><span data-stu-id="054b5-136">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





