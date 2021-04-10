---
title: Utilisation des modèles de conformité des appareils
description: Utilisation des modèles de conformité des appareils
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- profils, modèles de conformité des appareils
- profils, modèles de conformité
- codecs, modèles de conformité des appareils
- codecs, modèles de conformité
- modèles de conformité des appareils, à propos de
- modèles de conformité
- modèles, modèles de conformité des appareils
- ASF (Advanced Systems Format), modèles de conformité des appareils
- ASF (format des systèmes avancés), modèles de conformité des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101249"
---
# <a name="working-with-device-conformance-templates"></a><span data-ttu-id="10242-112">Utilisation des modèles de conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="10242-112">Working with Device Conformance Templates</span></span>

<span data-ttu-id="10242-113">En raison de la grande flexibilité des fichiers ASF, il est souvent difficile de déterminer si un fichier est adapté à la lecture sur un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="10242-113">Because of the great flexibility of ASF files, it is often difficult to determine whether a file is appropriate for playback on a specific device.</span></span> <span data-ttu-id="10242-114">Par exemple, les fichiers écrits pour la lecture locale sur les ordinateurs de bureau ne sont pas optimaux pour une utilisation sur des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="10242-114">For example, files written for local playback on desktop computers are not optimal for use on handheld devices.</span></span> <span data-ttu-id="10242-115">Les modèles de conformité des appareils permettent aux applications d’identifier rapidement le type d’appareil de lecture pour lequel un fichier a été conçu.</span><span class="sxs-lookup"><span data-stu-id="10242-115">Device conformance templates enable applications to quickly identify the type of playback device for which a file was intended.</span></span> <span data-ttu-id="10242-116">Si le modèle de conformité de l’appareil ne correspond pas à l’appareil, l’application peut informer l’utilisateur que le fichier est inapproprié pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="10242-116">If the device conformance template does not match the device, the application can inform the user that the file is inappropriate for the device.</span></span> <span data-ttu-id="10242-117">De cette façon, l’utilisateur peut être assuré d’une meilleure expérience de lecture.</span><span class="sxs-lookup"><span data-stu-id="10242-117">In this way, the user can be assured of a better playback experience.</span></span>

<span data-ttu-id="10242-118">Si vous écrivez des fichiers exclusivement pour une utilisation sur des ordinateurs personnels, les modèles de conformité des appareils ne seront pas autant d’un facteur à prendre en compte lors de la création de profils.</span><span class="sxs-lookup"><span data-stu-id="10242-118">If you are writing files exclusively for use on personal computers, device conformance templates will not be as much of a factor in creating profiles.</span></span> <span data-ttu-id="10242-119">L’objectif principal de ces modèles est de s’assurer que les fichiers créés pour une utilisation avec un matériel spécial sont compatibles avec une gamme complète d’appareils et pas seulement un appareil unique.</span><span class="sxs-lookup"><span data-stu-id="10242-119">The main purpose of these templates is to ensure that files created for use with special hardware are compatible with a whole range of devices and not just a single device.</span></span>

<span data-ttu-id="10242-120">Un modèle de conformité des appareils est une assertion selon laquelle un fichier ASF contient des données encodées dans certains paramètres.</span><span class="sxs-lookup"><span data-stu-id="10242-120">A device conformance template is an assertion that an ASF file contains data encoded within certain parameters.</span></span> <span data-ttu-id="10242-121">Pour plus d’informations sur les paramètres appropriés pour les modèles individuels, consultez [paramètres de modèle de conformité des appareils](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="10242-121">For more information about the settings appropriate to the individual templates, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="10242-122">Les codecs suivants prennent en charge les modèles de conformité des appareils :</span><span class="sxs-lookup"><span data-stu-id="10242-122">The following codecs support device conformance templates:</span></span>

-   <span data-ttu-id="10242-123">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="10242-123">Windows Media Video 9</span></span>
-   <span data-ttu-id="10242-124">Windows Media Audio 9 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="10242-124">Windows Media Audio 9 and later</span></span>
-   <span data-ttu-id="10242-125">Windows Media Audio 9 professionnel et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="10242-125">Windows Media Audio 9 Professional and later</span></span>
-   <span data-ttu-id="10242-126">Voix Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="10242-126">Windows Media Audio 9 Voice</span></span>

<span data-ttu-id="10242-127">Vous n’avez pas besoin de prendre des mesures spéciales pour utiliser les modèles de conformité des appareils.</span><span class="sxs-lookup"><span data-stu-id="10242-127">You do not need to take any special steps to use device conformance templates.</span></span> <span data-ttu-id="10242-128">Le codec écrit automatiquement une chaîne de modèle pour chaque flux approprié dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="10242-128">The codec automatically writes a template string for each appropriate stream in the file.</span></span> <span data-ttu-id="10242-129">Le codec détermine le modèle à utiliser, en fonction des paramètres de configuration de flux du profil.</span><span class="sxs-lookup"><span data-stu-id="10242-129">The codec will decide which template to use, based on the stream configuration settings in the profile.</span></span> <span data-ttu-id="10242-130">Il existe un chevauchement des paramètres de modèle de conformité des appareils. vous pouvez donc demander un modèle spécifique au lieu de laisser le codec en affecter un pour vous.</span><span class="sxs-lookup"><span data-stu-id="10242-130">There is some overlap in device conformance template parameters, so you may want to request a specific template instead of letting the codec assign one for you.</span></span> <span data-ttu-id="10242-131">Vous pouvez spécifier le modèle de votre choix en définissant la \_ propriété g wszDecoderComplexityRequested avec les méthodes de l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) de l’objet de configuration de flux approprié.</span><span class="sxs-lookup"><span data-stu-id="10242-131">You can specify which template you want by setting the g\_wszDecoderComplexityRequested property with the methods of the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the appropriate stream configuration object.</span></span>

<span data-ttu-id="10242-132">Lors de l’écriture d’un fichier ASF, le modèle de conformité de périphérique réel pour chaque flux est défini sur la valeur transmise au writer par le codec.</span><span class="sxs-lookup"><span data-stu-id="10242-132">When an ASF file is written, the actual device conformance template for each stream is set to the value passed to the writer by the codec.</span></span> <span data-ttu-id="10242-133">Lors de l’ouverture d’un fichier en lecture, vous pouvez identifier le modèle dans lequel les flux du fichier sont conformes à l’aide des méthodes de l’interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) pour récupérer l' \_ attribut g wszDeviceConformanceTemplate au niveau du flux.</span><span class="sxs-lookup"><span data-stu-id="10242-133">When opening a file for reading, you can find out which template the streams of the file conform to by using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface to retrieve the g\_wszDeviceConformanceTemplate stream-level attribute.</span></span> <span data-ttu-id="10242-134">Pour plus d’informations sur les attributs, consultez [utilisation des métadonnées](working-with-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="10242-134">For more information about attributes, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="10242-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10242-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10242-136">**Conception de profils**</span><span class="sxs-lookup"><span data-stu-id="10242-136">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="10242-137">**Paramètres du modèle de conformité des appareils**</span><span class="sxs-lookup"><span data-stu-id="10242-137">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> </dl>

 

 




