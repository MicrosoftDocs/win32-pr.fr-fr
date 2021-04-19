---
description: Configuration de l’enregistreur ASF
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configuration de l’enregistreur ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515747"
---
# <a name="configuring-the-asf-writer"></a><span data-ttu-id="bbf8b-103">Configuration de l’enregistreur ASF</span><span class="sxs-lookup"><span data-stu-id="bbf8b-103">Configuring the ASF Writer</span></span>

<span data-ttu-id="bbf8b-104">Lorsque le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) est créé, il est configuré automatiquement avec le \_ Profil WMProfile V80 \_ 256Video.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-104">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile.</span></span> <span data-ttu-id="bbf8b-105">Ce profil utilise les codecs Windows Media Audio et Windows Media Video version 8, qui ne sont pas aussi récents que les codecs de la série Windows Media 9.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-105">This profile uses the Windows Media Audio and Windows Media Video version 8 codecs, which are not as recent as the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="bbf8b-106">Il est recommandé de créer un profil personnalisé qui utilise les codecs Windows Media 9 Series et de configurer l’enregistreur ASF WM avec le profil personnalisé, comme décrit dans [configuration de profils et d’autres propriétés de fichier ASF](configuring-profiles-and-other-asf-file-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bbf8b-106">It is recommended to create a custom profile that uses the Windows Media 9 Series codecs, and configure the WM ASF Writer with the custom profile, as described in [Configuring Profiles and Other ASF File Properties](configuring-profiles-and-other-asf-file-properties.md).</span></span> <span data-ttu-id="bbf8b-107">Vous devez ajouter le filtre d’enregistreur ASF WM au graphique de filtre avant de configurer le filtre et configurer le filtre avant de le connecter à d’autres filtres.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-107">You must add the WM ASF Writer filter to the filter graph before configuring the filter, and configure the filter before connecting it to any other filters.</span></span>

<span data-ttu-id="bbf8b-108">Toutes les données d’entrée doivent être horodatées et toutes les broches d’entrée doivent être connectées pour que le filtre puisse être exécuté ou suspendu.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-108">All input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="bbf8b-109">Par conséquent, si vous configurez le filtre avec un profil qui a un flux audio et un flux vidéo, le filtre crée un fichier audio et une broche d’entrée vidéo, et les deux broches doivent être connectées pour que le filtre puisse être exécuté.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-109">Therefore, if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span> <span data-ttu-id="bbf8b-110">Étant donné que le kit de développement logiciel (SDK) du format Windows Media nécessite le fonctionnement d’un flux audio, l’enregistreur ASF WM doit toujours disposer d’un code confidentiel audio d’entrée, même s’il s’agit d’un flux factice, c’est-à-dire un flux audio muet, à vitesse de transmission faible.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-110">Because the Windows Media Format SDK requires an audio stream to work, the WM ASF Writer must always have an input audio pin, even if it is for a dummy stream—that is, a muted, low-bit-rate audio stream.</span></span>

<span data-ttu-id="bbf8b-111">Ajout d’extensions d’unité de données</span><span class="sxs-lookup"><span data-stu-id="bbf8b-111">Adding Data Unit Extensions</span></span>

<span data-ttu-id="bbf8b-112">Vous pouvez configurer un flux de profil pour les extensions d’unité de données, telles que les codes temporels SMPTE, avant ou après la connexion du filtre, à condition que vous suiviez cet ordre d’opérations :</span><span class="sxs-lookup"><span data-stu-id="bbf8b-112">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="bbf8b-113">Ajoutez une ou plusieurs extensions d’unité de données au flux à l’aide de **IWMStreamConfig2 :: AddDataUnitExtension**.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-113">Add one or more data unit extensions to the stream using **IWMStreamConfig2::AddDataUnitExtension**.</span></span>
2.  <span data-ttu-id="bbf8b-114">Appelez **IWMProfile :: ReconfigStream** pour mettre à jour le profil.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-114">Call **IWMProfile::ReconfigStream** to update the profile.</span></span>
3.  <span data-ttu-id="bbf8b-115">Appelez [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) avec l’objet de profil mis à jour.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-115">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) with the updated profile object.</span></span>
4.  <span data-ttu-id="bbf8b-116">Recherchez la broche d’entrée vidéo et appelez sa méthode [**IAMWMBufferPass :: SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) pour inscrire votre interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-116">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="bbf8b-117">Lorsque le graphique est exécuté, votre méthode [**IAMWMBufferPassCallback :: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) est appelée pour chaque frame, et vous pouvez obtenir et définir des propriétés sur l’exemple à l’aide de ses méthodes d’interface **INSSBuffer3** .</span><span class="sxs-lookup"><span data-stu-id="bbf8b-117">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method will be called for each frame, and you will be able to get and set properties on the sample using its **INSSBuffer3** interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="bbf8b-118">Dans certains scénarios nécessitant beaucoup de ressources processeur, comme inverse telecine, le rédacteur WM ASF peut nécessiter plus de tampons de sortie que certains filtres en aval peuvent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-118">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="bbf8b-119">Par exemple, le décodeur DV n’acceptera pas plus d’une mémoire tampon pour sa broche de sortie et c’est le cas pour le décompresseur AVI dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-119">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="bbf8b-120">Si vous rencontrez des problèmes lors de la tentative de connexion à ces filtres, ou éventuellement lors de l’exécution du graphique, il peut être nécessaire d’écrire un filtre intermédiaire qui accepte un nombre quelconque de mémoires tampons sur sa broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="bbf8b-120">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bbf8b-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bbf8b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbf8b-122">Création de fichiers ASF dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="bbf8b-122">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



