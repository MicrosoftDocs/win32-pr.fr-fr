---
description: Objet ASF ContentInfo
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Objet ASF ContentInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517215"
---
# <a name="asf-contentinfo-object"></a><span data-ttu-id="b7c54-103">Objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="b7c54-103">ASF ContentInfo Object</span></span>

<span data-ttu-id="b7c54-104">L’objet ASF *ContentInfo* stocke les informations de l’objet d’en-tête ASF d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="b7c54-104">The ASF *ContentInfo* object stores information from the ASF Header Object of a file.</span></span> <span data-ttu-id="b7c54-105">Une application peut utiliser l’objet ContentInfo pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7c54-105">An application can use the ContentInfo object for the following purposes:</span></span>

-   <span data-ttu-id="b7c54-106">Lire l’objet d’en-tête d’un fichier multimédia existant.</span><span class="sxs-lookup"><span data-stu-id="b7c54-106">Read the Header Object for an existing media file.</span></span> <span data-ttu-id="b7c54-107">Dans ce cas, l’objet ContentInfo analyse l’objet d’en-tête et stocke les informations sur le fichier de caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="b7c54-107">In this case, the ContentInfo object parses the Header Object and stores information about the characteristics file.</span></span> <span data-ttu-id="b7c54-108">Media Foundation expose plusieurs de ces propriétés via des attributs et des interfaces.</span><span class="sxs-lookup"><span data-stu-id="b7c54-108">Media Foundation exposes several of these properties through attributes and interfaces.</span></span> <span data-ttu-id="b7c54-109">Celles-ci sont décrites dans [Media Foundation attributs pour les objets d’en-tête ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b7c54-109">These are described in [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>
-   <span data-ttu-id="b7c54-110">Écrire des informations d’en-tête et construire un objet d’en-tête pour un nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="b7c54-110">Write header information and construct a Header Object for a new file.</span></span>
-   <span data-ttu-id="b7c54-111">Initialiser d’autres objets ASF tels que le [séparateur ASF](asf-splitter.md), le [multiplexeur ASF](asf-multiplexer.md)et l’indexeur ASF, lors de la lecture ou de l’écriture d’un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="b7c54-111">Initialize other ASF objects such as the [ASF Splitter](asf-splitter.md), [ASF Multiplexer](asf-multiplexer.md), and the ASF Indexer, while reading or writing a media file.</span></span>

<span data-ttu-id="b7c54-112">Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="b7c54-112">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="creating-the-contentinfo-object"></a><span data-ttu-id="b7c54-113">Création de l’objet ContentInfo</span><span class="sxs-lookup"><span data-stu-id="b7c54-113">Creating the ContentInfo Object</span></span>

<span data-ttu-id="b7c54-114">Pour créer une nouvelle instance de l’objet ContentInfo, appelez la fonction [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="b7c54-114">To create a new instance of the ContentInfo object, call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function.</span></span> <span data-ttu-id="b7c54-115">Cette méthode retourne un pointeur vers un objet ContentInfo vide qui doit être initialisé pour fonctionner avec un fichier ASF spécifique.</span><span class="sxs-lookup"><span data-stu-id="b7c54-115">This method returns a pointer to an empty ContentInfo object that must be initialized to work with a specific ASF file.</span></span> <span data-ttu-id="b7c54-116">Selon que l’application lit un fichier existant ou écrit un nouveau fichier ASF, elle doit appeler [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ou [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) pour remplir l’objet vide.</span><span class="sxs-lookup"><span data-stu-id="b7c54-116">Depending on whether the application is reading an existing file or writing a new ASF file, it must call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) or [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to populate the empty object.</span></span>

<span data-ttu-id="b7c54-117">Pour plus d’informations sur ces appels de méthode, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7c54-117">For more information about these method calls, see the following topics:</span></span>

-   [<span data-ttu-id="b7c54-118">Lecture de l’objet d’en-tête ASF d’un fichier existant</span><span class="sxs-lookup"><span data-stu-id="b7c54-118">Reading the ASF Header Object of an Existing File</span></span>](reading-the-asf-header-object-of-an-existing-file.md)
-   [<span data-ttu-id="b7c54-119">Obtention d’informations à partir d’objets d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="b7c54-119">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
-   [<span data-ttu-id="b7c54-120">Écriture d’un objet d’en-tête ASF pour un nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="b7c54-120">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
-   [<span data-ttu-id="b7c54-121">Attributs Media Foundation pour les objets d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="b7c54-121">Media Foundation Attributes for ASF Header Objects</span></span>](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a><span data-ttu-id="b7c54-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7c54-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7c54-123">Composants WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="b7c54-123">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



