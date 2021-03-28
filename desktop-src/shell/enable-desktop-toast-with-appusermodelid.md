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
ms.openlocfilehash: bd02a0ec6512aa7637f0d6b2b281e1b862e61d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972799"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a><span data-ttu-id="23ac0-103">Guide pratique pour activer les notifications toast de bureau via un AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="23ac0-103">How to enable desktop toast notifications through an AppUserModelID</span></span>

<span data-ttu-id="23ac0-104">Cette rubrique vous montre comment créer un raccourci pour votre application, lui assigner une valeur [AppUserModelID](appids.md)et l’installer dans l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="23ac0-104">This topic shows you how to create a shortcut for your app, assign it an [AppUserModelID](appids.md), and install it in the Start screen.</span></span> <span data-ttu-id="23ac0-105">Nous vous recommandons vivement de le faire dans le Windows Installer plutôt que dans le code de votre application.</span><span class="sxs-lookup"><span data-stu-id="23ac0-105">We strongly recommend that you do this in the Windows Installer rather than in your app's code.</span></span> <span data-ttu-id="23ac0-106">Si vous ne disposez pas d’un raccourci valide sur l’écran d’accueil ou dans **tous les programmes**, vous ne pouvez pas déclencher une notification toast à partir d’une application de bureau.</span><span class="sxs-lookup"><span data-stu-id="23ac0-106">Without a valid shortcut installed in the Start screen or in **All Programs**, you cannot raise a toast notification from a desktop app.</span></span>

> [!Note]  
> <span data-ttu-id="23ac0-107">Les exemples de méthodes utilisés dans cette rubrique sont tirés de l' [exemple de Toast de bureau](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span><span class="sxs-lookup"><span data-stu-id="23ac0-107">The example methods used in this topic are taken from the [Desktop toast sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="23ac0-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="23ac0-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="23ac0-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="23ac0-109">Technologies</span></span>

-   <span data-ttu-id="23ac0-110">COM</span><span class="sxs-lookup"><span data-stu-id="23ac0-110">COM</span></span>

### <a name="prerequisites"></a><span data-ttu-id="23ac0-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="23ac0-111">Prerequisites</span></span>

-   <span data-ttu-id="23ac0-112">Bibliothèques</span><span class="sxs-lookup"><span data-stu-id="23ac0-112">Libraries</span></span>
    -   <span data-ttu-id="23ac0-113">C++ : Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="23ac0-113">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="23ac0-114">C \# : Windows. Winmd</span><span class="sxs-lookup"><span data-stu-id="23ac0-114">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="23ac0-115">C \# : Pack de code d’API Windows pour Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="23ac0-115">C\#: Windows API Code Pack for Microsoft .NET Framework</span></span>
-   <span data-ttu-id="23ac0-116">Une version de Microsoft Visual Studio qui prend en charge au moins Windows 8</span><span class="sxs-lookup"><span data-stu-id="23ac0-116">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="23ac0-117">Instructions</span><span class="sxs-lookup"><span data-stu-id="23ac0-117">Instructions</span></span>

### <a name="step-1-prepare-the-shortcut-to-be-created"></a><span data-ttu-id="23ac0-118">Étape 1 : préparer le raccourci à créer</span><span class="sxs-lookup"><span data-stu-id="23ac0-118">Step 1: Prepare the shortcut to be created</span></span>

<span data-ttu-id="23ac0-119">Cet exemple détermine d’abord le chemin d’accès du dossier de données d’application de l’utilisateur via la fonction [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) .</span><span class="sxs-lookup"><span data-stu-id="23ac0-119">This example first determines the path of the user's app data folder through the [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) function.</span></span> <span data-ttu-id="23ac0-120">Il compose ensuite le chemin d’accès complet au raccourci, détermine qu’un raccourci de ce nom n’existe pas déjà à cet emplacement et transmet ces informations à une autre méthode qui crée et installe le raccourci.</span><span class="sxs-lookup"><span data-stu-id="23ac0-120">It then composes the full path to the shortcut, determines that a shortcut of that name does not already exist at that location, and passes that information to another method which creates and installs the shortcut.</span></span>

