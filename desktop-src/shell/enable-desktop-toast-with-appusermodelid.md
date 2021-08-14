---
description: Cette rubrique vous montre comment créer un raccourci pour votre application, lui assigner une valeur AppUserModelID et l’installer dans l’écran d’accueil.
title: Guide pratique pour activer les notifications toast de bureau via un AppUserModelID
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 517c2b72e830c00b105048adc63923291f896cd5d0d77569c91b1aa12e034e60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459791"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a>Guide pratique pour activer les notifications toast de bureau via un AppUserModelID

Cette rubrique vous montre comment créer un raccourci pour votre application, lui assigner une valeur [AppUserModelID](appids.md)et l’installer dans l’écran d’accueil. nous vous recommandons vivement de le faire dans le Windows Installer plutôt que dans le code de votre application. Si vous ne disposez pas d’un raccourci valide sur l’écran d’accueil ou dans **tous les programmes**, vous ne pouvez pas déclencher une notification toast à partir d’une application de bureau.

> [!Note]  
> Les exemples de méthodes utilisés dans cette rubrique sont tirés de l' [exemple de Toast de bureau](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).

 

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   COM

### <a name="prerequisites"></a>Prérequis

-   Bibliothèques
    -   C++ : Runtime. Object. lib
    -   C \# : Windows. Winmd
-   C \# : Windows Pack de Code d’API pour Microsoft .NET Framework
-   une version de Microsoft Visual Studio qui prend en charge au moins Windows 8

## <a name="instructions"></a>Instructions

### <a name="step-1-prepare-the-shortcut-to-be-created"></a>Étape 1 : préparer le raccourci à créer

Cet exemple détermine d’abord le chemin d’accès du dossier de données d’application de l’utilisateur via la fonction [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) . Il compose ensuite le chemin d’accès complet au raccourci, détermine qu’un raccourci de ce nom n’existe pas déjà à cet emplacement et transmet ces informations à une autre méthode qui crée et installe le raccourci.

Notez que le raccourci peut être déployé par utilisateur ou par application.


```C++
HRESULT DesktopToastsApp::TryCreateShortcut()
{
    wchar_t shortcutPath[MAX_PATH];
    DWORD charWritten = GetEnvironmentVariable(L"APPDATA", shortcutPath, MAX_PATH);
    HRESULT hr = charWritten > 0 ? S_OK : E_INVALIDARG;

    if (SUCCEEDED(hr))
    {
        errno_t concatError = wcscat_s(shortcutPath, ARRAYSIZE(shortcutPath), L"\\Microsoft\\Windows\\Start Menu\\Programs\\Desktop Toasts App.lnk");
 
        hr = concatError == 0 ? S_OK : E_INVALIDARG;
        if (SUCCEEDED(hr))
        {
            DWORD attributes = GetFileAttributes(shortcutPath);
            bool fileExists = attributes < 0xFFFFFFF;

            if (!fileExists)
            {
                hr = InstallShortcut(shortcutPath);  // See step 2.
            }
            else
            {
                hr = S_FALSE;
            }
        }
    }
    return hr;
}
```



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a>Étape 2 : créer le raccourci et l’installer dans l’écran d’accueil

Cet exemple récupère également la Banque de propriétés du raccourci et définit la propriété [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) requise à partir d’une variable précédemment définie, `AppID` .


```C++
HRESULT DesktopToastsApp::InstallShortcut(_In_z_ wchar_t *shortcutPath)
{
    wchar_t exePath[MAX_PATH];
    
    DWORD charWritten = GetModuleFileNameEx(GetCurrentProcess(), nullptr, exePath, ARRAYSIZE(exePath));

    HRESULT hr = charWritten > 0 ? S_OK : E_FAIL;
    
    if (SUCCEEDED(hr))
    {
        ComPtr<IShellLink> shellLink;
        hr = CoCreateInstance(CLSID_ShellLink, nullptr, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&shellLink));

        if (SUCCEEDED(hr))
        {
            hr = shellLink->SetPath(exePath);
            if (SUCCEEDED(hr))
            {
                hr = shellLink->SetArguments(L"");
                if (SUCCEEDED(hr))
                {
                    ComPtr<IPropertyStore> propertyStore;

                    hr = shellLink.As(&propertyStore);
                    if (SUCCEEDED(hr))
                    {
                        PROPVARIANT appIdPropVar;
                        hr = InitPropVariantFromString(AppId, &appIdPropVar);
                        if (SUCCEEDED(hr))
                        {
                            hr = propertyStore->SetValue(PKEY_AppUserModel_ID, appIdPropVar);
                            if (SUCCEEDED(hr))
                            {
                                hr = propertyStore->Commit();
                                if (SUCCEEDED(hr))
                                {
                                    ComPtr<IPersistFile> persistFile;
                                    hr = shellLink.As(&persistFile);
                                    if (SUCCEEDED(hr))
                                    {
                                        hr = persistFile->Save(shortcutPath, TRUE);
                                    }
                                }
                            }
                            PropVariantClear(&appIdPropVar);
                        }
                    }
                }
            }
        }
    }
    return hr;
}
```



## <a name="remarks"></a>Remarques

comme alternative à l’approche illustrée dans cette rubrique, vous pouvez utiliser une infrastructure telle que le Windows Installer XML (WiX) pour générer le raccourci et le déployer dans le cadre du Windows Installer. Dans ce cas, ce code doit être inclus dans le MSI plutôt que dans le code de l’application. Pour plus d’informations, consultez l’exemple de fichier de configuration WiX inclus avec l’exemple [envoi de notifications toast à partir d’applications de bureau](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Démarrage rapide : envoi d’une notification toast à partir du Bureau](quickstart-sending-desktop-toast.md)
</dt> <dt>

[Exemple d’envoi de notifications toast à partir d’applications de bureau](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))
</dt> <dt>

[ID de modèle d’utilisateur d’application (AppUserModelIDs)](appids.md)
</dt> <dt>

[comment : installer les outils Windows Installer XML (WiX)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))
</dt> <dt>

[Schéma de Toast XML](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Présentation des notifications Toast](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Démarrage rapide : envoi d’une notification Toast](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Démarrage rapide : envoi d’une notification push Toast](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Instructions et liste de vérification pour les notifications Toast](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Comment ajouter des images à un modèle de Toast](/previous-versions/windows/)
</dt> <dt>

[Comment vérifier les paramètres de notification Toast](/previous-versions/windows/)
</dt> <dt>

[Comment choisir et utiliser un modèle de Toast](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Comment gérer l’activation à partir d’une notification Toast](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Comment s’abonner aux notifications Toast](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Choix d’un modèle de Toast](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Options audio Toast](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
