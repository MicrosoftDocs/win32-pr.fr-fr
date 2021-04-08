---
description: Cette section contient des rubriques conceptuelles qui décrivent le système de métadonnées WIC (Windows Imaging Component).
ms.assetid: 68f08f5a-eec6-4484-b901-dbe96c443a0d
title: Traitement des métadonnées de l’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475294acb6c5f6836409938fbaedf22306181f08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034872"
---
# <a name="processing-image-metadata"></a><span data-ttu-id="5eccb-103">Traitement des métadonnées de l’image</span><span class="sxs-lookup"><span data-stu-id="5eccb-103">Processing Image Metadata</span></span>

<span data-ttu-id="5eccb-104">Cette section contient des rubriques conceptuelles qui décrivent le système de métadonnées WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="5eccb-104">This section contains conceptual topics that describe the Windows Imaging Component (WIC) metadata system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5eccb-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="5eccb-105">In this section</span></span>



| <span data-ttu-id="5eccb-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5eccb-106">Topic</span></span>                                                                                              | <span data-ttu-id="5eccb-107">Description</span><span class="sxs-lookup"><span data-stu-id="5eccb-107">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eccb-108">Vue d’ensemble des métadonnées WIC</span><span class="sxs-lookup"><span data-stu-id="5eccb-108">WIC Metadata Overview</span></span>](-wic-about-metadata.md)<br/>                                        | <span data-ttu-id="5eccb-109">Cette rubrique présente la prise en charge des métadonnées de création d’images fournie par le WIC.</span><span class="sxs-lookup"><span data-stu-id="5eccb-109">This topic introduces the imaging metadata support provided by the WIC.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="5eccb-110">Vue d’ensemble du langage de requête de métadonnées</span><span class="sxs-lookup"><span data-stu-id="5eccb-110">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)<br/>                | <span data-ttu-id="5eccb-111">Cette rubrique présente le langage de requête de métadonnées pour WIC.</span><span class="sxs-lookup"><span data-stu-id="5eccb-111">This topic introduces the metadata query language for WIC.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="5eccb-112">Requêtes de métadonnées au format d’image natif</span><span class="sxs-lookup"><span data-stu-id="5eccb-112">Native Image Format Metadata Queries</span></span>](-wic-native-image-format-metadata-queries.md)<br/>   | <span data-ttu-id="5eccb-113">Cette rubrique fournit une vue d’ensemble des requêtes de [langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md) pour la lecture et l’écriture de métadonnées prises en charge par les images gif, png, TIFF et JPEG.</span><span class="sxs-lookup"><span data-stu-id="5eccb-113">This topic provides an overview of the [metadata query language](-wic-codec-metadataquerylanguage.md) queries for reading and writing metadata supported by GIF, PNG, TIFF and JPEG images.</span></span><br/>                                                                  |
| [<span data-ttu-id="5eccb-114">Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image</span><span class="sxs-lookup"><span data-stu-id="5eccb-114">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)<br/> | <span data-ttu-id="5eccb-115">Cette rubrique fournit une vue d’ensemble de la façon dont vous pouvez utiliser les API WIC pour lire et écrire des métadonnées incorporées dans des fichiers image.</span><span class="sxs-lookup"><span data-stu-id="5eccb-115">This topic provides an overview of how you can use the WIC APIs to read and write metadata that is embedded in image files.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="5eccb-116">Vue d’ensemble de l’extensibilité des métadonnées</span><span class="sxs-lookup"><span data-stu-id="5eccb-116">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)<br/>                      | <span data-ttu-id="5eccb-117">Cette rubrique présente la configuration requise pour la création de gestionnaires de métadonnées personnalisés pour le WIC, y compris les lecteurs et les enregistreurs de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="5eccb-117">This topic introduces the requirements for creating custom metadata handlers for the WIC, including both metadata readers and writers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="5eccb-118">Vue d’ensemble du balisage des personnes</span><span class="sxs-lookup"><span data-stu-id="5eccb-118">People Tagging Overview</span></span>](-wic-people-tagging.md)<br/>                                      | <span data-ttu-id="5eccb-119">Cette rubrique présente le nouveau schéma XMP (Extensible Metadata Platform) et la propriété photo Windows 7 [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) qui permet d’étiqueter des individus dans une photo numérique.</span><span class="sxs-lookup"><span data-stu-id="5eccb-119">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5eccb-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5eccb-120">See Also</span></span>

[<span data-ttu-id="5eccb-121">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="5eccb-121">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="5eccb-122">Référence</span><span class="sxs-lookup"><span data-stu-id="5eccb-122">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="5eccb-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="5eccb-123">Samples</span></span>](-wic-samples.md)


 

 
