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
# <a name="saving-profiles"></a>Enregistrement des profils

Vous pouvez utiliser la méthode [**IWMProfileManager :: saveprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) pour enregistrer le contenu d’un objet de profil dans une chaîne au format XML. Aucune méthode n’est fournie pour stocker la chaîne de profil dans un fichier ; vous pouvez utiliser les routines d’e/s de fichier de votre choix.

> [!Note]  
> Vous ne devez jamais modifier la chaîne de profil écrite dans un fichier. Toutes les modifications que vous souhaitez apporter à un profil doivent être effectuées par programme. La modification de valeurs dans un fichier. prx peut entraîner des résultats imprévisibles.

 

L’exemple suivant est une fonction permettant d’enregistrer un profil dans un fichier à l’aide d’e/s de fichier de style C standard. Pour compiler une application qui utilise cet exemple, vous devez inclure stdio. h dans votre projet.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 




