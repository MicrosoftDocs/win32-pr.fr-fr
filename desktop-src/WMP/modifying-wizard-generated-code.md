---
title: Modification du code généré par l’Assistant
description: Modification du code généré par l’Assistant
ms.assetid: 391a7773-c3e2-499a-bb63-e5934537d963
keywords:
- Windows Media Player Mobile, plug-ins
- Windows Media Player Mobile, plug-ins d’interface utilisateur
- Plug-ins Windows Media Player Mobile
- plug-ins, interface utilisateur
- plug-ins, Windows Media Player Mobile
- plug-ins d’interface utilisateur, Windows Media Player Mobile
- Plug-ins d’interface utilisateur, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83bda7cb265d0c2e039ada6d9d827c6da3faf63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106536876"
---
# <a name="modifying-wizard-generated-code"></a>Modification du code généré par l’Assistant

Il y a plusieurs endroits dans le code de plug-in généré par l’Assistant que vous devez modifier pour que votre plug-in fonctionne avec le lecteur Windows Media 10 mobile. Le code que vous devez modifier est gras dans les exemples suivants.

## <a name="changes-to-wmpplugh"></a>Modifications apportées à wmpplug. h

Les méthodes ANSI ne sont pas prises en charge sur les appareils exécutant Windows CE. vous devez donc modifier la méthode ANSI suivante générée par l’Assistant dans wmpplug. h :


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

Contrairement à ATL pour Windows, ATL pour Windows CE ne prend pas en charge le modèle de thread cloisonné car le modèle cloisonné requiert plus de ressources mémoire que les modèles de thread unique et de thread libre. Par conséquent, vous devez rechercher toutes les instances de cloisonnement Threading dans StdAfx. h et NetworkPlugin. RGS et les modifier pour indiquer le Threading libre.

En outre, vous pouvez uniquement appeler le contrôle mobile du lecteur Windows Media 10 à partir du thread sur lequel il a été créé.

## <a name="build-and-test-the-project"></a>Générer et tester le projet

Après avoir apporté ces modifications décrites ici, vous pouvez générer votre projet pour vérifier qu’il est compilé avant d’ajouter du code personnalisé.

1.  Définissez la configuration de projet active sur Win32 (WCE ARMV4) debug ou Win32 (WCE ARMV4) Release.
2.  Définissez la plateforme active sur Pocket PC 2003.
3.  Cliquez sur l’élément de menu **générer** , puis sélectionnez **générer NetworkPlugin.dll**. Elle doit être compilée, téléchargée et inscrite sur votre appareil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un plug-in d’interface utilisateur pour Windows Media Player 10 mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> </dl>

 

 




