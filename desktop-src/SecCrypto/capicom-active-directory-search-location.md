---
description: Indique l’emplacement où rechercher un magasin de certificats Active Directory.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Énumération CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528675"
---
# <a name="capicom_active_directory_search_location-enumeration"></a><span data-ttu-id="8894e-103">\_Énumération de l' \_ \_ emplacement de recherche Active Directory \_ CAPICOM</span><span class="sxs-lookup"><span data-stu-id="8894e-103">CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION enumeration</span></span>

<span data-ttu-id="8894e-104">Le type d’énumération de l' **emplacement de \_ recherche d’active \_ Directory \_ \_ CAPICOM** indique l’emplacement dans lequel Rechercher un [*magasin de certificats*](../secgloss/c-gly.md)Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8894e-104">The **CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION** enumeration type indicates the location to be searched for an Active Directory [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="8894e-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8894e-105">Members</span></span>



| <span data-ttu-id="8894e-106">Membre</span><span class="sxs-lookup"><span data-stu-id="8894e-106">Member</span></span>                               | <span data-ttu-id="8894e-107">Description</span><span class="sxs-lookup"><span data-stu-id="8894e-107">Description</span></span>                                  | <span data-ttu-id="8894e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8894e-108">Value</span></span> |
|--------------------------------------|----------------------------------------------|-------|
| <span data-ttu-id="8894e-109">**Rechercher dans CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8894e-109">**CAPICOM\_SEARCH\_ANY**</span></span>             | <span data-ttu-id="8894e-110">Effectue une recherche dans tous les emplacements disponibles.</span><span class="sxs-lookup"><span data-stu-id="8894e-110">Searches all available locations.</span></span><br/> | <span data-ttu-id="8894e-111">0</span><span class="sxs-lookup"><span data-stu-id="8894e-111">0</span></span>     |
| <span data-ttu-id="8894e-112">**\_catalogue global de recherche \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="8894e-112">**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</span></span> | <span data-ttu-id="8894e-113">Recherche uniquement dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="8894e-113">Searches only the global catalog.</span></span><br/> | <span data-ttu-id="8894e-114">1</span><span class="sxs-lookup"><span data-stu-id="8894e-114">1</span></span>     |
| <span data-ttu-id="8894e-115">**\_ \_ domaine par défaut de recherche \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="8894e-115">**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</span></span> | <span data-ttu-id="8894e-116">Recherche uniquement le domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="8894e-116">Searches only the default domain.</span></span><br/> | <span data-ttu-id="8894e-117">2</span><span class="sxs-lookup"><span data-stu-id="8894e-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="8894e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8894e-118">Remarks</span></span>

<span data-ttu-id="8894e-119">Ce type d’énumération est utilisé par la propriété suivante :</span><span class="sxs-lookup"><span data-stu-id="8894e-119">This enumeration type is used by the following property:</span></span>

-   [<span data-ttu-id="8894e-120">**Paramètres. ActiveDirectorySearchLocation**</span><span class="sxs-lookup"><span data-stu-id="8894e-120">**Settings.ActiveDirectorySearchLocation**</span></span>](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a><span data-ttu-id="8894e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8894e-121">Requirements</span></span>



| <span data-ttu-id="8894e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8894e-122">Requirement</span></span> | <span data-ttu-id="8894e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8894e-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8894e-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8894e-124">Redistributable</span></span><br/> | <span data-ttu-id="8894e-125">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="8894e-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="8894e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8894e-126">Header</span></span><br/>          | <dl> <span data-ttu-id="8894e-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="8894e-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 
