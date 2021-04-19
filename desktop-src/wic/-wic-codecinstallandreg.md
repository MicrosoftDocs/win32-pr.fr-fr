---
description: Lorsque vous installez un codec, vous devez l’inscrire dans le registre. Vous devez également vous assurer que le cache de miniatures est mis à jour si des images dans votre format existent déjà sur l’ordinateur.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Installation et inscription du codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522045"
---
# <a name="codec-installation-and-registration"></a><span data-ttu-id="8ad59-104">Installation et inscription du codec</span><span class="sxs-lookup"><span data-stu-id="8ad59-104">Codec Installation and Registration</span></span>

<span data-ttu-id="8ad59-105">Lorsque vous installez un codec, vous devez l’inscrire dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8ad59-105">When you install a codec, you must register it in the registry.</span></span> <span data-ttu-id="8ad59-106">Vous devez également vous assurer que le cache de miniatures est mis à jour si des images dans votre format existent déjà sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8ad59-106">You must also make sure the thumbnail cache gets updated in case any images in your format already exist on the computer.</span></span>

<span data-ttu-id="8ad59-107">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ad59-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="8ad59-108">Inscription d’un codec</span><span class="sxs-lookup"><span data-stu-id="8ad59-108">Registering a Codec</span></span>](#registering-a-codec)
-   [<span data-ttu-id="8ad59-109">Mise à jour du cache de miniatures lors de l’installation de votre codec</span><span class="sxs-lookup"><span data-stu-id="8ad59-109">Updating the Thumbnail Cache When Installing Your Codec</span></span>](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [<span data-ttu-id="8ad59-110">Mise à la disposition des utilisateurs de votre codec WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8ad59-110">Making Your WIC-Enabled Codec Available To Users</span></span>](#making-your-wic-enabled-codec-available-to-users)
-   [<span data-ttu-id="8ad59-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ad59-111">Related topics</span></span>](#related-topics)

## <a name="registering-a-codec"></a><span data-ttu-id="8ad59-112">Inscription d’un codec</span><span class="sxs-lookup"><span data-stu-id="8ad59-112">Registering a Codec</span></span>

<span data-ttu-id="8ad59-113">Lorsque vous inscrivez un codec, vous inscrivez en fait deux composants : l’encodeur et le décodeur.</span><span class="sxs-lookup"><span data-stu-id="8ad59-113">When you register a codec, you are actually registering two components: the encoder and the decoder.</span></span> <span data-ttu-id="8ad59-114">Vous devez également créer des entrées de Registre pour inscrire votre format de conteneur auprès des gestionnaires de métadonnées pour les formats de métadonnées pris en charge par votre format d’image.</span><span class="sxs-lookup"><span data-stu-id="8ad59-114">You also need to make registry entries to register your container format with the metadata handlers for the metadata formats that your image format supports.</span></span>

<span data-ttu-id="8ad59-115">Les rubriques suivantes décrivent les entrées de registre dont vous avez besoin pour inscrire votre codec :</span><span class="sxs-lookup"><span data-stu-id="8ad59-115">The following topics describe the registry entries you need to register your codec:</span></span>

[<span data-ttu-id="8ad59-116">Entrées de Registre générales</span><span class="sxs-lookup"><span data-stu-id="8ad59-116">General Registry Entries</span></span>](-wic-generalregentries.md)

[<span data-ttu-id="8ad59-117">Entrées de Registre spécifiques à l’encodeur</span><span class="sxs-lookup"><span data-stu-id="8ad59-117">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)

[<span data-ttu-id="8ad59-118">Entrées de Registre spécifiques au décodeur</span><span class="sxs-lookup"><span data-stu-id="8ad59-118">Decoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)

[<span data-ttu-id="8ad59-119">Intégration à la Galerie de photos Windows et à l’Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="8ad59-119">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a><span data-ttu-id="8ad59-120">Mise à jour du cache de miniatures lors de l’installation de votre codec</span><span class="sxs-lookup"><span data-stu-id="8ad59-120">Updating the Thumbnail Cache When Installing Your Codec</span></span>

<span data-ttu-id="8ad59-121">Lorsqu’un codec est installé, le programme d’installation doit appeler la fonction suivante après avoir écrit ses entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="8ad59-121">When a codec is installed, the installer needs to call the following function after writing its registry entries.</span></span>


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



<span data-ttu-id="8ad59-122">Cet appel informe Windows que de nouvelles informations d’association de fichiers sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="8ad59-122">This call notifies Windows that new file association information is available.</span></span> <span data-ttu-id="8ad59-123">Si des images dans votre format d’image existent déjà sur l’ordinateur, le cache de miniatures contiendra des miniatures par défaut, car aucun décodeur n’était disponible pour extraire les miniatures lorsque les images ont été acquises pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="8ad59-123">If images in your image format already exist on the computer, the thumbnail cache will contain default thumbnails for them because no decoder was available to extract the thumbnails when the images were first acquired.</span></span> <span data-ttu-id="8ad59-124">Lorsque vous notifiez Windows qu’une nouvelle association de fichiers est disponible, le cache de miniatures ignore les miniatures vides et extrait les miniatures réelles des fichiers qui peuvent maintenant être décodés.</span><span class="sxs-lookup"><span data-stu-id="8ad59-124">When you notify Windows that a new file association is available, the thumbnail cache discards any empty thumbnails and extracts the actual thumbnails from the files that can now be decoded.</span></span>

## <a name="making-your-wic-enabled-codec-available-to-users"></a><span data-ttu-id="8ad59-125">Mise à la disposition des utilisateurs de votre codec WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8ad59-125">Making Your WIC-Enabled Codec Available To Users</span></span>

<span data-ttu-id="8ad59-126">Si vous êtes un fabricant d’appareils photo, vous pouvez expédier vos codecs bruts dans le boîtier avec vos appareils photo.</span><span class="sxs-lookup"><span data-stu-id="8ad59-126">If you are a camera manufacturer, you can ship your raw codecs in the box with your cameras.</span></span> <span data-ttu-id="8ad59-127">Vous pouvez également poster vos codecs sur la page de téléchargement de votre site Web.</span><span class="sxs-lookup"><span data-stu-id="8ad59-127">You can also post your codecs on the Download page of your Web site.</span></span> <span data-ttu-id="8ad59-128">Toutefois, si un utilisateur acquiert un fichier image dans votre format à partir d’une autre source, telle qu’un ami, un partenaire commercial ou un autre site Web, il peut ne pas savoir où obtenir le codec pour le décoder.</span><span class="sxs-lookup"><span data-stu-id="8ad59-128">However, if a user acquires an image file in your format from some other source, such as a friend, business associate, or some other Web site, they may not know where to get the codec to decode it with.</span></span>

<span data-ttu-id="8ad59-129">En raison de ce problème, Windows offre aux utilisateurs de votre format d’image un moyen plus simple de rechercher votre codec et de le télécharger sur leur ordinateur, en commençant par Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8ad59-129">Because of this issue, Windows offers an easier way for users of your image format to find your codec and download it onto their computer, starting with Windows Vista.</span></span> <span data-ttu-id="8ad59-130">Si la Galerie de photos Windows reconnaît une extension de nom de fichier en tant que format d’image et que le codec pour ce format n’est pas installé, une boîte de dialogue indique à l’utilisateur que la photo ne peut pas être affichée et demande si l’utilisateur souhaite télécharger le logiciel requis pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="8ad59-130">If the Windows Photo Gallery recognizes a file name extension as an image format, and the codec for that format is not installed, a dialog box tells the user that the photo can’t be displayed, and asks whether the user wants to download the software required to display it.</span></span> <span data-ttu-id="8ad59-131">Lorsque l’utilisateur accepte, un site Web hébergé par Microsoft s’affiche avec un lien vers le site de téléchargement du fabricant du codec.</span><span class="sxs-lookup"><span data-stu-id="8ad59-131">When the user accepts, a Microsoft-hosted Web site appears with a link to the codec manufacturer’s download site.</span></span> <span data-ttu-id="8ad59-132">(Si vous le souhaitez, vous pouvez demander que les utilisateurs soient directement dirigés vers votre site de téléchargement.)</span><span class="sxs-lookup"><span data-stu-id="8ad59-132">(Optionally, you can request that users be taken directly to your download site.)</span></span>

<span data-ttu-id="8ad59-133">Si vous souhaitez que les extensions de nom de fichier de votre format d’image soient reconnues par la Galerie de photos Windows afin que les utilisateurs puissent être dirigés vers votre site de téléchargement, vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ad59-133">If you want your image format’s file name extensions to be recognized by the Windows Photo Gallery so that users can be directed to your download site, you must do the following:</span></span>

1.  <span data-ttu-id="8ad59-134">Fournissez un site de téléchargement pour votre codec.</span><span class="sxs-lookup"><span data-stu-id="8ad59-134">Provide a download site for your codec.</span></span> <span data-ttu-id="8ad59-135">(Vous pouvez avoir une page distincte pour chaque codec que vous fournissez ou une page qui fournit des téléchargements pour tous vos codecs).</span><span class="sxs-lookup"><span data-stu-id="8ad59-135">(You can have a separate page for each codec you provide, or one page that provides downloads for all your codecs.)</span></span>

    <span data-ttu-id="8ad59-136">Le site de téléchargement doit être localisé et facilement consultable par le modèle d’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="8ad59-136">The download site should be localized and easily searchable by camera model.</span></span>

2.  <span data-ttu-id="8ad59-137">Fournissez à Microsoft une liste d’extensions pour vos formats d’image et les URL de vos sites de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="8ad59-137">Provide Microsoft with a list of extensions for your image formats, and the URLs for your download sites.</span></span>

<span data-ttu-id="8ad59-138">Vous devez informer Microsoft des extensions pour les nouveaux codecs que vous développez à l’avenir, ainsi que des modifications apportées aux URL de vos sites de téléchargement, afin que les nouvelles informations puissent être ajoutées à la Galerie de photos Windows.</span><span class="sxs-lookup"><span data-stu-id="8ad59-138">You must inform Microsoft of the extensions for any new codecs you develop in the future, and of any changes to the URLs of your download sites, so that the new information can be added to the Windows Photo Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ad59-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ad59-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8ad59-140">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="8ad59-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8ad59-141">Implémentation de IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="8ad59-141">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="8ad59-142">Conclusion (écriture d’un CODEC WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="8ad59-142">Conclusion (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[<span data-ttu-id="8ad59-143">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8ad59-143">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="8ad59-144">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="8ad59-144">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



