---
description: Encoder-Specific les entrées de Registre
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific les entrées de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523290"
---
# <a name="encoder-specific-registry-entries"></a><span data-ttu-id="9d0d4-103">Encoder-Specific les entrées de Registre</span><span class="sxs-lookup"><span data-stu-id="9d0d4-103">Encoder-Specific Registry Entries</span></span>


<span data-ttu-id="9d0d4-104">En plus des entrées listées ci-dessus pour l’encodeur, vous devez également inscrire votre encodeur sous la catégorie des encodeurs WIC (Windows Imaging Component) pour que le moteur de découverte puisse le trouver.</span><span class="sxs-lookup"><span data-stu-id="9d0d4-104">In addition to the entries listed above for encoder, you must also register your encoder under the category of Windows Imaging Component (WIC) encoders so the discovery engine can find it.</span></span> <span data-ttu-id="9d0d4-105">Pour ce faire, vous devez créer les entrées de Registre suivantes.</span><span class="sxs-lookup"><span data-stu-id="9d0d4-105">You do this by making the following registry entries.</span></span> <span data-ttu-id="9d0d4-106">Le premier GUID dans les entrées suivantes est l’identificateur de catégorie (CATID) pour WICBitmapEncoders.</span><span class="sxs-lookup"><span data-stu-id="9d0d4-106">The first GUID in the following entries is the category identifier (CATID) for WICBitmapEncoders.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a><span data-ttu-id="9d0d4-107">Inscription d’un format de conteneur avec des enregistreurs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9d0d4-107">Registering a Container Format with Metadata Writers</span></span>

<span data-ttu-id="9d0d4-108">Si vous créez un nouveau format de conteneur pour votre codec, vous devez également créer des entrées de Registre pour prendre en charge les enregistreurs de métadonnées pour les blocs de métadonnées dans vos images.</span><span class="sxs-lookup"><span data-stu-id="9d0d4-108">If you create a new container format for your codec, you must also create registry entries to support metadata writers for the metadata blocks in your images.</span></span> <span data-ttu-id="9d0d4-109">Les entrées suivantes doivent être créées sous l’identificateur de classe (CLSID) de l’enregistreur de métadonnées pour chaque format de métadonnées pris en charge dans votre format de conteneur.</span><span class="sxs-lookup"><span data-stu-id="9d0d4-109">The following entries need to be created under the class identifier (CLSID) of the metadata writer for each metadata format supported in your container format.</span></span> <span data-ttu-id="9d0d4-110">Si votre codec utilise un conteneur TIFF (Tagged Image File Format), ces informations se trouvent déjà dans le registre et vous n’avez pas besoin de créer ces entrées.</span><span class="sxs-lookup"><span data-stu-id="9d0d4-110">If your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry and you don't need to create these entries.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

<span data-ttu-id="9d0d4-111">Si vous utilisez un format de conteneur de style TIFF ou JPEG, vous devez inscrire une association entre votre conteneur et ce format de conteneur.</span><span class="sxs-lookup"><span data-stu-id="9d0d4-111">If you use a TIFF-style or JPEG-style container format, you must register an association between your container and that container format.</span></span> <span data-ttu-id="9d0d4-112">Pour plus d’informations, consultez la présentation de l' [intégration avec la Galerie de photos Windows et l’Explorateur Windows](-wic-integrationregentries.md).</span><span class="sxs-lookup"><span data-stu-id="9d0d4-112">For more information, see the introduction in [Integration with Windows Photo Gallery and Windows Explorer](-wic-integrationregentries.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d0d4-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d0d4-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9d0d4-114">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9d0d4-114">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9d0d4-115">Entrées de Registre générales</span><span class="sxs-lookup"><span data-stu-id="9d0d4-115">General Registry Entries</span></span>](-wic-generalregentries.md)
</dt> <dt>

[<span data-ttu-id="9d0d4-116">Entrées de Registre spécifiques à l’encodeur</span><span class="sxs-lookup"><span data-stu-id="9d0d4-116">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="9d0d4-117">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="9d0d4-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="9d0d4-118">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="9d0d4-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



