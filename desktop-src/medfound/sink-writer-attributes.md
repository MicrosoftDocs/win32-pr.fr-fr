---
description: Attributs du writer du récepteur
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Attributs du writer du récepteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114354"
---
# <a name="sink-writer-attributes"></a><span data-ttu-id="748a6-103">Attributs du writer du récepteur</span><span class="sxs-lookup"><span data-stu-id="748a6-103">Sink Writer Attributes</span></span>

<span data-ttu-id="748a6-104">Les attributs suivants peuvent être utilisés pour initialiser le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="748a6-104">The following attributes can be used to initialize the sink writer.</span></span>



| <span data-ttu-id="748a6-105">Attribut</span><span class="sxs-lookup"><span data-stu-id="748a6-105">Attribute</span></span>                                                                                  | <span data-ttu-id="748a6-106">Description</span><span class="sxs-lookup"><span data-stu-id="748a6-106">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="748a6-107">\_latence faible \_ MF</span><span class="sxs-lookup"><span data-stu-id="748a6-107">MF\_LOW\_LATENCY</span></span>](mf-low-latency.md)                                                     | <span data-ttu-id="748a6-108">Active le traitement à faible latence.</span><span class="sxs-lookup"><span data-stu-id="748a6-108">Enables low-latency processing.</span></span>                                                                                                                                                                                                    |
| [<span data-ttu-id="748a6-109">\_ \_ convertisseurs de désactivation MF ReadWrite \_</span><span class="sxs-lookup"><span data-stu-id="748a6-109">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)                  | <span data-ttu-id="748a6-110">Active ou désactive les conversions de format par le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="748a6-110">Enables or disables format conversions by the sink writer.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="748a6-111">MF \_ ReadWrite \_ activer \_ les \_ transformations matérielles</span><span class="sxs-lookup"><span data-stu-id="748a6-111">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS</span></span>](mf-readwrite-enable-hardware-transforms.md) | <span data-ttu-id="748a6-112">Permet au writer de récepteur d’utiliser des transformations de Media Foundation basées sur le matériel (MFTs).</span><span class="sxs-lookup"><span data-stu-id="748a6-112">Enables the sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>                                                                                                                                                  |
| [<span data-ttu-id="748a6-113">\_ \_ rappel asynchrone du writer de récepteur MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="748a6-113">MF\_SINK\_WRITER\_ASYNC\_CALLBACK</span></span>](mf-sink-writer-async-callback.md)                     | <span data-ttu-id="748a6-114">Contient un pointeur vers l’interface de rappel de l’application pour le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="748a6-114">Contains a pointer to the application's callback interface for the sink writer.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="748a6-115">\_limitation de \_ \_ désactivation de l’enregistreur de récepteur MF \_</span><span class="sxs-lookup"><span data-stu-id="748a6-115">MF\_SINK\_WRITER\_DISABLE\_THROTTLING</span></span>](mf-sink-writer-disable-throttling.md)             | <span data-ttu-id="748a6-116">Spécifie si l’enregistreur du récepteur limite le taux des données entrantes.</span><span class="sxs-lookup"><span data-stu-id="748a6-116">Specifies whether the sink writer limits the rate of incoming data.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="748a6-117">\_CONTAINERTYPE de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="748a6-117">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                             | <span data-ttu-id="748a6-118">Spécifie le type de conteneur du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="748a6-118">Specifies the container type of the output file.</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="748a6-119">\_Attribut de \_ déverrouillage MFT FIELDOFUSE \_</span><span class="sxs-lookup"><span data-stu-id="748a6-119">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)                  | <span data-ttu-id="748a6-120">Contient un pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , utilisé pour déverrouiller une table MFT avec des restrictions de champ d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="748a6-120">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which is used to unlock an MFT with field-of-use restrictions.</span></span> <span data-ttu-id="748a6-121">Pour plus d’informations, consultez [restrictions relatives au champ d’utilisation](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="748a6-121">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> |
| [<span data-ttu-id="748a6-122">\_ \_ \_ Gestionnaire D3D de l’enregistreur du récepteur MF \_</span><span class="sxs-lookup"><span data-stu-id="748a6-122">MF\_SINK\_WRITER\_D3D\_MANAGER</span></span>](mf-sink-writer-d3d-manager.md)                           | <span data-ttu-id="748a6-123">Utilisez cet attribut pour fournir un appareil Direct3D pour tous les encodeurs vidéo ou récepteurs multimédias chargés par le writer du récepteur.</span><span class="sxs-lookup"><span data-stu-id="748a6-123">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the sink writer.</span></span>                                                                                                                   |



 

<span data-ttu-id="748a6-124">Utilisez ces attributs avec les méthodes et fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="748a6-124">Use these attributes with the following methods and functions:</span></span>

-   [<span data-ttu-id="748a6-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span><span class="sxs-lookup"><span data-stu-id="748a6-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [<span data-ttu-id="748a6-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span><span class="sxs-lookup"><span data-stu-id="748a6-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [<span data-ttu-id="748a6-127">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="748a6-127">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="748a6-128">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="748a6-128">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="748a6-129">Pour utiliser l’un de ces attributs, appelez d’abord [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un nouveau magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="748a6-129">To use any of these attributes, first call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span> <span data-ttu-id="748a6-130">Utilisez ensuite l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour définir les attributs souhaités sur le magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="748a6-130">Then use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface to set the desired attributes on the attribute store.</span></span> <span data-ttu-id="748a6-131">Transmettez le pointeur **IMFAttributes** au paramètre *pAttributes* de l’une des méthodes ou fonctions indiquées précédemment.</span><span class="sxs-lookup"><span data-stu-id="748a6-131">Pass the **IMFAttributes** pointer to the *pAttributes* parameter of any of the methods or functions listed previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="748a6-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="748a6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="748a6-133">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="748a6-133">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="748a6-134">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="748a6-134">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



