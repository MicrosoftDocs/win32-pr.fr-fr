---
description: Prise en charge ASF dans Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Prise en charge ASF dans Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522274"
---
# <a name="asf-support-in-media-foundation"></a><span data-ttu-id="7da62-103">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7da62-103">ASF Support in Media Foundation</span></span>

<span data-ttu-id="7da62-104">Media Foundation prend en charge les fichiers multimédias au format ASF (Advanced Systems Format) :</span><span class="sxs-lookup"><span data-stu-id="7da62-104">Media Foundation supports media files in the Advanced Systems Format (ASF):</span></span>

-   <span data-ttu-id="7da62-105">Windows Media Video (fichiers WMV)</span><span class="sxs-lookup"><span data-stu-id="7da62-105">Windows Media Video (WMV files)</span></span>
-   <span data-ttu-id="7da62-106">Windows Media Audio (fichiers WMA)</span><span class="sxs-lookup"><span data-stu-id="7da62-106">Windows Media Audio (WMA files)</span></span>

<span data-ttu-id="7da62-107">Media Foundation fournit plusieurs objets pour la lecture et l’écriture de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="7da62-107">Media Foundation provides several objects for reading and writing ASF files.</span></span> <span data-ttu-id="7da62-108">Ces objets sont fournis dans deux couches architecturales différentes.</span><span class="sxs-lookup"><span data-stu-id="7da62-108">These objects are provided in two different architectural layers.</span></span>

<span data-ttu-id="7da62-109">Tout d’abord, la couche de *pipeline* contient des objets qui fonctionnent dans le [pipeline Media Foundation](media-foundation-pipeline.md) et sont conformes aux API définies par le pipeline.</span><span class="sxs-lookup"><span data-stu-id="7da62-109">First, the *pipeline* layer contains objects that work inside the [Media Foundation pipeline](media-foundation-pipeline.md) and conform to the APIs defined by the pipeline.</span></span> <span data-ttu-id="7da62-110">La couche de pipeline ASF contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7da62-110">The ASF pipeline layer contains:</span></span>

-   <span data-ttu-id="7da62-111">[Source du média ASF](asf-media-source.md): analyse les fichiers ASF et remet les paquets de données audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="7da62-111">[ASF Media Source](asf-media-source.md): Parses ASF files and delivers the audio/video data packets.</span></span>
-   <span data-ttu-id="7da62-112">[Codecs Windows Media](windows-media-codecs.md): décodez ou encodez des flux audio ou vidéo Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7da62-112">[Windows Media Codecs](windows-media-codecs.md): Decode or encode Windows Media audio or video streams.</span></span>
-   <span data-ttu-id="7da62-113">[Récepteur multimédia ASF](asf-media-sinks.md): reçoit les paquets de données et écrit un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="7da62-113">[ASF Media Sink](asf-media-sinks.md): Receives data packets and writes an ASF file.</span></span>

<span data-ttu-id="7da62-114">Deuxièmement, la couche de conteneur WM offre un contrôle de bas niveau de l’analyse et de l’écriture d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="7da62-114">Second, the WM Container layer provides low-level control over parsing and writing an ASF file.</span></span> <span data-ttu-id="7da62-115">La couche de pipeline utilise WMContainer en interne.</span><span class="sxs-lookup"><span data-stu-id="7da62-115">The pipeline layer uses WMContainer internally.</span></span> <span data-ttu-id="7da62-116">Les applications peuvent également utiliser WMContainer pour l’analyse et l’écriture ASF de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="7da62-116">Applications can also use WMContainer for low-level ASF parsing and writing.</span></span>

![Diagramme montrant les éléments de la couche de pipeline et le conteneur WM](images/asf-components.png)

## <a name="in-this-section"></a><span data-ttu-id="7da62-118">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="7da62-118">In this section</span></span>



| <span data-ttu-id="7da62-119">Rubrique</span><span class="sxs-lookup"><span data-stu-id="7da62-119">Topic</span></span>                                                                         | <span data-ttu-id="7da62-120">Description</span><span class="sxs-lookup"><span data-stu-id="7da62-120">Description</span></span>                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7da62-121">Structure de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="7da62-121">ASF File Structure</span></span>](asf-file-structure.md)<br/>                       | <span data-ttu-id="7da62-122">Vue d’ensemble de la structure de fichiers ASF et des objets fournis par Media Foundation pour travailler avec des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="7da62-122">Overview of the ASF file structure and the objects provided by Media Foundation to work with ASF files.</span></span><br/> |
| [<span data-ttu-id="7da62-123">Composants ASF de couche de pipeline</span><span class="sxs-lookup"><span data-stu-id="7da62-123">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)<br/> | <span data-ttu-id="7da62-124">Décrit comment analyser et créer des fichiers ASF à l’aide de la couche de pipeline.</span><span class="sxs-lookup"><span data-stu-id="7da62-124">Describes how to parse and author ASF files using the pipeline layer.</span></span><br/>                                   |
| [<span data-ttu-id="7da62-125">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="7da62-125">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)<br/>       | <span data-ttu-id="7da62-126">Décrit comment analyser et créer des fichiers ASF à l’aide de la couche WMContainer.</span><span class="sxs-lookup"><span data-stu-id="7da62-126">Describes how to parse and author ASF files using the WMContainer layer.</span></span><br/>                                |



 

<span data-ttu-id="7da62-127">Pour plus d’informations sur la structure d’un fichier ASF, consultez la spécification ASF, qui peut être téléchargée à partir de ce [site Web Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="7da62-127">For detailed information about the structure of an ASF file, see the ASF specification, which can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7da62-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7da62-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7da62-129">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7da62-129">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




