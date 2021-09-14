---
title: Modification du code généré par l’Assistant
description: Modification du code généré par l’Assistant
ms.assetid: 391a7773-c3e2-499a-bb63-e5934537d963
keywords:
- Lecteur Windows Media Périphériques mobiles, plug-ins
- Lecteur Windows Media Périphériques mobiles, plug-ins d’interface utilisateur
- Lecteur Windows Media Plug-ins mobiles
- plug-ins, interface utilisateur
- plug-ins, Lecteur Windows Media Mobile
- plug-ins d’interface utilisateur, Lecteur Windows Media Mobile
- plug-ins d’interface utilisateur, Lecteur Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83bda7cb265d0c2e039ada6d9d827c6da3faf63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292570"
---
# <a name="modifying-wizard-generated-code"></a>Modification du code généré par l’Assistant

il y a plusieurs endroits dans le code de plug-in généré par l’assistant que vous devez modifier pour que votre plug-in fonctionne avec Lecteur Windows Media 10 Mobile. Le code que vous devez modifier est gras dans les exemples suivants.

## <a name="changes-to-wmpplugh"></a>Modifications apportées à wmpplug. h

les méthodes ansi ne sont pas prises en charge sur les appareils exécutant Windows CE. vous devez donc modifier la méthode ansi suivante générée par l’assistant dans wmpplug. h :


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageA( "WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



Modifiez-le comme indiqué dans le code suivant afin qu’il devienne une méthode Unicode :


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageW( L"WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



## <a name="changes-to-networkpluginh"></a>Modifications apportées à NetworkPlugin. h

Recherchez le code suivant dans NetworkPlugin. h :


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    COM_INTERFACE(IWMPPluginUI)
END_COM_MAP()
```



Modifiez le code afin qu’il ressemble à ceci :


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    
COM_INTERFACE_ENTRY_IID(__uuidof(IWMPPluginUI), IWMPPluginUI)
END_COM_MAP()
```



## <a name="changes-to-networkplugindllcpp"></a>Modifications apportées à NetworkPlugindll. cpp

Recherchez la fonction **DllMain** dans NetworkPlugindll. cpp :


```C++
extern "C" BOOL WINAPI DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, hInstance);
        DisableThreadLibraryCalls(hInstance);
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



Modifiez le code afin qu’il ressemble à ceci :


```C++
extern "C" BOOL WINAPI DllMain(HANDLE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, (HINSTANCE)hInstance);
#ifndef UNDER_CE
        DisableThreadLibraryCalls((HINSTANCE)hInstance);
#endif
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



## <a name="changes-to-networkplugincpp"></a>Modifications apportées à NetworkPlugin. cpp

Recherchez le code suivant dans NetworkPlugin. cpp :


```C++
hr = m_spCore->QueryInterface(&spConnectionContainer);
```



Modifiez le code afin qu’il ressemble à ceci :


```C++
hr = m_spCore->QueryInterface(__uuidof(IConnectionPointContainer), (void**)&spConnectionContainer);
```



## <a name="change-the-threading-model"></a>Modifier le modèle de thread

contrairement à atl pour Windows, atl pour Windows CE ne prend pas en charge le modèle de thread cloisonné car le modèle cloisonné requiert plus de ressources mémoire que les modèles de thread unique et de thread libre. Par conséquent, vous devez rechercher toutes les instances de cloisonnement Threading dans StdAfx. h et NetworkPlugin. RGS et les modifier pour indiquer le Threading libre.

en outre, vous pouvez uniquement appeler le contrôle Mobile Lecteur Windows Media 10 à partir du thread sur lequel il a été créé.

## <a name="build-and-test-the-project"></a>Générez et testez le Project

Après avoir apporté ces modifications décrites ici, vous pouvez générer votre projet pour vérifier qu’il est compilé avant d’ajouter du code personnalisé.

1.  affectez à la configuration de projet active la version Debug win32 (WCE armv4) ou win32 (WCE armv4).
2.  définissez la plateforme active sur Pocket PC 2003.
3.  Cliquez sur l’élément de menu **générer** , puis sélectionnez **générer NetworkPlugin.dll**. Elle doit être compilée, téléchargée et inscrite sur votre appareil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**création d’un Plug-in d’Interface utilisateur pour Lecteur Windows Media 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> </dl>

 

 




