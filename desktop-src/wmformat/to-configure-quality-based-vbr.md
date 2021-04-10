---
title: Pour configurer Quality-Based VBR
description: Pour configurer Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- flux, configuration des flux VBR
- flux, débit binaire variable (VBR)
- Vitesse de transmission variable (VBR), flux
- VBR (vitesse de transmission variable), flux
- flux, configuration du VBR basé sur la qualité
- Vitesse de transmission variable (VBR), configuration de la qualité
- VBR (vitesse de transmission variable), configuration de la qualité
- profils, configuration du VBR basé sur la qualité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103940756"
---
# <a name="to-configure-quality-based-vbr"></a><span data-ttu-id="307b3-111">Pour configurer Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="307b3-111">To Configure Quality-Based VBR</span></span>

<span data-ttu-id="307b3-112">Vous pouvez utiliser l’encodage VBR (Quality bit rate) sur un flux pour spécifier un niveau de qualité qui sera conservé pour l’ensemble du flux, indépendamment des exigences de vitesse de transmission qui en résultent.</span><span class="sxs-lookup"><span data-stu-id="307b3-112">You can use quality-based variable bit rate (VBR) encoding on a stream to specify a quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>

<span data-ttu-id="307b3-113">Pour les flux vidéo VBR basés sur la qualité, vous devez spécifier un niveau de qualité compris entre 1 et 100, 100 représentant la qualité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="307b3-113">For quality-based VBR video streams, you must specify a quality level from 1 to 100, with 100 representing the highest quality.</span></span> <span data-ttu-id="307b3-114">À l’heure actuelle, il n’existe que 30 paramètres de qualité discrets.</span><span class="sxs-lookup"><span data-stu-id="307b3-114">At present there are only 30 discrete quality settings.</span></span> <span data-ttu-id="307b3-115">Les niveaux de qualité suivants sont équivalents aux paramètres de qualité discrets : 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span><span class="sxs-lookup"><span data-stu-id="307b3-115">The following quality levels equate to discrete quality settings: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span></span> <span data-ttu-id="307b3-116">Les nombres entre deux valeurs consécutives dans la liste précédente sont équivalents au même paramètre de qualité que le nombre inférieur.</span><span class="sxs-lookup"><span data-stu-id="307b3-116">Numbers between two consecutive values in the preceding list equate to the same quality setting as the lower number.</span></span> <span data-ttu-id="307b3-117">Par exemple, 1 et 4 sont répertoriés, si bien que 2 et 3 produisent le même paramètre de qualité que 1.</span><span class="sxs-lookup"><span data-stu-id="307b3-117">For example, 1 and 4 are listed, so 2 and 3 both result in the same quality setting as 1.</span></span>

<span data-ttu-id="307b3-118">Pour les flux audio, vous pouvez énumérer les modes disponibles et récupérer un objet de configuration de flux.</span><span class="sxs-lookup"><span data-stu-id="307b3-118">For audio streams, you can enumerate the available modes and retrieve a stream configuration object.</span></span> <span data-ttu-id="307b3-119">Pour plus d’informations, consultez [pour énumérer des formats de codec](to-enumerate-codec-formats.md).</span><span class="sxs-lookup"><span data-stu-id="307b3-119">For more information, see [To Enumerate Codec Formats](to-enumerate-codec-formats.md).</span></span>

<span data-ttu-id="307b3-120">Lorsque vous utilisez une vidéo VBR basée sur la qualité, vous devez définir le membre **dwBitrate** de la structure [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) sur une valeur positive.</span><span class="sxs-lookup"><span data-stu-id="307b3-120">When using quality-based VBR video, you must set the **dwBitrate** member of the [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure to a positive value.</span></span> <span data-ttu-id="307b3-121">Cette valeur n’est pas utilisée par le writer, mais le passage de zéro ou d’un nombre négatif peut provoquer des erreurs lors de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="307b3-121">This value is not used by the writer, but passing zero or a negative number can cause errors when writing.</span></span>

<span data-ttu-id="307b3-122">Pour configurer un flux dans un profil à encoder avec un VBR basé sur la qualité, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="307b3-122">To configure a stream in a profile to be encoded with quality-based VBR, perform the following steps.</span></span>

1.  <span data-ttu-id="307b3-123">Créez un objet de gestionnaire de profils en appelant la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="307b3-123">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="307b3-124">Ouvrez un profil existant auquel vous souhaitez ajouter la prise en charge VBR.</span><span class="sxs-lookup"><span data-stu-id="307b3-124">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="307b3-125">Pour plus d’informations sur l’ouverture des profils, consultez [utilisation des profils](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="307b3-125">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="307b3-126">Récupérez un objet de configuration de flux pour le flux que vous souhaitez utiliser en appelant [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile :: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="307b3-126">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="307b3-127">Obtenir un pointeur vers l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) de l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="307b3-127">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="307b3-128">Activez le VBR pour le flux en appelant [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) pour la propriété **g \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="307b3-128">Enable VBR for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="307b3-129">Définissez le niveau de qualité pour le flux VBR en appelant **IWMPropertyVault :: SetProperty** pour la propriété **g \_ wszVBRQuality** .</span><span class="sxs-lookup"><span data-stu-id="307b3-129">Set the quality level for the VBR stream by calling **IWMPropertyVault::SetProperty** for the **g\_wszVBRQuality** property.</span></span>
7.  <span data-ttu-id="307b3-130">Affectez aux paramètres **g \_ wszVBRBitrateMax** et **g \_ WszVBRBufferWindowMax** la valeur zéro avec **IWMPropertyVault :: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="307b3-130">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
8.  <span data-ttu-id="307b3-131">Enregistrez les modifications apportées au flux en appelant [**IWMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="307b3-131">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
9.  <span data-ttu-id="307b3-132">Enregistrez le profil ou transmettez-le à l’objet Writer et commencez l’écriture.</span><span class="sxs-lookup"><span data-stu-id="307b3-132">Save the profile, or pass it to the writer object and start writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="307b3-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="307b3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="307b3-134">**Configuration de flux VBR**</span><span class="sxs-lookup"><span data-stu-id="307b3-134">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




