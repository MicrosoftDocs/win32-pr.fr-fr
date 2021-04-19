---
description: L’objet de dépendance retourne un module dont dépend le module en cours et qui n’a pas encore été fusionné dans la base de données d’installation actuelle.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Objet de dépendance (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528751"
---
# <a name="dependency-object"></a><span data-ttu-id="2ba34-103">Objet de dépendance</span><span class="sxs-lookup"><span data-stu-id="2ba34-103">Dependency object</span></span>

<span data-ttu-id="2ba34-104">L’objet de **dépendance** retourne un module dont dépend le module en cours et qui n’a pas encore été fusionné dans la base de données d’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="2ba34-104">The **Dependency** object returns a module that the current module is dependent upon and which has not yet been merged into the current installation database.</span></span>

## <a name="members"></a><span data-ttu-id="2ba34-105">Membres</span><span class="sxs-lookup"><span data-stu-id="2ba34-105">Members</span></span>

<span data-ttu-id="2ba34-106">L’objet de **dépendance** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2ba34-106">The **Dependency** object has these types of members:</span></span>

-   [<span data-ttu-id="2ba34-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2ba34-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ba34-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2ba34-108">Properties</span></span>

<span data-ttu-id="2ba34-109">L’objet de **dépendance** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2ba34-109">The **Dependency** object has these properties.</span></span>



| <span data-ttu-id="2ba34-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="2ba34-110">Property</span></span>                                           | <span data-ttu-id="2ba34-111">Description</span><span class="sxs-lookup"><span data-stu-id="2ba34-111">Description</span></span>                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="2ba34-112">**Language**</span><span class="sxs-lookup"><span data-stu-id="2ba34-112">**Language**</span></span>](dependency-language.md)<br/> | <span data-ttu-id="2ba34-113">Retourne la langue du module.</span><span class="sxs-lookup"><span data-stu-id="2ba34-113">Return the language of the module.</span></span><br/>           |
| [<span data-ttu-id="2ba34-114">**Module**</span><span class="sxs-lookup"><span data-stu-id="2ba34-114">**Module**</span></span>](dependency-module.md)<br/>     | <span data-ttu-id="2ba34-115">Retourne l’ID du module requis.</span><span class="sxs-lookup"><span data-stu-id="2ba34-115">Return the module ID of the required module.</span></span><br/> |
| [<span data-ttu-id="2ba34-116">**Version**</span><span class="sxs-lookup"><span data-stu-id="2ba34-116">**Version**</span></span>](dependency-version.md)<br/>   | <span data-ttu-id="2ba34-117">Retourne la version du module requis.</span><span class="sxs-lookup"><span data-stu-id="2ba34-117">Return the version of the required module.</span></span><br/>   |



 

## <a name="c"></a><span data-ttu-id="2ba34-118">C++</span><span class="sxs-lookup"><span data-stu-id="2ba34-118">C++</span></span>

<span data-ttu-id="2ba34-119">interface **IMsmDependency : IDispatch**</span><span class="sxs-lookup"><span data-stu-id="2ba34-119">interface **IMsmDependency : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="2ba34-120">ID d’interface</span><span class="sxs-lookup"><span data-stu-id="2ba34-120">Interface ID</span></span>



| <span data-ttu-id="2ba34-121">Constante</span><span class="sxs-lookup"><span data-stu-id="2ba34-121">Constant</span></span>                | <span data-ttu-id="2ba34-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ba34-122">Value</span></span>                                  |
|-------------------------|----------------------------------------|
| <span data-ttu-id="2ba34-123">**IID \_ IMsmDependency**</span><span class="sxs-lookup"><span data-stu-id="2ba34-123">**IID\_IMsmDependency**</span></span> | <span data-ttu-id="2ba34-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="2ba34-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="2ba34-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ba34-125">Requirements</span></span>



| <span data-ttu-id="2ba34-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ba34-126">Requirement</span></span> | <span data-ttu-id="2ba34-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ba34-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba34-128">Version</span><span class="sxs-lookup"><span data-stu-id="2ba34-128">Version</span></span><br/> | <span data-ttu-id="2ba34-129">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2ba34-129">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="2ba34-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ba34-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2ba34-131"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ba34-131"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ba34-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2ba34-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="2ba34-133"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ba34-133"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




