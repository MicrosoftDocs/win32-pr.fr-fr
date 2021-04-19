---
description: Écriture d’un objet d’en-tête ASF pour un nouveau fichier
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Écriture d’un objet d’en-tête ASF pour un nouveau fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521153"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a><span data-ttu-id="9fced-103">Écriture d’un objet d’en-tête ASF pour un nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="9fced-103">Writing an ASF Header Object for a New File</span></span>

<span data-ttu-id="9fced-104">L’objet ASF ContentInfo stocke les informations d’objet d’en-tête ASF pour un fichier.</span><span class="sxs-lookup"><span data-stu-id="9fced-104">The ASF ContentInfo object stores ASF Header Object information for a file.</span></span> <span data-ttu-id="9fced-105">Lors de la création ou de la modification d’un fichier ASF, l’objet d’en-tête doit être généré.</span><span class="sxs-lookup"><span data-stu-id="9fced-105">When an ASF file is created or modified, the Header Object must be generated.</span></span> <span data-ttu-id="9fced-106">Pour ce faire, l’application doit fournir le profil d’encodage du contenu à l’objet ContentInfo afin qu’il sache les caractéristiques du fichier multimédia à créer.</span><span class="sxs-lookup"><span data-stu-id="9fced-106">To do this, the application must provide the encoding profile of the content to the ContentInfo object so that it knows the characteristics of the media file to be created.</span></span>

<span data-ttu-id="9fced-107">Pour écrire un nouveau fichier, vous pouvez utiliser l’objet ContentInfo pour :</span><span class="sxs-lookup"><span data-stu-id="9fced-107">For writing a new file, you can use the ContentInfo object to:</span></span>

-   <span data-ttu-id="9fced-108">Collecter les informations d’en-tête à partir de l’objet profil du fichier à créer,</span><span class="sxs-lookup"><span data-stu-id="9fced-108">Collect header information from the profile object of the file to be created,</span></span>
-   <span data-ttu-id="9fced-109">Remplir plusieurs objets d’en-tête dans la bibliothèque ASF gérée en interne par Media Foundation,</span><span class="sxs-lookup"><span data-stu-id="9fced-109">Populate various Header Objects in the ASF library maintained internally by Media Foundation,</span></span>
-   <span data-ttu-id="9fced-110">Initialiser le [multiplexeur ASF](asf-multiplexer.md) pour la génération de paquets de données ASF et</span><span class="sxs-lookup"><span data-stu-id="9fced-110">Initialize the [ASF Multiplexer](asf-multiplexer.md) for ASF data packet generation, and</span></span>
-   <span data-ttu-id="9fced-111">Construit l’objet d’en-tête de niveau supérieur au format binaire qui peut être écrit dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="9fced-111">Construct the top-level Header Object in binary format that can be written to a file.</span></span>

<span data-ttu-id="9fced-112">Pour plus d’informations sur les profils, consultez [ASF Profile](asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="9fced-112">For information about profiles, see [ASF Profile](asf-profile.md).</span></span>

<span data-ttu-id="9fced-113">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fced-113">This section contains the following topics:</span></span>



| <span data-ttu-id="9fced-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9fced-114">Topic</span></span>                                                                                                              | <span data-ttu-id="9fced-115">Description</span><span class="sxs-lookup"><span data-stu-id="9fced-115">Description</span></span>                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fced-116">Initialisation de l’objet ContentInfo d’un nouveau fichier ASF</span><span class="sxs-lookup"><span data-stu-id="9fced-116">Initializing the ContentInfo Object of a New ASF File</span></span>](initializing-the-contentinfo-object-of-a-new-asf-file.md) | <span data-ttu-id="9fced-117">Décrit la méthode [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) qui initialise l’objet ContentInfo avec les informations d’en-tête stockées dans un objet de profil.</span><span class="sxs-lookup"><span data-stu-id="9fced-117">Describes the [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) method that initializes the ContentInfo object with header information stored in a profile object.</span></span> |
| [<span data-ttu-id="9fced-118">Définition des propriétés dans l’objet ContentInfo</span><span class="sxs-lookup"><span data-stu-id="9fced-118">Setting Properties in the ContentInfo Object</span></span>](setting-properties-in-the-contentinfo-object.md)                   | <span data-ttu-id="9fced-119">Informations sur les différentes propriétés de configuration qui doivent être définies sur l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="9fced-119">Information about various configuration properties that must be set on the ContentInfo object.</span></span>                                                                                         |
| [<span data-ttu-id="9fced-120">Génération d’un nouvel objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="9fced-120">Generating a New ASF Header Object</span></span>](generating-a-new-asf-header-object.md)                                       | <span data-ttu-id="9fced-121">Comment générer une mémoire tampon de média, qui contient l’objet d’en-tête ASF réel du nouveau fichier, à partir de l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="9fced-121">How to generate a media buffer, which contains the actual ASF Header Object of the new file, from the ContentInfo object.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="9fced-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9fced-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fced-123">Objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="9fced-123">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="9fced-124">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="9fced-124">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="9fced-125">Structure de fichiers ASF</span><span class="sxs-lookup"><span data-stu-id="9fced-125">ASF File Structure</span></span>
</dt> </dl>

 

 



