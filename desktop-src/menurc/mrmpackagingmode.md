---
title: Énumération MrmPackagingMode (MrmResourceIndexer. h)
description: Définit des constantes qui spécifient le type de fichier PRI à créer par MrmCreateResourceFile et MrmCreateResourceFileInMemory.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Menus de l’énumération MrmPackagingMode et autres ressources
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317273"
---
# <a name="mrmpackagingmode-enumeration"></a><span data-ttu-id="46541-104">Énumération MrmPackagingMode</span><span class="sxs-lookup"><span data-stu-id="46541-104">MrmPackagingMode enumeration</span></span>

<span data-ttu-id="46541-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="46541-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="46541-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="46541-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="46541-107">Définit des constantes qui spécifient le type de fichier PRI à créer par [**MrmCreateResourceFile**](mrmcreateresourcefile.md) et [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="46541-107">Defines constants that specify what kind of PRI file(s) should be created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="46541-108">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="46541-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="46541-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46541-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a><span data-ttu-id="46541-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="46541-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="46541-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span><span class="sxs-lookup"><span data-stu-id="46541-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span></span>
</dt> <dd>

<span data-ttu-id="46541-112">Spécifie qu’un seul fichier PRI doit être créé.</span><span class="sxs-lookup"><span data-stu-id="46541-112">Specifies that a single PRI file should be created.</span></span>

</dd> <dt>

<span data-ttu-id="46541-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span><span class="sxs-lookup"><span data-stu-id="46541-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span></span>
</dt> <dd>

<span data-ttu-id="46541-114">Spécifie que plusieurs fichiers PRI doivent être créés. fractionner automatiquement par tous les qualificateurs pris en charge (plus précisément, langage et échelle).</span><span class="sxs-lookup"><span data-stu-id="46541-114">Specifies that multiple PRI files should be created; split automatically by all supported qualifiers (specifically, language and scale).</span></span>

</dd> <dt>

<span data-ttu-id="46541-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span><span class="sxs-lookup"><span data-stu-id="46541-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span></span>
</dt> <dd>

<span data-ttu-id="46541-116">Spécifie qu’un fichier PRI satellite de module complémentaire doit être créé.</span><span class="sxs-lookup"><span data-stu-id="46541-116">Specifies that an add-on satellite PRI file should be created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46541-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46541-117">Requirements</span></span>



| <span data-ttu-id="46541-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46541-118">Requirement</span></span> | <span data-ttu-id="46541-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="46541-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46541-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46541-120">Minimum supported client</span></span><br/> | <span data-ttu-id="46541-121">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46541-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="46541-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46541-122">Minimum supported server</span></span><br/> | <span data-ttu-id="46541-123">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46541-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="46541-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="46541-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="46541-125"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="46541-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46541-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46541-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46541-127">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="46541-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

