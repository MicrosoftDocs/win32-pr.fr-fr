---
description: L’interface IHWEventHandler peut être inscrite dans la table ROT (Running Object Table) afin que les applications en cours d’exécution aient accès aux événements de lecture automatique.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Guide pratique pour utiliser des événements de lecture automatique dans des applications en cours d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab30fa020b5501f8832a5b350ad409934ecbb4258d75adf147e908c699516474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714815"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a>Guide pratique pour utiliser des événements de lecture automatique dans des applications en cours d’exécution

L’interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) peut être inscrite dans la table ROT (Running Object Table) afin que les applications en cours d’exécution aient accès aux événements de lecture automatique.

Les instructions suivantes décrivent comment utiliser des événements de lecture automatique dans des applications en cours d’exécution.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Créez un nouveau composant qui implémente l’interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .

### <a name="step-2"></a>Étape 2 :

Initialisez le nouveau composant avec la valeur InitCmdLine à partir de l’entrée du gestionnaire particulier sous la clé des **gestionnaires** .

Cette étape est requise, car la lecture automatique n’appelle pas la méthode Initialize.

### <a name="step-3"></a>Étape 3 :

Appelez la fonction [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) pour obtenir un moniker qui représente votre composant et le gestionnaire d’événements que vous souhaitez appeler.

### <a name="step-4"></a>Étape 4 :

Utilisez le paramètre *ppmoniker* pour inscrire votre composant dans la table ROT.

## <a name="remarks"></a>Remarques

> [!Note]  
> [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut poser des risques de sécurité. Reportez-vous à la documentation de **LoadLibrary** pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Windows.

```cpp
typedef HRESULT (*CREATEHARDWAREEVENTMONIKER)(REFCLSID clsid, LPCWSTR pszEventHandler, IMoniker **ppmoniker);

HRESULT RegisterComponent(IUnknown* punk, DWORD* dpwToken)
{
    HRESULT hr = E_FAIL;
    HINSTANCE hinstShSvcs = LoadLibrary(TEXT("shsvcs.dll"));
    
    if (hinstShSvcs)
    {   
        CREATEHARDWAREEVENTMONIKER fct = (CREATEHARDWAREEVENTMONIKER)GetProcAddress(hinstShSvcs, "CreateHardwareEventMoniker");
        if (fct)
        {
            IMoniker* pmoniker;
            
            hr = fct(CLSID_App, TEXT("VideoCameraArrival"), &pmoniker);

            if (SUCCEEDED(hr))
            {
                IRunningObjectTable *prot;
                    
                if (SUCCEEDED(GetRunningObjectTable(0, &prot)))
                {
                    hr = prot->Register(ROTFLAGS_ALLOWANYCLIENT | ROTFLAGS_REGISTRATIONKEEPSALIVE, punk, pmoniker, &_dwRegisterROT);
                    prot->Release();
                }
                pmoniker->Release();
            }
            CoRegisterClassObject(CLSID_App, static_cast<IClassFactory *>(this), CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE, &_dwRegisterClass;
        }
        FreeLibrary(hinstShSvcs);
    }
    return hr;
}
```

L’appel à [**IRunningObjectTable :: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requiert que le composant ait les informations **AppID** suivantes dans le registre.

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="related-topics"></a>Rubriques connexes

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[**CreateHardwareEventMoniker**](createhardwareeventmoniker.md)
