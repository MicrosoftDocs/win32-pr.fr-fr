---
description: Spécifie une version localisée du nom de l’appareil.
ms.assetid: 67ebbca0-bdb2-4a6e-98d8-3d8d1029884f
title: élément modelNameLS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47d2f83d1b636efc30e98dff8c46600bcee555d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995496"
---
# <a name="modelnamels-element"></a><span data-ttu-id="d99fc-103">élément modelNameLS</span><span class="sxs-lookup"><span data-stu-id="d99fc-103">modelNameLS element</span></span>

<span data-ttu-id="d99fc-104">Spécifie une version localisée du nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d99fc-104">Specifies a localized version of the device name.</span></span>

## <a name="usage"></a><span data-ttu-id="d99fc-105">Usage</span><span class="sxs-lookup"><span data-stu-id="d99fc-105">Usage</span></span>

``` syntax
<modelNameLS
  Language = "language identifier string"
  Data = "localized model name string"/>
```

## <a name="attributes"></a><span data-ttu-id="d99fc-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="d99fc-106">Attributes</span></span>



| <span data-ttu-id="d99fc-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="d99fc-107">Attribute</span></span>               | <span data-ttu-id="d99fc-108">Type</span><span class="sxs-lookup"><span data-stu-id="d99fc-108">Type</span></span>                                   | <span data-ttu-id="d99fc-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d99fc-109">Required</span></span>       | <span data-ttu-id="d99fc-110">Description</span><span class="sxs-lookup"><span data-stu-id="d99fc-110">Description</span></span>                                                      |
|-------------------------|----------------------------------------|----------------|------------------------------------------------------------------|
| <span data-ttu-id="d99fc-111">**Données**</span><span class="sxs-lookup"><span data-stu-id="d99fc-111">**Data**</span></span><br/>     | <span data-ttu-id="d99fc-112">chaîne de nom de modèle localisée</span><span class="sxs-lookup"><span data-stu-id="d99fc-112">localized model name string</span></span><br/> | <span data-ttu-id="d99fc-113">Oui</span><span class="sxs-lookup"><span data-stu-id="d99fc-113">Yes</span></span><br/> | <span data-ttu-id="d99fc-114">Nom de modèle localisé.</span><span class="sxs-lookup"><span data-stu-id="d99fc-114">The localized model name.</span></span><br/> <br/>                 |
| <span data-ttu-id="d99fc-115">**Language**</span><span class="sxs-lookup"><span data-stu-id="d99fc-115">**Language**</span></span><br/> | <span data-ttu-id="d99fc-116">chaîne d’identificateur de langue</span><span class="sxs-lookup"><span data-stu-id="d99fc-116">language identifier string</span></span><br/>  | <span data-ttu-id="d99fc-117">Oui</span><span class="sxs-lookup"><span data-stu-id="d99fc-117">Yes</span></span><br/> | <span data-ttu-id="d99fc-118">Langue du nom de modèle localisé.</span><span class="sxs-lookup"><span data-stu-id="d99fc-118">The language of the localized model name.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="d99fc-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d99fc-119">Child elements</span></span>

<span data-ttu-id="d99fc-120">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="d99fc-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d99fc-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d99fc-121">Parent elements</span></span>



| <span data-ttu-id="d99fc-122">Élément</span><span class="sxs-lookup"><span data-stu-id="d99fc-122">Element</span></span>                                                   | <span data-ttu-id="d99fc-123">Description</span><span class="sxs-lookup"><span data-stu-id="d99fc-123">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d99fc-124">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="d99fc-124">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="d99fc-125">Définit les métadonnées du fabricant et du modèle pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="d99fc-125">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="d99fc-126">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d99fc-126">Element information</span></span>



| <span data-ttu-id="d99fc-127">Étiquette</span><span class="sxs-lookup"><span data-stu-id="d99fc-127">Label</span></span> | <span data-ttu-id="d99fc-128">Value</span><span class="sxs-lookup"><span data-stu-id="d99fc-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="d99fc-129">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d99fc-129">Minimum supported system</span></span><br/> | <span data-ttu-id="d99fc-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d99fc-130">Windows Vista</span></span> |
| <span data-ttu-id="d99fc-131">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="d99fc-131">Can be empty</span></span>                        | <span data-ttu-id="d99fc-132">Oui</span><span class="sxs-lookup"><span data-stu-id="d99fc-132">Yes</span></span>           |



 

 




