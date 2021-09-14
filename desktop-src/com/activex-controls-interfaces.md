---
title: ActiveX Interfaces de contrôles
description: ActiveX Interfaces de contrôles
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd7c4e0b726e9f330910bd468c237c72462fa21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232799"
---
# <a name="activex-controls-interfaces"></a>ActiveX Interfaces de contrôles

outre d’autres mécanismes de communication entre le contrôle et son client, ActiveX contrôle la technologie spécifie les interfaces [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) et [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) pour la communication avec le contrôle du client. Il existe également l’interface [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) pour les conteneurs de contrôle simples.

Toutefois, ces trois interfaces sont spécifiques aux contrôles et ne sont généralement pas utiles en dehors du contexte des contrôles. Ces interfaces sont définies comme suit.

``` syntax
interface IOleControl : IUnknown 
  { 
    HRESULT GetControlInfo([out] CONTROLINFO *pCI); 
    HRESULT OnMnemonic([in] LPMSG pMsg); 
    HRESULT OnAmbientPropertyChange([in] DISPID dispID); 
    HRESULT FreezeEvents([in] BOOL bFreeze); 
  } 
 
interface IOleControlSite : IUnknown 
  { 
    HRESULT OnControlInfoChanged(void); 
    HRESULT LockInPlaceActive([in] BOOL fLock); 
    HRESULT GetExtendedControl([out] IDispatch **ppDisp); 
    HRESULT TransformCoords([in-out] POINTL *pptlHimetric, [in-out] POINTF *pptfContainer, [in] DWORD dwFlags); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg, [in] DWORD grfModifiers); 
    HRESULT OnFocus([in] BOOL fGotFocus); 
    HRESULT ShowPropertyFrame(void); 
  } 
 
interface ISimpleFrameSite : IUnknown 
  { 
    HRESULT PreMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [out] DWORD *pdwCookie); 
    HRESULT PostMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [in] DWORD dwCookie); 
  } 
 
```

Certains contrôles, comme une zone de groupe, sont simplement un conteneur simple d’autres contrôles. Dans ce cas, le contrôle simple, appelé simple cadre, n’a pas à implémenter toutes les spécifications du conteneur. Il peut déléguer la plupart des appels d’interface de ses contrôles contenus au conteneur qui gère le frame simple. outre les appels d’interface, le frame simple doit également gérer Windows des messages qui proviennent potentiellement de contrôles qu’il contient. Pour cette raison, un conteneur fournit des [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) pour permettre à ces contrôles Frame simples de transmettre des messages vers le conteneur. [**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) traite le message en premier ; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) est appelé après que le frame simple a traité le message lui-même.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ActiveX Commandes](activex-controls.md)
</dt> </dl>

 

 




