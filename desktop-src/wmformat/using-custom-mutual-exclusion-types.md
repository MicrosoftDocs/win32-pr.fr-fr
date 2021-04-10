---
title: Utilisation de types d’exclusion mutuelles personnalisés
description: Utilisation de types d’exclusion mutuelles personnalisés
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- exclusion mutuelle, interface IWMMutualExclusion
- exclusion mutuelle, types personnalisés
- profils, types d’exclusion mutuelle personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101261"
---
# <a name="using-custom-mutual-exclusion-types"></a><span data-ttu-id="8f795-107">Utilisation de types d’exclusion mutuelles personnalisés</span><span class="sxs-lookup"><span data-stu-id="8f795-107">Using Custom Mutual Exclusion Types</span></span>

<span data-ttu-id="8f795-108">Vous pouvez utiliser des objets d’exclusion mutuelle dans un profil pour répondre aux besoins des scénarios personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8f795-108">You can use mutual exclusion objects in a profile to meet the needs of custom scenarios.</span></span> <span data-ttu-id="8f795-109">En passant la valeur GUID CLSID \_ WMMUTEX \_ inconnu à [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), vous indiquez à l’objet d’exclusion mutuelle que vous utilisez un scénario personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8f795-109">By passing the GUID value CLSID\_WMMUTEX\_Unknown to [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), you inform the mutual exclusion object that you are using a custom scenario.</span></span>

<span data-ttu-id="8f795-110">Vous devez contrôler manuellement la sélection de flux quand vous lisez un fichier avec une valeur d’exclusion mutuelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="8f795-110">You must manually control stream selection when you read a file with a custom mutual exclusion value.</span></span> <span data-ttu-id="8f795-111">L’objet lecteur utilise le premier flux que vous ajoutez à l’exclusion mutuelle comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f795-111">The reader object will use the first stream you add to the mutual exclusion as the default.</span></span>

<span data-ttu-id="8f795-112">Procédez comme suit pour créer un objet d’exclusion mutuelle personnalisée et l’ajouter à un profil :</span><span class="sxs-lookup"><span data-stu-id="8f795-112">Use the following steps to create a custom mutual exclusion object and add it to a profile:</span></span>

1.  <span data-ttu-id="8f795-113">Créez un gestionnaire de profils en appelant la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="8f795-113">Create a profile manager by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="8f795-114">Démarrez avec un profil existant, ou créez-en un entièrement nouveau.</span><span class="sxs-lookup"><span data-stu-id="8f795-114">Either start with an existing profile, or create an entirely new one.</span></span>
    -   <span data-ttu-id="8f795-115">Si vous utilisez un profil existant, appelez l’une des méthodes Load de l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="8f795-115">If you are using an existing profile, call one of the load methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="8f795-116">Passez ensuite à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="8f795-116">Then skip to step 4.</span></span>
    -   <span data-ttu-id="8f795-117">Si vous créez un profil entièrement nouveau, appelez [**IWMProfileManager :: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="8f795-117">If you are creating an entirely new profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span>
3.  <span data-ttu-id="8f795-118">Ajoutez des flux au nouveau profil en appelant [**IWMProfile :: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span><span class="sxs-lookup"><span data-stu-id="8f795-118">Add streams to the new profile by calling [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span></span> <span data-ttu-id="8f795-119">Configurez les flux en fonction des besoins à l’aide des méthodes de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="8f795-119">Configure the streams as needed using the methods of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span> <span data-ttu-id="8f795-120">Vous pouvez également appeler **QueryInterface** pour accéder à d’autres interfaces dans l’objet de configuration Stream.</span><span class="sxs-lookup"><span data-stu-id="8f795-120">You can also call **QueryInterface** to access other interfaces in the stream configuration object.</span></span>

    <span data-ttu-id="8f795-121">**CreateNewStream** crée uniquement un objet de configuration de flux et n’affecte pas le profil.</span><span class="sxs-lookup"><span data-stu-id="8f795-121">**CreateNewStream** creates only a stream configuration object, and does not affect the profile.</span></span> <span data-ttu-id="8f795-122">Une fois qu’un flux est correctement configuré, vous devez appeler [**IWMProfile :: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) pour ajouter le flux au profil.</span><span class="sxs-lookup"><span data-stu-id="8f795-122">After a stream is configured properly, you must call [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add the stream to the profile.</span></span>

4.  <span data-ttu-id="8f795-123">Créez un objet d’exclusion mutuelle en appelant [**IWMProfile :: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="8f795-123">Create a mutual exclusion object by calling [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span></span>
5.  <span data-ttu-id="8f795-124">Ajoutez les flux souhaités à l’objet exclusion mutuelle en appelant [**IWMStreamList :: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponible directement à partir de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), qui hérite de [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span><span class="sxs-lookup"><span data-stu-id="8f795-124">Add the desired streams to the mutual exclusion object by calling [**IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (available directly from [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), which inherits from [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span></span>
6.  <span data-ttu-id="8f795-125">Définissez le type d’exclusion mutuelle sur personnalisé en appelant [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="8f795-125">Set the type of mutual exclusion to custom by calling [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span> <span data-ttu-id="8f795-126">Transmettez le CLSID \_ WMMUTEX \_ Unknown comme GUID de type.</span><span class="sxs-lookup"><span data-stu-id="8f795-126">Pass the CLSID\_WMMUTEX\_Unknown as the type GUID.</span></span>
7.  <span data-ttu-id="8f795-127">Ajoutez l’objet exclusion mutuelle configurée au profil en appelant [**IWMProfile :: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="8f795-127">Add the configured mutual exclusion object to the profile by calling [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f795-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f795-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f795-129">**Interface IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="8f795-129">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="8f795-130">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="8f795-130">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="8f795-131">**Interface IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="8f795-131">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="8f795-132">**Interface IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="8f795-132">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="8f795-133">**Interface IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="8f795-133">**IWMStreamList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[<span data-ttu-id="8f795-134">**Utilisation de l’exclusion mutuelle**</span><span class="sxs-lookup"><span data-stu-id="8f795-134">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="8f795-135">**WMCreateProfileManager**</span><span class="sxs-lookup"><span data-stu-id="8f795-135">**WMCreateProfileManager**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




