---
title: Structure WINBIO_BSP_SCHEMA ( \_ types WINBIO. h)
description: Décrit les fonctionnalités d’un fournisseur de services biométriques.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BSP_SCHEMA
- API du pointeur de structure PWINBIO_BSP_SCHEMA Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465414"
---
# <a name="winbio_bsp_schema-structure"></a><span data-ttu-id="d290f-105">\_Structure de \_ schéma BSP WINBIO</span><span class="sxs-lookup"><span data-stu-id="d290f-105">WINBIO\_BSP\_SCHEMA structure</span></span>

<span data-ttu-id="d290f-106">La structure de **\_ \_ schéma BSP WINBIO** décrit les fonctionnalités d’un fournisseur de services biométriques.</span><span class="sxs-lookup"><span data-stu-id="d290f-106">The **WINBIO\_BSP\_SCHEMA** structure describes the capabilities of a biometric service provider.</span></span> <span data-ttu-id="d290f-107">Cette structure est utilisée par la fonction [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) .</span><span class="sxs-lookup"><span data-stu-id="d290f-107">This structure is used by the [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d290f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d290f-108">Syntax</span></span>


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="d290f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d290f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d290f-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="d290f-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="d290f-111">Type de mesure biométrique utilisé par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="d290f-111">The type of biometric measurement used by this device.</span></span> <span data-ttu-id="d290f-112">Actuellement, il doit s’agir d’une **\_ \_ empreinte digitale de type WINBIO**.</span><span class="sxs-lookup"><span data-stu-id="d290f-112">Currently this must be **WINBIO\_TYPE\_FINGERPRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="d290f-113">**BspId**</span><span class="sxs-lookup"><span data-stu-id="d290f-113">**BspId**</span></span>
</dt> <dd>

<span data-ttu-id="d290f-114">Valeur qui identifie de façon unique ce composant du fournisseur de services biométriques.</span><span class="sxs-lookup"><span data-stu-id="d290f-114">A value that uniquely identifies this biometric service provider component.</span></span>

</dd> <dt>

<span data-ttu-id="d290f-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="d290f-115">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d290f-116">Chaîne Unicode terminée par le caractère **null** qui contient une description du fournisseur de services biométriques.</span><span class="sxs-lookup"><span data-stu-id="d290f-116">A **NULL**-terminated Unicode string that contains a description of the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="d290f-117">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="d290f-117">**Vendor**</span></span>
</dt> <dd>

<span data-ttu-id="d290f-118">Chaîne Unicode terminée par le caractère **null** qui contient le nom du fournisseur qui fournit le fournisseur de services biométriques.</span><span class="sxs-lookup"><span data-stu-id="d290f-118">A **NULL**-terminated Unicode string that contains the name of the vendor supplying the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="d290f-119">**Version**</span><span class="sxs-lookup"><span data-stu-id="d290f-119">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="d290f-120">Une structure de [**\_ version WINBIO**](winbio-version.md) contient la version logicielle du composant du fournisseur de services biométriques.</span><span class="sxs-lookup"><span data-stu-id="d290f-120">A [**WINBIO\_VERSION**](winbio-version.md) structure the contains the software version of the biometric service provider component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d290f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d290f-121">Requirements</span></span>



| <span data-ttu-id="d290f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d290f-122">Requirement</span></span> | <span data-ttu-id="d290f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d290f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d290f-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d290f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d290f-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d290f-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="d290f-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d290f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d290f-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d290f-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d290f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d290f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d290f-129"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d290f-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d290f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d290f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d290f-131">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="d290f-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="d290f-132">**WinBioEnumServiceProviders**</span><span class="sxs-lookup"><span data-stu-id="d290f-132">**WinBioEnumServiceProviders**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





