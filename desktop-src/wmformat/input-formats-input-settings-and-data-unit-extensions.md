---
title: Formats d’entrée, paramètres d’entrée et extensions d’unité de données
description: Formats d’entrée, paramètres d’entrée et extensions d’unité de données
ms.assetid: 8e8a0ec8-cb7c-4483-86b0-142ea9f2b835
keywords:
- Windows Media Format SDK, formats d’entrée et paramètres
- Windows Media Format SDK, Data Unit extensions
- SDK Windows Media format, systèmes d’extension de charge utile
- ASF (Advanced Systems Format), formats d’entrée et paramètres
- ASF (format des systèmes avancés), formats d’entrée et paramètres
- ASF (Advanced Systems Format), extensions d’unité de données
- ASF (format de systèmes avancés), extensions d’unité de données
- ASF (Advanced Systems Format), systèmes d’extension de charge utile
- ASF (format de systèmes avancés), systèmes d’extension de charge utile
- extensions d’unité de données, à propos de
- systèmes d’extension de charge utile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c590895fca23a3c668a19ac4e6c5437a35ddb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940207"
---
# <a name="input-formats-input-settings-and-data-unit-extensions"></a><span data-ttu-id="11ea9-114">Formats d’entrée, paramètres d’entrée et extensions d’unité de données</span><span class="sxs-lookup"><span data-stu-id="11ea9-114">Input Formats, Input Settings, and Data Unit Extensions</span></span>

<span data-ttu-id="11ea9-115">L’objet Writer prend en charge les paramètres d’entrée, les formats d’entrée et les extensions d’unité de données, qui vous permettent de contrôler les fonctionnalités du writer.</span><span class="sxs-lookup"><span data-stu-id="11ea9-115">The writer object supports input settings, input formats, and data unit extensions, all of which enable you to control features of the writer.</span></span> <span data-ttu-id="11ea9-116">Il n’est pas toujours évident de déterminer les méthodes à utiliser pour contrôler une fonctionnalité spécifique.</span><span class="sxs-lookup"><span data-stu-id="11ea9-116">It is not always obvious which methods to use to control a specific feature.</span></span>

<span data-ttu-id="11ea9-117">Les formats d’entrée sont des formats multimédias qui décrivent les propriétés de base du média que vous transmettez à l’enregistreur pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="11ea9-117">Input formats are media formats that describe the basic properties of the media that you pass to the writer for encoding.</span></span> <span data-ttu-id="11ea9-118">Par exemple, la taille de frame et l’espace colorimétrique de la vidéo d’entrée sont décrits par le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="11ea9-118">For example, the frame size and color space of input video is described by the input format.</span></span>

<span data-ttu-id="11ea9-119">Les paramètres d’entrée sont des caractéristiques des données d’entrée au-delà des principes de base, ou des informations sur les transformations à effectuer sur les données.</span><span class="sxs-lookup"><span data-stu-id="11ea9-119">Input settings are characteristics of the input data beyond the basics, or information about transforms to perform on the data.</span></span> <span data-ttu-id="11ea9-120">Les paramètres vidéo entrelacés et les informations sur un système de filigrane sont des exemples de paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="11ea9-120">Interlaced video settings and information about a watermarking system are examples of input settings.</span></span>

<span data-ttu-id="11ea9-121">Les extensions d’unité de données, également appelées systèmes d’extension de charge utile, sont des valeurs qui sont attachées à des échantillons individuels dans la section de données du fichier.</span><span class="sxs-lookup"><span data-stu-id="11ea9-121">Data unit extensions, also called payload extension systems, are values that are attached to individual samples in the data section of the file.</span></span> <span data-ttu-id="11ea9-122">Les codes temporels SMPTE et les informations sur les pixels non carrés sont des exemples d’extensions d’unité de données.</span><span class="sxs-lookup"><span data-stu-id="11ea9-122">SMPTE time codes and non-square pixel information are examples of data unit extensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11ea9-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11ea9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11ea9-124">**Configuration d’extensions d’unité de données**</span><span class="sxs-lookup"><span data-stu-id="11ea9-124">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="11ea9-125">**Extensions d’unité de données**</span><span class="sxs-lookup"><span data-stu-id="11ea9-125">**Data Unit Extensions**</span></span>](data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="11ea9-126">**Fonctionnalités d’écriture de fichier**</span><span class="sxs-lookup"><span data-stu-id="11ea9-126">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="11ea9-127">**Énumération de format d’entrée**</span><span class="sxs-lookup"><span data-stu-id="11ea9-127">**Input Format Enumeration**</span></span>](input-format-enumeration.md)
</dt> <dt>

[<span data-ttu-id="11ea9-128">**Paramètres d’entrée**</span><span class="sxs-lookup"><span data-stu-id="11ea9-128">**Input Settings**</span></span>](input-settings.md)
</dt> <dt>

[<span data-ttu-id="11ea9-129">**Utilisation des entrées**</span><span class="sxs-lookup"><span data-stu-id="11ea9-129">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




