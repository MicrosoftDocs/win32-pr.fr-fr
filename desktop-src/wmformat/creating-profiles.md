---
title: Création de profils
description: Création de profils
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows Media Format SDK, profils
- profils, création
- profils, interface IWMProfileManager
- IWMProfileManager, création de profils
- profils, fonction WMCreateProfileManager
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030775"
---
# <a name="creating-profiles"></a><span data-ttu-id="cf33a-109">Création de profils</span><span class="sxs-lookup"><span data-stu-id="cf33a-109">Creating Profiles</span></span>

<span data-ttu-id="cf33a-110">Dans de nombreux cas, vous souhaiterez peut-être créer un profil vide pour configurer vos besoins.</span><span class="sxs-lookup"><span data-stu-id="cf33a-110">In many cases, you will want to create an empty profile to configure for your needs.</span></span> <span data-ttu-id="cf33a-111">Dans d’autres cas, il est plus facile de modifier un profil existant, comme un profil système.</span><span class="sxs-lookup"><span data-stu-id="cf33a-111">In other cases it is easier to edit an existing profile, like a system profile.</span></span> <span data-ttu-id="cf33a-112">Pour plus d’informations sur l’utilisation des profils système, consultez [utilisation des profils système](using-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="cf33a-112">For more information about using system profiles, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="cf33a-113">La création d’un profil vide, prêt à être configuré, nécessite un objet gestionnaire de profils.</span><span class="sxs-lookup"><span data-stu-id="cf33a-113">Creating an empty profile, ready for you to configure, requires a profile manager object.</span></span> <span data-ttu-id="cf33a-114">Pour obtenir l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) d’un objet de gestionnaire de profils, appelez la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="cf33a-114">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>

<span data-ttu-id="cf33a-115">Pour créer un profil vide, appelez [**IWMProfileManager :: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="cf33a-115">To create an empty profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span> <span data-ttu-id="cf33a-116">Lorsque vous créez un profil vide, la seule chose que vous spécifiez est la version du kit de développement logiciel (SDK) de format Windows Media avec laquelle le profil est conforme.</span><span class="sxs-lookup"><span data-stu-id="cf33a-116">When you create an empty profile, the only thing you specify is the version of the Windows Media Format SDK with which the profile complies.</span></span> <span data-ttu-id="cf33a-117">À moins que vous n’ayez besoin d’utiliser une version antérieure, vous devez toujours utiliser la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="cf33a-117">Unless you have a specific need to use a previous version, you should always use the latest version.</span></span> <span data-ttu-id="cf33a-118">La version dicte la structure du profil ; les versions précédentes ne prenaient pas en charge certaines propriétés.</span><span class="sxs-lookup"><span data-stu-id="cf33a-118">The version dictates the structure of the profile; previous versions did not support some properties.</span></span>

<span data-ttu-id="cf33a-119">L’exemple de code suivant montre comment créer un nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="cf33a-119">The following example code shows how to create a new profile.</span></span> <span data-ttu-id="cf33a-120">Pour compiler ce code dans votre application, incluez stdio. h.</span><span class="sxs-lookup"><span data-stu-id="cf33a-120">To compile this code in your application, include stdio.h.</span></span> <span data-ttu-id="cf33a-121">Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="cf33a-121">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="cf33a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cf33a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf33a-123">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="cf33a-123">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="cf33a-124">**Interface IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="cf33a-124">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="cf33a-125">**Utilisation des profils**</span><span class="sxs-lookup"><span data-stu-id="cf33a-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




