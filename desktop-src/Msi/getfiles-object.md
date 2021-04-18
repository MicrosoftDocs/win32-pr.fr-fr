---
description: L’objet GetFiles récupère les fichiers nécessaires dans une langue particulière du module. Certaines actions doivent être effectuées par le biais de l’objet de fusion avant que toutes les parties de cette interface ne retournent des résultats valides.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Objet GetFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526664"
---
# <a name="getfiles-object"></a><span data-ttu-id="2a4f2-104">GetFiles (objet)</span><span class="sxs-lookup"><span data-stu-id="2a4f2-104">GetFiles object</span></span>

<span data-ttu-id="2a4f2-105">L’objet **GetFiles** récupère les fichiers nécessaires dans une langue particulière du module.</span><span class="sxs-lookup"><span data-stu-id="2a4f2-105">The **GetFiles** object retrieves the files needed in a particular language of the module.</span></span> <span data-ttu-id="2a4f2-106">Certaines actions doivent être effectuées par le biais de l' [objet de fusion](merge-object.md) avant que toutes les parties de cette interface ne retournent des résultats valides.</span><span class="sxs-lookup"><span data-stu-id="2a4f2-106">Requires certain actions be performed through the [Merge object](merge-object.md) before all parts of this interface returns valid results.</span></span>

## <a name="members"></a><span data-ttu-id="2a4f2-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2a4f2-107">Members</span></span>

<span data-ttu-id="2a4f2-108">L’objet **GetFiles** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2a4f2-108">The **GetFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="2a4f2-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2a4f2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a4f2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2a4f2-110">Properties</span></span>

<span data-ttu-id="2a4f2-111">L’objet **GetFiles** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2a4f2-111">The **GetFiles** object has these properties.</span></span>



| <span data-ttu-id="2a4f2-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="2a4f2-112">Property</span></span>                                               | <span data-ttu-id="2a4f2-113">Description</span><span class="sxs-lookup"><span data-stu-id="2a4f2-113">Description</span></span>                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a4f2-114">**ModuleFiles**</span><span class="sxs-lookup"><span data-stu-id="2a4f2-114">**ModuleFiles**</span></span>](getfiles-modulefiles.md)<br/> | <span data-ttu-id="2a4f2-115">La propriété [**ModuleFiles**](getfiles-modulefiles.md) retourne toutes les clés primaires de la [table de fichiers](file-table.md) pour le module actuellement ouvert.</span><span class="sxs-lookup"><span data-stu-id="2a4f2-115">[**ModuleFiles**](getfiles-modulefiles.md) property returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span><br/> |



 

## <a name="c"></a><span data-ttu-id="2a4f2-116">C++</span><span class="sxs-lookup"><span data-stu-id="2a4f2-116">C++</span></span>

<span data-ttu-id="2a4f2-117">interface **IMsmGetFiles : IDispatch**</span><span class="sxs-lookup"><span data-stu-id="2a4f2-117">interface **IMsmGetFiles : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="2a4f2-118">ID d’interface</span><span class="sxs-lookup"><span data-stu-id="2a4f2-118">Interface ID</span></span>



| <span data-ttu-id="2a4f2-119">Constante</span><span class="sxs-lookup"><span data-stu-id="2a4f2-119">Constant</span></span>              | <span data-ttu-id="2a4f2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4f2-120">Value</span></span>                                  |
|-----------------------|----------------------------------------|
| <span data-ttu-id="2a4f2-121">**IID \_ IMsmGetFiles**</span><span class="sxs-lookup"><span data-stu-id="2a4f2-121">**IID\_IMsmGetFiles**</span></span> | <span data-ttu-id="2a4f2-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="2a4f2-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="2a4f2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a4f2-123">Requirements</span></span>



| <span data-ttu-id="2a4f2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a4f2-124">Requirement</span></span> | <span data-ttu-id="2a4f2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a4f2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4f2-126">Version</span><span class="sxs-lookup"><span data-stu-id="2a4f2-126">Version</span></span><br/> | <span data-ttu-id="2a4f2-127">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2a4f2-127">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="2a4f2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a4f2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2a4f2-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a4f2-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a4f2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2a4f2-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a4f2-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a4f2-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




