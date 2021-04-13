---
title: Énumération MrmDumpType (MrmResourceIndexer. h)
description: Définit des constantes qui spécifient le type de vidage de fichier PRI à produire. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 71E49F35-4B79-478A-A26A-C0D9A9FC2D11
keywords:
- Menus de l’énumération MrmDumpType et autres ressources
topic_type:
- apiref
api_name:
- MrmDumpType
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff693f933af299d042b97de319fb221ac133a5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465598"
---
# <a name="mrmdumptype-enumeration"></a><span data-ttu-id="b1def-105">Énumération MrmDumpType</span><span class="sxs-lookup"><span data-stu-id="b1def-105">MrmDumpType enumeration</span></span>

<span data-ttu-id="b1def-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b1def-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b1def-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b1def-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b1def-108">Définit des constantes qui spécifient le type de vidage de fichier PRI à produire.</span><span class="sxs-lookup"><span data-stu-id="b1def-108">Defines constants that specify the type of PRI file dump to produce.</span></span> <span data-ttu-id="b1def-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="b1def-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1def-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1def-110">Syntax</span></span>


```C++
typedef enum _MrmDumpType { 
  MrmDumpType_Basic     = 0,
  MrmDumpType_Detailed  = 1,
  MrmDumpType_Schema    = 2
} MrmDumpType;
```



## <a name="constants"></a><span data-ttu-id="b1def-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="b1def-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b1def-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType de \_ base**</span><span class="sxs-lookup"><span data-stu-id="b1def-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType\_Basic**</span></span>
</dt> <dd>

<span data-ttu-id="b1def-113">Spécifie que le vidage doit être de base.</span><span class="sxs-lookup"><span data-stu-id="b1def-113">Specifies that the dump should be basic.</span></span>

</dd> <dt>

<span data-ttu-id="b1def-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType \_ détaillé**</span><span class="sxs-lookup"><span data-stu-id="b1def-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType\_Detailed**</span></span>
</dt> <dd>

<span data-ttu-id="b1def-115">Spécifie que le vidage doit être détaillé.</span><span class="sxs-lookup"><span data-stu-id="b1def-115">Specifies that the dump should be detailed.</span></span>

</dd> <dt>

<span data-ttu-id="b1def-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**\_Schéma MrmDumpType**</span><span class="sxs-lookup"><span data-stu-id="b1def-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**MrmDumpType\_Schema**</span></span>
</dt> <dd>

<span data-ttu-id="b1def-117">Spécifie que le vidage doit être un schéma.</span><span class="sxs-lookup"><span data-stu-id="b1def-117">Specifies that the dump should be a schema.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1def-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1def-118">Requirements</span></span>



| <span data-ttu-id="b1def-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1def-119">Requirement</span></span> | <span data-ttu-id="b1def-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1def-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1def-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1def-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b1def-122">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1def-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b1def-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1def-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b1def-124">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1def-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1def-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1def-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1def-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1def-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1def-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1def-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1def-128">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="b1def-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

