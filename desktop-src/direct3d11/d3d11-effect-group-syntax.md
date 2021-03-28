---
title: Syntaxe des groupes d’effets (Direct3D 11)
description: Un groupe d’effets est déclaré avec la syntaxe décrite dans cette section.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104462610"
---
# <a name="effect-group-syntax-direct3d-11"></a><span data-ttu-id="77457-103">Syntaxe des groupes d’effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="77457-103">Effect Group Syntax (Direct3D 11)</span></span>

<span data-ttu-id="77457-104">Un groupe d’effets est déclaré avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="77457-104">An effect group is declared with the syntax described in this section.</span></span>


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a><span data-ttu-id="77457-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77457-105">Parameters</span></span>



| <span data-ttu-id="77457-106">Élément</span><span class="sxs-lookup"><span data-stu-id="77457-106">Item</span></span>                                                                                                                                                                           | <span data-ttu-id="77457-107">Description</span><span class="sxs-lookup"><span data-stu-id="77457-107">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77457-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span><span class="sxs-lookup"><span data-stu-id="77457-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span></span><br/>                                                                                                         | <span data-ttu-id="77457-109">mot clé equises.</span><span class="sxs-lookup"><span data-stu-id="77457-109">equired keyword.</span></span><br/>                                                                                                                                                                                                         |
| <span data-ttu-id="77457-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span><span class="sxs-lookup"><span data-stu-id="77457-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span></span><br/>                                                                       | <span data-ttu-id="77457-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="77457-111">Required.</span></span> <span data-ttu-id="77457-112">Chaîne ASCII qui identifie de façon unique le nom du groupe d’effets.</span><span class="sxs-lookup"><span data-stu-id="77457-112">An ASCII string that uniquely identifies the name of the effect group.</span></span> <span data-ttu-id="77457-113">Contrairement aux techniques, les groupes doivent avoir des noms pour s’assurer que les techniques ont un identificateur unique (voir la section groupes et techniques ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="77457-113">Unlike techniques, groups must have names to ensure that techniques have a unique identifier (see Groups and Techniques section below).</span></span><br/> |
| <span data-ttu-id="77457-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> Annotations de < ></span><span class="sxs-lookup"><span data-stu-id="77457-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Annotations ></span></span><br/> | <span data-ttu-id="77457-115">\[\]facultatif.</span><span class="sxs-lookup"><span data-stu-id="77457-115">\[in\] Optional.</span></span> <span data-ttu-id="77457-116">Un ou plusieurs éléments d’informations fournies par l’utilisateur (métadonnées) qui sont ignorés par le système d’effet.</span><span class="sxs-lookup"><span data-stu-id="77457-116">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="77457-117">Pour obtenir la syntaxe, consultez syntaxe d’annotation (Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="77457-117">For syntax, see Annotation Syntax (Direct3D 11).</span></span> <br/>                                                      |
| <span data-ttu-id="77457-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="77457-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/>                                           | <span data-ttu-id="77457-119">« Technique10 » ou « technique11 ».</span><span class="sxs-lookup"><span data-stu-id="77457-119">Either "technique10" or "technique11".</span></span> <span data-ttu-id="77457-120">Les techniques qui utilisent les nouvelles fonctionnalités de Direct3D 11 (5 \_ nuanceurs, BindInterfaces, etc.) doivent utiliser « technique11 ».</span><span class="sxs-lookup"><span data-stu-id="77457-120">Techniques which use functionality new to Direct3D 11 (5\_0 shaders, BindInterfaces, etc) must use "technique11".</span></span><br/>                                                                 |
| <span data-ttu-id="77457-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span><span class="sxs-lookup"><span data-stu-id="77457-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span></span><br/>                                                       | <span data-ttu-id="77457-122">facultatif.</span><span class="sxs-lookup"><span data-stu-id="77457-122">Optional.</span></span> <span data-ttu-id="77457-123">Chaîne ASCII qui identifie de façon unique le nom de la technique d’effet.</span><span class="sxs-lookup"><span data-stu-id="77457-123">An ASCII string that uniquely identifies the name of the effect technique.</span></span> <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a><span data-ttu-id="77457-124">Groupes et techniques</span><span class="sxs-lookup"><span data-stu-id="77457-124">Groups and Techniques</span></span>

<span data-ttu-id="77457-125">Pour assurer la compatibilité avec les \_ effets FX 4 \_ 0, les groupes sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="77457-125">In order to maintain compatibility with fx\_4\_0 effects, groups are optional.</span></span> <span data-ttu-id="77457-126">Il existe un groupe implicite nommé NULL entourant toutes les techniques globales.</span><span class="sxs-lookup"><span data-stu-id="77457-126">There is an implicit NULL-named group surrounding all global techniques.</span></span>

<span data-ttu-id="77457-127">Prenons l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="77457-127">Consider the following example:</span></span>


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



<span data-ttu-id="77457-128">En C++, il est possible d’obtenir une technique par nom de deux manières.</span><span class="sxs-lookup"><span data-stu-id="77457-128">In C++, one can get a technique by name in two ways.</span></span> <span data-ttu-id="77457-129">Les commandes suivantes permettent de trouver les techniques évidentes :</span><span class="sxs-lookup"><span data-stu-id="77457-129">The following commands will find the obvious techniques:</span></span>


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



<span data-ttu-id="77457-130">Pour vous assurer que [**ID3DX11Effect :: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) fonctionne de la même façon que les effets 10, tous les groupes définis doivent avoir un nom.</span><span class="sxs-lookup"><span data-stu-id="77457-130">In order to ensure that [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) works similarly to Effects 10, all defined groups must have a name.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77457-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77457-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77457-132">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="77457-132">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="77457-133">Syntaxe d’effet technique (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="77457-133">Effect Technique Syntax (Direct3D 11)</span></span>](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





