---
title: Pour configurer le VBR restreint
description: Pour configurer le VBR restreint
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- flux, configuration des flux VBR
- flux, débit binaire variable (VBR)
- Vitesse de transmission variable (VBR), flux
- VBR (vitesse de transmission variable), flux
- flux, configuration du VBR restreint
- Vitesse de transmission variable (VBR), configuration avec restriction
- VBR (vitesse de transmission variable), configuration avec restriction
- profils, configuration du VBR restreint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030928"
---
# <a name="to-configure-constrained-vbr"></a><span data-ttu-id="5a03a-111">Pour configurer le VBR restreint</span><span class="sxs-lookup"><span data-stu-id="5a03a-111">To Configure Constrained VBR</span></span>

<span data-ttu-id="5a03a-112">Vous pouvez utiliser l’encodage VBR (variable bit rate) sur un flux pour spécifier un débit binaire moyen qui sera maintenu dans le contenu encodé.</span><span class="sxs-lookup"><span data-stu-id="5a03a-112">You can use constrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="5a03a-113">Vous spécifiez également la vitesse de transmission maximale du flux et la fenêtre de mémoire tampon maximale requise.</span><span class="sxs-lookup"><span data-stu-id="5a03a-113">You also specify the maximum bit rate of the stream and the maximum required buffer window.</span></span>

<span data-ttu-id="5a03a-114">Vous ne pouvez pas savoir quel est le taux de bits moyen pour un flux VBR restreint avant l’encodage, mais vous pouvez utiliser une estimation approximative.</span><span class="sxs-lookup"><span data-stu-id="5a03a-114">You cannot know what the average bit rate will be for a constrained VBR stream before encoding, but you can use a rough estimate.</span></span> <span data-ttu-id="5a03a-115">En règle générale, la vitesse de transmission maximale que vous spécifiez se termine deux à trois fois la vitesse de transmission moyenne.</span><span class="sxs-lookup"><span data-stu-id="5a03a-115">As a general rule, the maximum bit rate you specify will end up being two to three times the average bit rate.</span></span>

<span data-ttu-id="5a03a-116">Le VBR restreint doit être utilisé conjointement avec l’encodage en deux passes.</span><span class="sxs-lookup"><span data-stu-id="5a03a-116">Constrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="5a03a-117">L’encodage en deux passes n’est pas défini dans le profil.</span><span class="sxs-lookup"><span data-stu-id="5a03a-117">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="5a03a-118">Vous devez configurer le writer pour effectuer une étape de prétraitement avant d’écrire le flux.</span><span class="sxs-lookup"><span data-stu-id="5a03a-118">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="5a03a-119">Pour plus d’informations sur l’utilisation de l’encodage en deux passes, consultez [utilisation de l’encodage Two-Pass](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="5a03a-119">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="5a03a-120">Pour configurer un flux dans un profil afin d’utiliser l’encodage VBR restreint, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="5a03a-120">To configure a stream in a profile to use constrained VBR encoding, perform the following steps.</span></span>

1.  <span data-ttu-id="5a03a-121">Créez un objet de gestionnaire de profils en appelant la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="5a03a-121">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="5a03a-122">Ouvrez un profil existant auquel vous souhaitez ajouter la prise en charge VBR.</span><span class="sxs-lookup"><span data-stu-id="5a03a-122">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="5a03a-123">Pour plus d’informations sur l’ouverture des profils, consultez [utilisation des profils](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="5a03a-123">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="5a03a-124">Récupérez un objet de configuration de flux pour le flux que vous souhaitez utiliser en appelant [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) ou [**IWMProfile :: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="5a03a-124">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="5a03a-125">Obtenir un pointeur vers l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) de l’objet de configuration de flux en appelant **IWMStreamConfig :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="5a03a-125">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="5a03a-126">Activez le codage VBR pour le flux en appelant [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) pour la propriété **g \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="5a03a-126">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="5a03a-127">Utilisez des appels à **IWMPropertyVault :: SetProperty** pour définir les valeurs maximales souhaitées pour les propriétés **g \_ wszVBRBitrateMax** et **g \_ wszVBRBufferWindowMax** .</span><span class="sxs-lookup"><span data-stu-id="5a03a-127">Use calls to **IWMPropertyVault::SetProperty** to set the desired maximum values for the **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** properties.</span></span>
7.  <span data-ttu-id="5a03a-128">Enregistrez les modifications apportées au flux en appelant [**IWMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="5a03a-128">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="5a03a-129">Enregistrez le profil ou transmettez-le à l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="5a03a-129">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="5a03a-130">Configurez l’enregistreur pour effectuer une passe de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="5a03a-130">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a03a-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a03a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a03a-132">**Configuration de flux VBR**</span><span class="sxs-lookup"><span data-stu-id="5a03a-132">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




