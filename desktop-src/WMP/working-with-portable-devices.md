---
title: Utilisation d’appareils mobiles
description: Utilisation d’appareils mobiles
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Lecteur Windows Media, appareils mobiles
- Modèle objet du lecteur Windows Media, appareils mobiles
- modèle objet, appareils mobiles
- Contrôle ActiveX du lecteur Windows Media, appareils mobiles
- Contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile, appareils mobiles
- appareils mobiles, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311314"
---
# <a name="working-with-portable-devices"></a>Utilisation d’appareils mobiles

Cette section explique comment utiliser un contrôle ActiveX Windows Media Player distant pour travailler avec des appareils mobiles.

Les exemples de code de cette section utilisent des classes Active Template Library (ATL), telles que **CComPtr**.

## <a name="included-headers"></a>En-têtes inclus

Pour utiliser le code de cette section, incluez les en-têtes suivants :


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a>Pointeur IWMPPlayer

Le pointeur **IWMPPlayer** est stocké dans une variable membre.


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a>Les appareils sont stockés dans un tableau

L’exemple de code accède à la variable de membre suivante, qui doit être déclarée dans l’en-tête du projet :


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



Le nombre de périphériques est stocké dans une variable membre.


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a>Récupération d’un pointeur d’appareil

Un pointeur vers un appareil particulier est récupéré via son index de tableau à l’aide d’un code similaire à ce qui suit :


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



Notez que l’index présenté dans les exemples précédents n’est pas l’index de partenariat pour l’appareil. Il s’agit de l’index de l’appareil dans le tableau personnalisé des appareils.

## <a name="cleaning-up"></a>Nettoyage

Les exemples utilisent la fonction suivante pour libérer la mémoire dans le tableau de périphériques et pour libérer les pointeurs d’interface :


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a>Les appareils s’affichent dans une zone de liste

La fonction GetSelectedDeviceIndex retourne l’index de l’appareil que l’utilisateur a sélectionné dans une zone de liste à l’aide du code suivant :


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a>L’état de l’interface utilisateur est géré par une seule fonction

La fonction SetUIState gère l’interface utilisateur.


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



Les détails de cette fonction ne sont pas pertinents pour les discussions de cette section, mais n’oubliez pas que cette fonction effectue des tâches telles que l’activation ou la désactivation de contrôles et la modification du texte affiché dans l’interface utilisateur.

L’énumération UIState a été définie comme suit :


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



Le paramètre *bconnected* spécifie s’il faut configurer l’interface utilisateur pour un appareil connecté (true signifie que l’appareil est connecté). Les paramètres *NewState* et *bconnected* fournissent les informations nécessaires à la fonction pour effectuer son travail.

Les sections suivantes fournissent des explications sur l’exemple de code :

-   [Énumération des appareils](enumerating-devices.md)
-   [Récupération des attributs de l’appareil](retrieving-device-attributes.md)
-   [Indication de la progression de la synchronisation](showing-synchronization-progress.md)
-   [Gestion des sélections de synchronisation](managing-synchronization-playlists.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de contrôle du lecteur**](player-control-guide.md)
</dt> </dl>

 

 




