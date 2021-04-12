---
title: Structure WINBIO_REGISTERED_FORMAT ( \_ types WINBIO. h)
description: Spécifie un format de données inscrit comme une paire propriétaire/format.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- API de Windows Biometric Framework de structure de WINBIO_REGISTERED_FORMAT
- API du pointeur de structure PWINBIO_REGISTERED_FORMAT Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508594"
---
# <a name="winbio_registered_format-structure"></a><span data-ttu-id="03df1-105">\_Structure de format inscrite WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="03df1-105">WINBIO\_REGISTERED\_FORMAT structure</span></span>

<span data-ttu-id="03df1-106">La structure de **\_ \_ format inscrite WINBIO** spécifie un format de données inscrit comme une paire propriétaire/format.</span><span class="sxs-lookup"><span data-stu-id="03df1-106">The **WINBIO\_REGISTERED\_FORMAT** structure specifies a registered data format as an owner/format pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="03df1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03df1-107">Syntax</span></span>


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a><span data-ttu-id="03df1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="03df1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="03df1-109">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="03df1-109">**Owner**</span></span>
</dt> <dd>

<span data-ttu-id="03df1-110">Valeur propriétaire assignée à IBIA (International Biometric Industry Association).</span><span class="sxs-lookup"><span data-stu-id="03df1-110">An IBIA (International Biometric Industry Association) assigned owner value.</span></span>

</dd> <dt>

<span data-ttu-id="03df1-111">**Type**</span><span class="sxs-lookup"><span data-stu-id="03df1-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="03df1-112">Format assigné par le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="03df1-112">An owner assigned format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03df1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="03df1-113">Remarks</span></span>

<span data-ttu-id="03df1-114">Étant donné que Windows ne prend actuellement en charge que les lecteurs d’empreintes digitales, les valeurs suivantes doivent être utilisées dans la structure de **\_ \_ format inscrit WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="03df1-114">Because Windows currently supports only fingerprint readers, the following values should be used in the **WINBIO\_REGISTERED\_FORMAT** structure.</span></span>



| <span data-ttu-id="03df1-115">Constante</span><span class="sxs-lookup"><span data-stu-id="03df1-115">Constant</span></span>                                    | <span data-ttu-id="03df1-116">Signification</span><span class="sxs-lookup"><span data-stu-id="03df1-116">Meaning</span></span>                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03df1-117">\_Propriétaire du \_ FORMAT ANSI 381 \_ \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="03df1-117">WINBIO\_ANSI\_381\_FORMAT\_OWNER</span></span><br/> | <span data-ttu-id="03df1-118">InterNational Committee for Information Technology Standards (INCITS) Technical Committee M1 (biométrique).</span><span class="sxs-lookup"><span data-stu-id="03df1-118">InterNational Committee for Information Technology Standards (INCITS) technical committee M1 (biometrics).</span></span><br/> |
| <span data-ttu-id="03df1-119">\_Type de \_ FORMAT ANSI 381 \_ \_ WINBIO</span><span class="sxs-lookup"><span data-stu-id="03df1-119">WINBIO\_ANSI\_381\_FORMAT\_TYPE</span></span><br/>  | <span data-ttu-id="03df1-120">Format d’échange de données basé sur l’image Finger ANSI INCITS 381.</span><span class="sxs-lookup"><span data-stu-id="03df1-120">ANSI INCITS 381 finger image based data interchange format.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="03df1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03df1-121">Requirements</span></span>



| <span data-ttu-id="03df1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03df1-122">Requirement</span></span> | <span data-ttu-id="03df1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="03df1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03df1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03df1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="03df1-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03df1-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="03df1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03df1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="03df1-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03df1-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="03df1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="03df1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="03df1-129"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03df1-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03df1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03df1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03df1-131">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="03df1-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="03df1-132">**\_ \_ Constantes de FORMAT ANSI 381 WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="03df1-132">**WINBIO\_ANSI\_381\_FORMAT Constants**</span></span>](winbio-ansi-381-format-constants.md)
</dt> <dt>

[<span data-ttu-id="03df1-133">**WINBIO \_ BDB \_ ANSI \_ 381 \_ en-tête**</span><span class="sxs-lookup"><span data-stu-id="03df1-133">**WINBIO\_BDB\_ANSI\_381\_HEADER**</span></span>](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[<span data-ttu-id="03df1-134">**\_ \_ en-tête Bir WINBIO**</span><span class="sxs-lookup"><span data-stu-id="03df1-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





