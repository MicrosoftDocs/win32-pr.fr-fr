---
title: Public et exemple de code
description: Cette rubrique décrit les groupes de développeurs pour lesquels l’interface d’analyse anti-programme malveillant est conçue.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 22cf1156a8fa0aedc212b2ab70e34b984d13470f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920583"
---
# <a name="developer-audience-and-sample-code"></a>Public et exemple de code

L’interface d’analyse anti-programme malveillant est conçue pour être utilisée par deux groupes de développeurs.

- Les développeurs d’applications qui souhaitent effectuer des demandes aux produits anti-programme malveillant à partir de leurs applications.
- Créateurs de logiciels anti-programmes malveillants tiers qui souhaitent que leurs produits offrent les meilleures fonctionnalités aux applications.

## <a name="application-developers"></a>Développeurs d’applications

AMSI est conçu en particulier pour combattre les « programmes malveillants en fichier ». les types d’applications qui peuvent tirer le meilleur parti de la technologie AMSI incluent les moteurs de script, les applications qui ont besoin de mémoires tampons pour être analysés avant de les utiliser, et les applications qui traitent les fichiers qui peuvent contenir du code exécutable non PE (par exemple, les macros Microsoft Word et Excel ou les documents PDF). Toutefois, l’utilité de la technologie AMSI n’est pas limitée à ces exemples.

Il existe deux façons d’interagir avec AMSI dans votre application.

- À l’aide des API Win32 AMSI. Voir [fonctions de l’interface d’analyse anti-programme malveillant (AMSI)](/windows/desktop/amsi/antimalware-scan-interface-functions).
- À l’aide des interfaces COM AMSI. Voir [interface **IAmsiStream**](/windows/desktop/api/amsi/nn-amsi-iamsistream).

Pour obtenir un exemple de code illustrant l’utilisation de AMSI dans votre application COM, consultez l' [exemple d’application IAmsiStream interface](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## <a name="third-party-creators-of-antimalware-products"></a>Créateurs de logiciels anti-programme malveillant tiers

En tant que créateur de produits anti-programme malveillant, vous pouvez choisir de créer et d’inscrire votre propre serveur COM in-process (une DLL) pour qu’il fonctionne en tant que fournisseur AMSI. Ce fournisseur AMSI doit implémenter l' [interface **IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)et doit s’exécuter in-process.

notez que, après Windows 10, la version 1709 (la mise à jour automne 2017 Creators), votre DLL de fournisseur AMSI peut ne pas fonctionner si cela dépend d’autres dll dans son chemin d’accès à charger en même temps. Pour empêcher le détournement de DLL, nous recommandons que votre DLL de fournisseur charge explicitement ses dépendances (avec un chemin d’accès complet) à l’aide d’appels [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) sécurisés, ou d’un équivalent. Nous vous recommandons de le faire au lieu de vous appuyer sur le comportement de recherche **LoadLibrary** .

La section ci-dessous montre comment inscrire votre fournisseur AMSI. Pour obtenir un exemple de code complet illustrant comment créer votre propre DLL de fournisseur AMSI, consultez l' [exemple d’application IAntimalwareProvider interface](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).

### <a name="register-your-provider-dll-with-amsi"></a>Inscrire votre DLL de fournisseur auprès de AMSI

pour commencer, vous devez vous assurer que ces clés de registre Windows existent.

- HKLM\SOFTWARE\Microsoft\AMSI\Providers
- HKLM\SOFTWARE\Classes\CLSID

Un fournisseur AMSI est un serveur COM in-process. Par conséquent, il doit s’inscrire auprès de COM. Les classes COM sont inscrites dans `HKLM\SOFTWARE\Classes\CLSID` .

Le code ci-dessous montre comment inscrire un fournisseur AMSI dont le GUID (pour cet exemple) est `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .

```cpp
#include <strsafe.h>
...
HRESULT SetKeyStringValue(_In_ HKEY key, _In_opt_ PCWSTR subkey, _In_opt_ PCWSTR valueName, _In_ PCWSTR stringValue)
{
    LONG status = RegSetKeyValue(key, subkey, valueName, REG_SZ, stringValue, (wcslen(stringValue) + 1) * sizeof(wchar_t));
    return HRESULT_FROM_WIN32(status);
}

STDAPI DllRegisterServer()
{
    wchar_t modulePath[MAX_PATH];
    if (GetModuleFileName(g_currentModule, modulePath, ARRAYSIZE(modulePath)) >= ARRAYSIZE(modulePath))
    {
        return E_UNEXPECTED;
    }

    // Create a standard COM registration for our CLSID.
    // The class must be registered as "Both" threading model,
    // and support multithreaded access.
    wchar_t clsidString[40];
    if (StringFromGUID2(__uuidof(SampleAmsiProvider), clsidString, ARRAYSIZE(clsidString)) == 0)
    {
        return E_UNEXPECTED;
    }

    wchar_t keyPath[200];
    HRESULT hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls\\InProcServer32", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, modulePath);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, L"ThreadingModel", L"Both");
    if (FAILED(hr)) return hr;

    // Register this CLSID as an anti-malware provider.
    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Microsoft\\AMSI\\Providers\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    return S_OK;
}
```

si votre DLL implémente la [fonction DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), comme l’illustre l’exemple ci-dessus, vous pouvez l’inscrire à l’aide de l’exécutable fourni par le Windows `regsvr32.exe` . À partir d’une invite de commandes avec élévation de privilèges, émettez une commande de ce formulaire.

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

Dans cet exemple, la commande crée les entrées suivantes.

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

&nbsp;&nbsp;&nbsp;&nbsp;**Valeurs    REG_SZ exemple d’implémentation de fournisseur AMSI**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**Valeurs    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ les deux**

En plus de l’inscription COM standard, vous devez également inscrire le fournisseur auprès de AMSI. Pour ce faire, ajoutez une entrée à la clé suivante.

**HKLM\SOFTWARE\Microsoft\AMSI\Providers**

Par exemple,

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**
