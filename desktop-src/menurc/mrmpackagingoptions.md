---
title: Énumération MrmPackagingOptions (MrmResourceIndexer. h)
description: Définit des constantes qui spécifient des options pour le fichier PRI créé par MrmCreateResourceFile et MrmCreateResourceFileInMemory.
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- Menus de l’énumération MrmPackagingOptions et autres ressources
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a8b2bee733fe17e91501fe295e5f80be159ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509506"
---
# <a name="mrmpackagingoptions-enumeration"></a><span data-ttu-id="535ea-104">Énumération MrmPackagingOptions</span><span class="sxs-lookup"><span data-stu-id="535ea-104">MrmPackagingOptions enumeration</span></span>

<span data-ttu-id="535ea-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="535ea-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="535ea-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="535ea-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="535ea-107">Définit des constantes qui spécifient des options pour le fichier PRI créé par [**MrmCreateResourceFile**](mrmcreateresourcefile.md) et [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="535ea-107">Defines constants that specify options for the PRI file created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="535ea-108">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="535ea-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="535ea-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="535ea-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a><span data-ttu-id="535ea-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="535ea-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="535ea-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span><span class="sxs-lookup"><span data-stu-id="535ea-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span></span>
</dt> <dd>

<span data-ttu-id="535ea-112">Ne spécifie aucune option de Packaging.</span><span class="sxs-lookup"><span data-stu-id="535ea-112">Specifies no packaging options.</span></span>

</dd> <dt>

<span data-ttu-id="535ea-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span><span class="sxs-lookup"><span data-stu-id="535ea-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span></span>
</dt> <dd>

<span data-ttu-id="535ea-114">Spécifie qu’un pack de ressources sans schéma doit être créé.</span><span class="sxs-lookup"><span data-stu-id="535ea-114">Specifies that a schema-free resource pack should be created.</span></span>

</dd> <dt>

<span data-ttu-id="535ea-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span><span class="sxs-lookup"><span data-stu-id="535ea-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span></span>
</dt> <dd>

<span data-ttu-id="535ea-116">Spécifie que le fichier PRI doit être automatiquement divisé par tous les qualificateurs pris en charge (plus précisément, langue et échelle).</span><span class="sxs-lookup"><span data-stu-id="535ea-116">Specifies that the PRI file should be automatically split by all supported qualifiers (specifically, language and scale).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="535ea-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="535ea-117">Requirements</span></span>



| <span data-ttu-id="535ea-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="535ea-118">Requirement</span></span> | <span data-ttu-id="535ea-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="535ea-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="535ea-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="535ea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="535ea-121">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="535ea-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="535ea-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="535ea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="535ea-123">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="535ea-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="535ea-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="535ea-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="535ea-125"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="535ea-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="535ea-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="535ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="535ea-127">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="535ea-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

