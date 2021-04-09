---
title: Pour configurer le VBR sans contrainte
description: Pour configurer le VBR sans contrainte
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- flux, configuration des flux VBR
- flux, débit binaire variable (VBR)
- Vitesse de transmission variable (VBR), flux
- VBR (vitesse de transmission variable), flux
- flux, configuration du VBR sans contrainte
- Vitesse de transmission variable (VBR), configuration sans contrainte
- VBR (vitesse de transmission variable), configuration sans contrainte
- profils, configuration du VBR sans contrainte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101340"
---
# <a name="to-configure-unconstrained-vbr"></a><span data-ttu-id="9a752-111">Pour configurer le VBR sans contrainte</span><span class="sxs-lookup"><span data-stu-id="9a752-111">To Configure Unconstrained VBR</span></span>

<span data-ttu-id="9a752-112">Vous pouvez utiliser l’encodage VBR (variable bit rate) sans contrainte sur un flux pour spécifier une vitesse de transmission moyenne qui sera maintenue dans le contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="9a752-112">You can use unconstrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="9a752-113">Le VBR sans contrainte diffère du CBR normal dans la mesure où la variance de la vitesse de transmission de l’ensemble du flux peut être supérieure.</span><span class="sxs-lookup"><span data-stu-id="9a752-113">Unconstrained VBR differs from normal CBR in that the variance in bit rate throughout the stream can be greater.</span></span>

<span data-ttu-id="9a752-114">La vitesse de transmission du flux, définie avec [**IWMStreamConfig :: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), est utilisée comme taux binaire moyen souhaité.</span><span class="sxs-lookup"><span data-stu-id="9a752-114">The bit rate of the stream, set with [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), is used as the desired average bit rate.</span></span> <span data-ttu-id="9a752-115">Lorsque l’encodage du flux est terminé, vous pouvez utiliser [**IWMPropertyVault :: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) pour récupérer deux propriétés supplémentaires : **g \_ wszVBRPeak** et **g \_ wszBufferAverage**.</span><span class="sxs-lookup"><span data-stu-id="9a752-115">When encoding of the stream is complete, you can use [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) to retrieve two additional properties: **g\_wszVBRPeak** and **g\_wszBufferAverage**.</span></span> <span data-ttu-id="9a752-116">Ces propriétés décrivent respectivement le taux de bits de pointe du contenu encodé et la fenêtre de mémoire tampon moyenne du contenu.</span><span class="sxs-lookup"><span data-stu-id="9a752-116">These properties describe the peak bit rate of the encoded content and the average buffer window of the content, respectively.</span></span>

<span data-ttu-id="9a752-117">Le VBR sans contrainte doit être utilisé conjointement avec l’encodage en deux passes.</span><span class="sxs-lookup"><span data-stu-id="9a752-117">Unconstrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="9a752-118">L’encodage en deux passes n’est pas défini dans le profil.</span><span class="sxs-lookup"><span data-stu-id="9a752-118">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="9a752-119">Vous devez configurer le writer pour effectuer une étape de prétraitement avant d’écrire le flux.</span><span class="sxs-lookup"><span data-stu-id="9a752-119">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="9a752-120">Pour plus d’informations sur l’utilisation de l’encodage en deux passes, consultez [utilisation de l’encodage Two-Pass](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="9a752-120">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="9a752-121">Pour configurer un flux dans un profil à encoder avec un VBR non restreint, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="9a752-121">To configure a stream in a profile to be encoded with unconstrained VBR, perform the following steps:</span></span>

1.  <span data-ttu-id="9a752-122">Créez un objet de gestionnaire de profils en appelant la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="9a752-122">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="9a752-123">Ouvrez un profil existant auquel vous souhaitez ajouter la prise en charge VBR.</span><span class="sxs-lookup"><span data-stu-id="9a752-123">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="9a752-124">Pour plus d’informations sur l’ouverture des profils, consultez [utilisation des profils](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="9a752-124">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="9a752-125">Récupérez un objet de configuration de flux pour le flux que vous souhaitez utiliser en appelant [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile :: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="9a752-125">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="9a752-126">Obtenir un pointeur vers l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) de l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="9a752-126">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="9a752-127">Activez le codage VBR pour le flux en appelant [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) pour la propriété **g \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="9a752-127">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="9a752-128">Affectez aux paramètres **g \_ wszVBRBitrateMax** et **g \_ WszVBRBufferWindowMax** la valeur zéro avec **IWMPropertyVault :: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="9a752-128">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
7.  <span data-ttu-id="9a752-129">Enregistrez les modifications apportées au flux en appelant [**IWMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="9a752-129">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="9a752-130">Enregistrez le profil ou transmettez-le à l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="9a752-130">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="9a752-131">Configurez l’enregistreur pour effectuer une passe de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="9a752-131">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a752-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a752-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a752-133">**Configuration de flux VBR**</span><span class="sxs-lookup"><span data-stu-id="9a752-133">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




