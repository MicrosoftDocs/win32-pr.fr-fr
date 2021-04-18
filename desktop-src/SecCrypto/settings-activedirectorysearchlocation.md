---
description: Définit ou récupère le Active Directory emplacement de recherche.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Propriété Settings. ActiveDirectorySearchLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526738"
---
# <a name="settingsactivedirectorysearchlocation-property"></a><span data-ttu-id="c7088-103">Propriété Settings. ActiveDirectorySearchLocation</span><span class="sxs-lookup"><span data-stu-id="c7088-103">Settings.ActiveDirectorySearchLocation property</span></span>

<span data-ttu-id="c7088-104">\[La propriété **ActiveDirectorySearchLocation** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.\]</span><span class="sxs-lookup"><span data-stu-id="c7088-104">\[The **ActiveDirectorySearchLocation** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="c7088-105">La propriété **ActiveDirectorySearchLocation** définit ou récupère le Active Directory emplacement de recherche.</span><span class="sxs-lookup"><span data-stu-id="c7088-105">The **ActiveDirectorySearchLocation** property sets or retrieves the Active Directory search location.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7088-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7088-106">Syntax</span></span>


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="c7088-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c7088-107">Property value</span></span>

<span data-ttu-id="c7088-108">Valeur de l’énumération de l' [**\_ emplacement de \_ \_ recherche \_ Active Directory CAPICOM**](capicom-active-directory-search-location.md) qui spécifie l’emplacement de recherche.</span><span class="sxs-lookup"><span data-stu-id="c7088-108">A value of the [**CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION**](capicom-active-directory-search-location.md) enumeration that specifies the search location.</span></span> <span data-ttu-id="c7088-109">La valeur par défaut est la \_ recherche CAPICOM \_ .</span><span class="sxs-lookup"><span data-stu-id="c7088-109">The default value is CAPICOM\_SEARCH\_ANY.</span></span> <span data-ttu-id="c7088-110">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="c7088-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="c7088-111">Value</span><span class="sxs-lookup"><span data-stu-id="c7088-111">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="c7088-112">Signification</span><span class="sxs-lookup"><span data-stu-id="c7088-112">Meaning</span></span>                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <span data-ttu-id="c7088-113"><dt>**Rechercher dans CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7088-113"><dt>**CAPICOM\_SEARCH\_ANY**</dt></span></span> </dl>                                   | <span data-ttu-id="c7088-114">Recherchez tous les emplacements disponibles.</span><span class="sxs-lookup"><span data-stu-id="c7088-114">Search all available locations.</span></span><br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <span data-ttu-id="c7088-115"><dt>**\_ \_ domaine par défaut de recherche \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="c7088-115"><dt>**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="c7088-116">Recherche uniquement dans le domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="c7088-116">Search only the default domain.</span></span><br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <span data-ttu-id="c7088-117"><dt>**\_catalogue global de recherche \_ CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7088-117"><dt>**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</dt></span></span> </dl> | <span data-ttu-id="c7088-118">Recherche uniquement dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="c7088-118">Search only the global catalog.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c7088-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7088-119">Requirements</span></span>



| <span data-ttu-id="c7088-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7088-120">Requirement</span></span> | <span data-ttu-id="c7088-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7088-121">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7088-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c7088-122">Redistributable</span></span><br/> | <span data-ttu-id="c7088-123">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7088-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c7088-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c7088-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="c7088-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7088-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7088-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7088-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7088-127">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="c7088-127">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




