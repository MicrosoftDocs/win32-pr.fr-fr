---
title: Pour charger un profil système
description: Pour charger un profil système
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- profils, système
- profils système, chargement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e745cb2fed32d650a22febef827ed7662f4448
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381512"
---
# <a name="to-load-a-system-profile"></a><span data-ttu-id="03b5b-105">Pour charger un profil système</span><span class="sxs-lookup"><span data-stu-id="03b5b-105">To Load a System Profile</span></span>

<span data-ttu-id="03b5b-106">Pour apporter des modifications à un profil système, vous devez le charger dans un objet de profil.</span><span class="sxs-lookup"><span data-stu-id="03b5b-106">To make changes to a system profile, you must load it into a profile object.</span></span> <span data-ttu-id="03b5b-107">Le gestionnaire de profils fournit deux options pour le chargement des profils système : par identificateur et par index.</span><span class="sxs-lookup"><span data-stu-id="03b5b-107">The profile manager provides two options for loading system profiles: by identifier, and by index.</span></span>

<span data-ttu-id="03b5b-108">Un identificateur de profil système est une valeur GUID affectée au profil système lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="03b5b-108">A system profile identifier is a GUID value assigned to the system profile when it was created.</span></span> <span data-ttu-id="03b5b-109">Pour obtenir la liste des constantes GUID associées aux profils système de la version 8, consultez [profils système](system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="03b5b-109">For a list of the GUID constants associated with the version 8 system profiles, see [System Profiles](system-profiles.md).</span></span> <span data-ttu-id="03b5b-110">Vous pouvez trouver les constantes GUID pour les versions précédentes dans le fichier d’en-tête WMSysPrf. h.</span><span class="sxs-lookup"><span data-stu-id="03b5b-110">You can find the GUID constants for previous versions in the header file WMSysPrf.h.</span></span> <span data-ttu-id="03b5b-111">Pour plus d’informations à ce sujet et sur les autres fichiers d’en-tête inclus dans le kit de développement logiciel (SDK) Windows Media format, consultez [fichiers de bibliothèque et paramètres du compilateur](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="03b5b-111">For more information about this and other header files included with the Windows Media Format SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

<span data-ttu-id="03b5b-112">L’exemple de code suivant montre comment charger un profil système à l’aide de l’identificateur de profil système.</span><span class="sxs-lookup"><span data-stu-id="03b5b-112">The following example code demonstrates how to load a system profile using the system profile identifier.</span></span> <span data-ttu-id="03b5b-113">Pour que ce code fonctionne, vous devez inclure WMSysPrf. h et stdio. h.</span><span class="sxs-lookup"><span data-stu-id="03b5b-113">For this code to work, you must include WMSysPrf.h and stdio.h.</span></span> <span data-ttu-id="03b5b-114">Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="03b5b-114">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



<span data-ttu-id="03b5b-115">Si vous ne connaissez pas le profil que vous souhaitez utiliser, vous pouvez effectuer une itération dans tous les profils système d’une version particulière à l’aide des méthodes [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) et [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) de l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="03b5b-115">If you do not know which profile you want to use, you can iterate through all of the system profiles of a particular version using the [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="03b5b-116">Ces méthodes traitent uniquement une version des profils système à la fois.</span><span class="sxs-lookup"><span data-stu-id="03b5b-116">These methods only deal with one version of the system profiles at a time.</span></span> <span data-ttu-id="03b5b-117">Pour plus d’informations sur la modification de la version du profil système, consultez [pour modifier les versions de profil système](to-change-system-profile-versions.md).</span><span class="sxs-lookup"><span data-stu-id="03b5b-117">For more information about changing the system profile version, see [To Change System Profile Versions](to-change-system-profile-versions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03b5b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03b5b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03b5b-119">**Utilisation des profils système**</span><span class="sxs-lookup"><span data-stu-id="03b5b-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




