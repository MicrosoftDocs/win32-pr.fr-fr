---
title: Énumération MrmPlatformVersion (MrmResourceIndexer. h)
description: Définit des constantes qui spécifient une version de plateforme. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 7BA30B8F-FB23-4DCA-930D-099C7F8476E9
keywords:
- Menus de l’énumération MrmPlatformVersion et autres ressources
topic_type:
- apiref
api_name:
- MrmPlatformVersion
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8127d3e6e99d974315327cf89ae9e82add7bc628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942771"
---
# <a name="mrmplatformversion-enumeration"></a><span data-ttu-id="fef6e-105">Énumération MrmPlatformVersion</span><span class="sxs-lookup"><span data-stu-id="fef6e-105">MrmPlatformVersion enumeration</span></span>

<span data-ttu-id="fef6e-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="fef6e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fef6e-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="fef6e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fef6e-108">Définit des constantes qui spécifient une version de plateforme.</span><span class="sxs-lookup"><span data-stu-id="fef6e-108">Defines constants that specify a platform version.</span></span> <span data-ttu-id="fef6e-109">Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="fef6e-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="fef6e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fef6e-110">Syntax</span></span>


```C++
typedef enum _MrmPlatformVersion { 
  MrmPlatformVersion_Default          = 0,
  MrmPlatformVersion_Windows10_0_0_0  = 0x010A0000,
  MrmPlatformVersion_Windows10_0_0_5  = 0x010A0005
} MrmPlatformVersion;
```



## <a name="constants"></a><span data-ttu-id="fef6e-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="fef6e-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fef6e-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="fef6e-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="fef6e-113">Spécifie que la version de la plateforme est la version par défaut.</span><span class="sxs-lookup"><span data-stu-id="fef6e-113">Specifies that the platform version is the default.</span></span>

</dd> <dt>

<span data-ttu-id="fef6e-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion \_ Windows 10 \_ 0 \_ 0 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="fef6e-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion\_Windows10\_0\_0\_0**</span></span>
</dt> <dd>

<span data-ttu-id="fef6e-115">Spécifie une version de plateforme de Windows 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="fef6e-115">Specifies a platform version of Windows 10.0.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="fef6e-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion \_ Windows 10 \_ 0 \_ 0 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="fef6e-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion\_Windows10\_0\_0\_5**</span></span>
</dt> <dd>

<span data-ttu-id="fef6e-117">Spécifie une version de plateforme de Windows 10.0.0.5.</span><span class="sxs-lookup"><span data-stu-id="fef6e-117">Specifies a platform version of Windows 10.0.0.5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fef6e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fef6e-118">Requirements</span></span>



| <span data-ttu-id="fef6e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fef6e-119">Requirement</span></span> | <span data-ttu-id="fef6e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fef6e-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef6e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fef6e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fef6e-122">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fef6e-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fef6e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fef6e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fef6e-124">Applications de \[ Bureau Windows Server uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fef6e-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fef6e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fef6e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fef6e-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fef6e-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef6e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fef6e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef6e-128">API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés</span><span class="sxs-lookup"><span data-stu-id="fef6e-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

