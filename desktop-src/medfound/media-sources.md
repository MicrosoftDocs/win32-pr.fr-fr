---
description: Sources multimédias
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Sources multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211228"
---
# <a name="media-sources"></a><span data-ttu-id="1a6db-103">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="1a6db-103">Media Sources</span></span>

<span data-ttu-id="1a6db-104">Les *sources multimédias* sont des objets qui génèrent des données multimédias dans le pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1a6db-104">*Media sources* are objects that generate media data in the Media Foundation pipeline.</span></span> <span data-ttu-id="1a6db-105">Cette section décrit en détail les API source des médias.</span><span class="sxs-lookup"><span data-stu-id="1a6db-105">This section describes the media source APIs in detail.</span></span> <span data-ttu-id="1a6db-106">Lisez cette section si vous implémentez une source de média personnalisée, ou si vous utilisez une source de média en dehors du pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1a6db-106">Read this section if you are implementing a custom media source, or using a media source outside of the Media Foundation pipeline.</span></span>

<span data-ttu-id="1a6db-107">Si votre application utilise la couche de contrôle, elle n’a besoin d’utiliser qu’un sous-ensemble limité des API sources du média.</span><span class="sxs-lookup"><span data-stu-id="1a6db-107">If your application uses the control layer, it needs to use only a limited subset of the media source APIs.</span></span> <span data-ttu-id="1a6db-108">Pour plus d’informations, consultez la rubrique [utilisation de sources multimédias avec la session multimédia](using-media-sources-with-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="1a6db-108">For information, see the topic [Using Media Sources with the Media Session](using-media-sources-with-the-media-session.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1a6db-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1a6db-109">In this section</span></span>



| <span data-ttu-id="1a6db-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1a6db-110">Topic</span></span>                                                                                                 | <span data-ttu-id="1a6db-111">Description</span><span class="sxs-lookup"><span data-stu-id="1a6db-111">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a6db-112">Modèle d’objet de source multimédia</span><span class="sxs-lookup"><span data-stu-id="1a6db-112">Media Source Object Model</span></span>](media-source-object-model.md)<br/>                                 | <span data-ttu-id="1a6db-113">Cette rubrique décrit le modèle d’objet pour les sources multimédias dans Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1a6db-113">This topic describes the object model for media sources in Microsoft Media Foundation</span></span><br/>                     |
| [<span data-ttu-id="1a6db-114">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="1a6db-114">Presentation Descriptors</span></span>](presentation-descriptors.md)<br/>                                   | <span data-ttu-id="1a6db-115">Un *descripteur de présentation* est un objet qui contient la description d’une présentation particulière.</span><span class="sxs-lookup"><span data-stu-id="1a6db-115">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span><br/>      |
| [<span data-ttu-id="1a6db-116">Événements de source de média</span><span class="sxs-lookup"><span data-stu-id="1a6db-116">Media Source Events</span></span>](media-source-events.md)<br/>                                             | <span data-ttu-id="1a6db-117">Cette rubrique répertorie les événements qui sont envoyés par les sources de média et les flux multimédias.</span><span class="sxs-lookup"><span data-stu-id="1a6db-117">This topic lists the events that are sent by media sources and media streams.</span></span><br/>                             |
| [<span data-ttu-id="1a6db-118">Écriture d’une source de média personnalisée</span><span class="sxs-lookup"><span data-stu-id="1a6db-118">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)<br/>                         | <span data-ttu-id="1a6db-119">Cette rubrique décrit comment implémenter une source de média personnalisée dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1a6db-119">This topic describes how to implement a custom media source in Media Foundation.</span></span><br/>                          |
| [<span data-ttu-id="1a6db-120">Étude de cas : source de média MPEG-1</span><span class="sxs-lookup"><span data-stu-id="1a6db-120">Case Study: MPEG-1 Media Source</span></span>](tutorial--writing-a-custom-media-source.md)<br/>             | <span data-ttu-id="1a6db-121">Cette rubrique présente en détail l’exemple du kit de développement logiciel (SDK) [source de média MPEG-1](mpeg1source-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="1a6db-121">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span><br/>        |
| [<span data-ttu-id="1a6db-122">Fournisseurs de métadonnées personnalisés pour les fichiers multimédias</span><span class="sxs-lookup"><span data-stu-id="1a6db-122">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)<br/> | <span data-ttu-id="1a6db-123">Cette rubrique explique comment écrire un gestionnaire de propriétés de shell personnalisé pour une source de média Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1a6db-123">This topic describes how to write a custom Shell property handler for a Media Foundation media source.</span></span><br/>    |
| [<span data-ttu-id="1a6db-124">Résolveur source</span><span class="sxs-lookup"><span data-stu-id="1a6db-124">Source Resolver</span></span>](source-resolver.md)<br/>                                                     | <span data-ttu-id="1a6db-125">Le résolveur de la source crée la source multimédia appropriée pour un contenu donné à partir d'une URL ou d'un flux d'octets.</span><span class="sxs-lookup"><span data-stu-id="1a6db-125">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1a6db-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a6db-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a6db-127">Pipeline Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1a6db-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="1a6db-128">Fournisseurs de métadonnées personnalisés pour les fichiers multimédias</span><span class="sxs-lookup"><span data-stu-id="1a6db-128">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[<span data-ttu-id="1a6db-129">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1a6db-129">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




