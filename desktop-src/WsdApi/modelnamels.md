---
description: Spécifie une version localisée du nom de l’appareil.
ms.assetid: 67ebbca0-bdb2-4a6e-98d8-3d8d1029884f
title: élément modelNameLS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e71be6ee3a2e1104858c0f51a4ff68a5cf8cb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534192"
---
# <a name="modelnamels-element"></a><span data-ttu-id="1d2bb-103">élément modelNameLS</span><span class="sxs-lookup"><span data-stu-id="1d2bb-103">modelNameLS element</span></span>

<span data-ttu-id="1d2bb-104">Spécifie une version localisée du nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d2bb-104">Specifies a localized version of the device name.</span></span>

## <a name="usage"></a><span data-ttu-id="1d2bb-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="1d2bb-105">Usage</span></span>

``` syntax
<modelNameLS
  Language = "language identifier string"
  Data = "localized model name string"/>
```

## <a name="attributes"></a><span data-ttu-id="1d2bb-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="1d2bb-106">Attributes</span></span>



| <span data-ttu-id="1d2bb-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="1d2bb-107">Attribute</span></span>               | <span data-ttu-id="1d2bb-108">Type</span><span class="sxs-lookup"><span data-stu-id="1d2bb-108">Type</span></span>                                   | <span data-ttu-id="1d2bb-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1d2bb-109">Required</span></span>       | <span data-ttu-id="1d2bb-110">Description</span><span class="sxs-lookup"><span data-stu-id="1d2bb-110">Description</span></span>                                                      |
|-------------------------|----------------------------------------|----------------|------------------------------------------------------------------|
| <span data-ttu-id="1d2bb-111">**Données**</span><span class="sxs-lookup"><span data-stu-id="1d2bb-111">**Data**</span></span><br/>     | <span data-ttu-id="1d2bb-112">chaîne de nom de modèle localisée</span><span class="sxs-lookup"><span data-stu-id="1d2bb-112">localized model name string</span></span><br/> | <span data-ttu-id="1d2bb-113">Oui</span><span class="sxs-lookup"><span data-stu-id="1d2bb-113">Yes</span></span><br/> | <span data-ttu-id="1d2bb-114">Nom de modèle localisé.</span><span class="sxs-lookup"><span data-stu-id="1d2bb-114">The localized model name.</span></span><br/> <br/>                 |
| <span data-ttu-id="1d2bb-115">**Langage**</span><span class="sxs-lookup"><span data-stu-id="1d2bb-115">**Language**</span></span><br/> | <span data-ttu-id="1d2bb-116">chaîne d’identificateur de langue</span><span class="sxs-lookup"><span data-stu-id="1d2bb-116">language identifier string</span></span><br/>  | <span data-ttu-id="1d2bb-117">Oui</span><span class="sxs-lookup"><span data-stu-id="1d2bb-117">Yes</span></span><br/> | <span data-ttu-id="1d2bb-118">Langue du nom de modèle localisé.</span><span class="sxs-lookup"><span data-stu-id="1d2bb-118">The language of the localized model name.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="1d2bb-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1d2bb-119">Child elements</span></span>

<span data-ttu-id="1d2bb-120">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="1d2bb-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1d2bb-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1d2bb-121">Parent elements</span></span>



| <span data-ttu-id="1d2bb-122">Élément</span><span class="sxs-lookup"><span data-stu-id="1d2bb-122">Element</span></span>                                                   | <span data-ttu-id="1d2bb-123">Description</span><span class="sxs-lookup"><span data-stu-id="1d2bb-123">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d2bb-124">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="1d2bb-124">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="1d2bb-125">Définit les métadonnées du fabricant et du modèle pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="1d2bb-125">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="1d2bb-126">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="1d2bb-126">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="1d2bb-127">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d2bb-127">Minimum supported system</span></span><br/> | <span data-ttu-id="1d2bb-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d2bb-128">Windows Vista</span></span> |
| <span data-ttu-id="1d2bb-129">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="1d2bb-129">Can be empty</span></span>                        | <span data-ttu-id="1d2bb-130">Oui</span><span class="sxs-lookup"><span data-stu-id="1d2bb-130">Yes</span></span>           |



 

 




