---
title: Enregistrement des profils
description: Enregistrement des profils
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows Media Format SDK, enregistrement des profils
- Windows Media Format SDK, enregistrement de profil
- profils, enregistrement
- profils, interface IWMProfileManager
- IWMProfileManager, enregistrement des profils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276b002f0b7f98de2e84f2c27a4f52bde25726bb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381482"
---
# <a name="saving-profiles"></a><span data-ttu-id="33fd6-108">Enregistrement des profils</span><span class="sxs-lookup"><span data-stu-id="33fd6-108">Saving Profiles</span></span>

<span data-ttu-id="33fd6-109">Vous pouvez utiliser la méthode [**IWMProfileManager :: saveprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) pour enregistrer le contenu d’un objet de profil dans une chaîne au format XML.</span><span class="sxs-lookup"><span data-stu-id="33fd6-109">You can use the [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) method to save the contents of a profile object to a string formatted with XML.</span></span> <span data-ttu-id="33fd6-110">Aucune méthode n’est fournie pour stocker la chaîne de profil dans un fichier ; vous pouvez utiliser les routines d’e/s de fichier de votre choix.</span><span class="sxs-lookup"><span data-stu-id="33fd6-110">No methods are provided to store the profile string to a file; you can use the file I/O routines of your choice.</span></span>

> [!Note]  
> <span data-ttu-id="33fd6-111">Vous ne devez jamais modifier la chaîne de profil écrite dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="33fd6-111">You should never alter the profile string written to a file.</span></span> <span data-ttu-id="33fd6-112">Toutes les modifications que vous souhaitez apporter à un profil doivent être effectuées par programme.</span><span class="sxs-lookup"><span data-stu-id="33fd6-112">Any changes you want to make to a profile should be made programmatically.</span></span> <span data-ttu-id="33fd6-113">La modification de valeurs dans un fichier. prx peut entraîner des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="33fd6-113">Changing values in a .prx file can cause unpredictable results.</span></span>

 

<span data-ttu-id="33fd6-114">L’exemple suivant est une fonction permettant d’enregistrer un profil dans un fichier à l’aide d’e/s de fichier de style C standard.</span><span class="sxs-lookup"><span data-stu-id="33fd6-114">The following example is a function to save a profile to a file using standard C-style file I/O.</span></span> <span data-ttu-id="33fd6-115">Pour compiler une application qui utilise cet exemple, vous devez inclure stdio. h dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="33fd6-115">To compile an application that uses this example, you must include stdio.h in your project.</span></span>


```C++
HRESULT ProfileToFile(IWMProfileManager* pProfileMgr, 
                      IWMProfile* pProfile)
{
    HRESULT hr = S_OK;

    FILE*   pFile;
    
    WCHAR*  pwszProfileString = NULL;
    DWORD   cchProfileString = 0;

    // Save the profile to a string.
    // First, retrieve the size of the string required.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  NULL, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not get the profile string size.");
        return hr;
    }

    // Allocate memory to hold the string.
    pwszProfileString = new WCHAR[cchProfileString];

    if(pwszProfileString == NULL)
    {
        printf("Could not allocate memory for the profile string.");
        return E_OUTOFMEMORY;
    }

    // Retrieve the string.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  pwszProfileString, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not save the profile string.");
        return hr;
    }

    // Create the output file.
    pFile = fopen("MyProfile.prx", "w");

    // Write the profile string to the file.
    fprintf(pFile, "%S\n", pwszProfileString);

    // Close the file.
    fclose(pFile);

    delete[] pwszProfileString;

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="33fd6-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33fd6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33fd6-117">**Utilisation des profils**</span><span class="sxs-lookup"><span data-stu-id="33fd6-117">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




