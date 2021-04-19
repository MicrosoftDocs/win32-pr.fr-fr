---
title: Interfaces de contrôles ActiveX
description: Interfaces de contrôles ActiveX
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd7c4e0b726e9f330910bd468c237c72462fa21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106532027"
---
# <a name="activex-controls-interfaces"></a>Interfaces de contrôles ActiveX

Outre d’autres mécanismes de communication entre le contrôle et son client, la technologie des contrôles ActiveX spécifie les interfaces [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) et [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) pour la communication de contrôle client. Il existe également l’interface [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) pour les conteneurs de contrôle simples.

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

Certains contrôles, comme une zone de groupe, sont simplement un conteneur simple d’autres contrôles. Dans ce cas, le contrôle simple, appelé simple cadre, n’a pas à implémenter toutes les spécifications du conteneur. Il peut déléguer la plupart des appels d’interface de ses contrôles contenus au conteneur qui gère le frame simple. Outre les appels d’interface, le frame simple doit également gérer les messages Windows qui peuvent provenir de contrôles qu’il contient. Pour cette raison, un conteneur fournit des [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) pour permettre à ces contrôles Frame simples de transmettre des messages vers le conteneur. [**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) traite le message en premier ; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) est appelé après que le frame simple a traité le message lui-même.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles ActiveX](activex-controls.md)
</dt> </dl>

 

 