<span data-ttu-id="23ac0-121">Notez que le raccourci peut être déployé par utilisateur ou par application.</span><span class="sxs-lookup"><span data-stu-id="23ac0-121">Note that the shortcut can be deployed per-user or per-app.</span></span>


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



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a><span data-ttu-id="23ac0-122">Étape 2 : créer le raccourci et l’installer dans l’écran d’accueil</span><span class="sxs-lookup"><span data-stu-id="23ac0-122">Step 2: Create the shortcut and install it in the Start screen</span></span>

<span data-ttu-id="23ac0-123">Cet exemple récupère également la Banque de propriétés du raccourci et définit la propriété [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) requise à partir d’une variable précédemment définie, `AppID` .</span><span class="sxs-lookup"><span data-stu-id="23ac0-123">This example also retrieves the shortcut's property store and sets the required [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property from a previously defined variable, `AppID`.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="23ac0-124">Notes</span><span class="sxs-lookup"><span data-stu-id="23ac0-124">Remarks</span></span>

<span data-ttu-id="23ac0-125">Comme alternative à l’approche illustrée dans cette rubrique, vous pouvez utiliser une infrastructure telle que le Windows Installer XML (WiX) pour générer le raccourci et le déployer dans le cadre du Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="23ac0-125">As an alternative to the approach shown in this topic, you can use a framework such as the Windows Installer XML (WiX) to generate the shortcut and deploy it as part of the Windows Installer.</span></span> <span data-ttu-id="23ac0-126">Dans ce cas, ce code doit être inclus dans le MSI plutôt que dans le code de l’application.</span><span class="sxs-lookup"><span data-stu-id="23ac0-126">In that case, this code should be included in the MSI rather than in the app's code.</span></span> <span data-ttu-id="23ac0-127">Pour plus d’informations, consultez l’exemple de fichier de configuration WiX inclus avec l’exemple [envoi de notifications toast à partir d’applications de bureau](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) .</span><span class="sxs-lookup"><span data-stu-id="23ac0-127">For more information, see the sample WiX configuration file included with the [Sending toast notifications from desktop apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23ac0-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23ac0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23ac0-129">Démarrage rapide : envoi d’une notification toast à partir du Bureau</span><span class="sxs-lookup"><span data-stu-id="23ac0-129">Quickstart: Sending a toast notification from the desktop</span></span>](quickstart-sending-desktop-toast.md)
</dt> <dt>

<span data-ttu-id="23ac0-130">[Exemple d’envoi de notifications toast à partir d’applications de bureau](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="23ac0-130">[Sending toast notifications from desktop apps sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span></span>
</dt> <dt>

[<span data-ttu-id="23ac0-131">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="23ac0-131">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> <dt>

<span data-ttu-id="23ac0-132">[Comment : installer les outils Windows Installer XML (WiX)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="23ac0-132">[How to: Install the Windows Installer XML (WiX) Tools](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="23ac0-133">Schéma de Toast XML</span><span class="sxs-lookup"><span data-stu-id="23ac0-133">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="23ac0-134">[Présentation des notifications Toast](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="23ac0-134">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="23ac0-135">[Démarrage rapide : envoi d’une notification Toast](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="23ac0-135">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="23ac0-136">[Démarrage rapide : envoi d’une notification push Toast](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="23ac0-136">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="23ac0-137">Instructions et liste de vérification pour les notifications Toast</span><span class="sxs-lookup"><span data-stu-id="23ac0-137">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[<span data-ttu-id="23ac0-138">Comment ajouter des images à un modèle de Toast</span><span class="sxs-lookup"><span data-stu-id="23ac0-138">How to add images to a toast template</span></span>](/previous-versions/windows/)
</dt> <dt>

[<span data-ttu-id="23ac0-139">Comment vérifier les paramètres de notification Toast</span><span class="sxs-lookup"><span data-stu-id="23ac0-139">How to check toast notification settings</span></span>](/previous-versions/windows/)
</dt> <dt>

<span data-ttu-id="23ac0-140">[Comment choisir et utiliser un modèle de Toast](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="23ac0-140">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="23ac0-141">[Comment gérer l’activation à partir d’une notification Toast](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="23ac0-141">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="23ac0-142">[Comment s’abonner aux notifications Toast](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="23ac0-142">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="23ac0-143">[Choix d’un modèle de Toast](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="23ac0-143">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="23ac0-144">[Options audio Toast](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="23ac0-144">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
