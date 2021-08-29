---
title: Exploration d’un appareil
description: Exploration d’un appareil
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Gestionnaire de périphériques multimédia, exploration des appareils
- Gestionnaire de périphériques, exploration des appareils
- Guide de programmation, exploration des appareils
- applications de bureau, exploration des appareils
- création d’applications Windows Media Gestionnaire de périphériques, exploration des appareils
- exploration des appareils
- stockages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cfdefbf5d71563cae2bb5b78383cfe0582e0af04e447e78166d0e80fda536d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957579"
---
# <a name="exploring-a-device"></a>Exploration d’un appareil

L’exploration d’un appareil est similaire à l’exploration d’un lecteur de disque. Tous les objets sur un appareil sont appelés « *stockages*». Un stockage peut être un fichier, un dossier ou un objet abstrait (par exemple, une sélection) sur l’appareil. Vous devez examiner les attributs et les métadonnées d’un stockage (si pris en charge) pour comprendre le type de stockage. Les stockages sont organisés de manière hiérarchique sur l’appareil. chaque stockage a exactement un parent et tous les stockages sont finalement décroissants d’un stockage d’appareil racine unique, généralement nommé « \\ ».

Les étapes suivantes décrivent comment explorer un appareil :

1.  Obtenir l’interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) d’un appareil, comme décrit dans la section [énumération des appareils](enumerating-devices.md).
2.  Appelez [**IWMDMDevice :: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) pour récupérer une interface [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) . Cette interface est utilisée pour récupérer tous les objets enfants du stockage qui retourne cette interface. Lors de l’obtention de cette interface à partir de l’appareil, comme nous sommes ici, il ne contiendra qu’un seul stockage : le stockage de l’appareil racine.
3.  Appelez [**IWMDMEnumStorage :: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) avec un nombre de 1 pour récupérer l’interface [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) pour le stockage de l’appareil racine. (Vous ne pouvez pas demander plus d’un enfant de l’appareil.)
4.  Examinez tous les stockages sur l’appareil en appelant de manière récursive [**IWMDMStorage :: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) , puis **IWMDMEnumStorage :: Next** pour obtenir les enfants d’un stockage. Pour voir si un stockage a des enfants pour éviter les appels à **EnumStorage** et **Next**, vous pouvez appeler [**IWMDMStorage :: GETATTRIBUTES**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) pour rechercher les indicateurs WMDM \_ Storage \_ attr \_ contient des \_ fichiers ou WMDM \_ Storage \_ attr contient des \_ \_ dossiers. Pour plus d’informations sur la façon d’obtenir les propriétés d’un stockage, consultez [obtention et définition des métadonnées et des attributs](getting-and-setting-metadata-and-attributes.md) et [obtention et définition des métadonnées et des attributs dans l’application](getting-and-setting-metadata-and-attributes-in-the-application.md).

Windows Media Gestionnaire de périphériques n’expose pas un ensemble standard de dossiers pour stocker les éléments multimédias d’un type spécifique (par exemple, un dossier « Mes playlists » pour les playlists). Chaque appareil possède un système de fichiers unique, et vous devez choisir un emplacement approprié pour rechercher ou envoyer un fichier spécifique.

> [!Note]  
> Windows L’Explorateur peut afficher les dossiers virtuels qui n’existent pas réellement sur l’appareil. Les dossiers virtuels sont, par exemple, les dossiers « Media » et « Data » affichés pour les appareils MTP. ces dossiers sont créés par Windows pour simplifier les téléchargements pour les utilisateurs finaux. ils n’existent pas réellement sur l’appareil. Votre application ne doit pas dépendre de la recherche de ces types de dossiers généraux. à l’inverse, Windows Explorer peut ne pas afficher certains dossiers ou objets qui existent sur l’appareil (par exemple, les sélections).

 

L’exemple de code C++ suivant illustre l’exploration récursive d’un appareil. Il utilise deux fonctions :

-   ExploreDevice, une fonction de démarrage qui reçoit un pointeur d’appareil et obtient un pointeur vers l’énumérateur racine de cet appareil.
-   RecursiveExploreStorage, qui est appelé pour explorer un appareil de manière récursive.


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**création d’une Application de Gestionnaire de périphériques multimédia Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




