---
title: Structure WMDRM_LICENSE_FILTER (wmdrmsdk. h)
description: La \_ \_ structure de filtre de licence WMDRM définit les paramètres de filtrage à utiliser lors de la création d’une énumération de licence.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- Structure WMDRM_LICENSE_FILTER format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539211"
---
# <a name="wmdrm_license_filter-structure"></a><span data-ttu-id="45fb9-105">Structure de filtre de \_ licence WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="45fb9-105">WMDRM\_LICENSE\_FILTER structure</span></span>

<span data-ttu-id="45fb9-106">La structure de **\_ \_ filtre de licence WMDRM** définit les paramètres de filtrage à utiliser lors de la création d’une énumération de licence.</span><span class="sxs-lookup"><span data-stu-id="45fb9-106">The **WMDRM\_LICENSE\_FILTER** structure defines filtering parameters for use when creating a license enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="45fb9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45fb9-107">Syntax</span></span>


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a><span data-ttu-id="45fb9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="45fb9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="45fb9-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="45fb9-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="45fb9-110">Spécifie un numéro de version minimal pour les licences retournées.</span><span class="sxs-lookup"><span data-stu-id="45fb9-110">Specifies a minimum version number for the returned licenses.</span></span>

</dd> <dt>

<span data-ttu-id="45fb9-111">**bstrKID**</span><span class="sxs-lookup"><span data-stu-id="45fb9-111">**bstrKID**</span></span>
</dt> <dd>

<span data-ttu-id="45fb9-112">Spécifie un ID de clé pour lequel filtrer les licences.</span><span class="sxs-lookup"><span data-stu-id="45fb9-112">Specifies a key ID to filter licenses for.</span></span> <span data-ttu-id="45fb9-113">Seules les licences avec l’ID de clé spécifié seront incluses dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="45fb9-113">Only licenses with the specified key ID will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="45fb9-114">**bstrRights**</span><span class="sxs-lookup"><span data-stu-id="45fb9-114">**bstrRights**</span></span>
</dt> <dd>

<span data-ttu-id="45fb9-115">Spécifie un ensemble de droits pour le filtrage des licences.</span><span class="sxs-lookup"><span data-stu-id="45fb9-115">Specifies a set of rights to filter licenses for.</span></span> <span data-ttu-id="45fb9-116">Seules les licences qui fournissent tous les droits spécifiés seront incluses dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="45fb9-116">Only licenses that provide all of the specified rights will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="45fb9-117">**bstrAllowedSourceIDs**</span><span class="sxs-lookup"><span data-stu-id="45fb9-117">**bstrAllowedSourceIDs**</span></span>
</dt> <dd>

<span data-ttu-id="45fb9-118">Spécifie les sources de contenu protégé à inclure dans la recherche de licence.</span><span class="sxs-lookup"><span data-stu-id="45fb9-118">Specifies the sources of protected content to include in the license search.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45fb9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="45fb9-119">Remarks</span></span>

<span data-ttu-id="45fb9-120">Cette structure est utilisée par la méthode [**IWMDRMLicenseManagement :: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="45fb9-120">This structure is used by the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="45fb9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45fb9-121">Requirements</span></span>



| <span data-ttu-id="45fb9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45fb9-122">Requirement</span></span> | <span data-ttu-id="45fb9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="45fb9-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45fb9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="45fb9-124">Header</span></span><br/> | <dl> <span data-ttu-id="45fb9-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="45fb9-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45fb9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45fb9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45fb9-127">**Structures**</span><span class="sxs-lookup"><span data-stu-id="45fb9-127">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





