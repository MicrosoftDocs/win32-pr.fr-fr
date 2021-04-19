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
# <a name="activex-controls-interfaces"></a><span data-ttu-id="28f8d-103">Interfaces de contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="28f8d-103">ActiveX Controls Interfaces</span></span>

<span data-ttu-id="28f8d-104">Outre d’autres mécanismes de communication entre le contrôle et son client, la technologie des contrôles ActiveX spécifie les interfaces [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) et [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) pour la communication de contrôle client.</span><span class="sxs-lookup"><span data-stu-id="28f8d-104">In addition to other mechanisms for communicating between the control and its client, ActiveX controls technology specifies the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) and [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interfaces for client-control communication.</span></span> <span data-ttu-id="28f8d-105">Il existe également l’interface [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) pour les conteneurs de contrôle simples.</span><span class="sxs-lookup"><span data-stu-id="28f8d-105">There is also the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface for simple control containers.</span></span>

<span data-ttu-id="28f8d-106">Toutefois, ces trois interfaces sont spécifiques aux contrôles et ne sont généralement pas utiles en dehors du contexte des contrôles.</span><span class="sxs-lookup"><span data-stu-id="28f8d-106">These three interfaces are, however, specific to controls and are not generally useful outside the context of controls.</span></span> <span data-ttu-id="28f8d-107">Ces interfaces sont définies comme suit.</span><span class="sxs-lookup"><span data-stu-id="28f8d-107">These interfaces are defined as follows.</span></span>

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

<span data-ttu-id="28f8d-108">Certains contrôles, comme une zone de groupe, sont simplement un conteneur simple d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="28f8d-108">Some controls, like a group box, are merely a simple container of other controls.</span></span> <span data-ttu-id="28f8d-109">Dans ce cas, le contrôle simple, appelé simple cadre, n’a pas à implémenter toutes les spécifications du conteneur.</span><span class="sxs-lookup"><span data-stu-id="28f8d-109">In such cases, the simple control, called a simple frame, doesn't have to implement all the container requirements.</span></span> <span data-ttu-id="28f8d-110">Il peut déléguer la plupart des appels d’interface de ses contrôles contenus au conteneur qui gère le frame simple.</span><span class="sxs-lookup"><span data-stu-id="28f8d-110">It can delegate most of the interface calls from its contained controls to the container that manages the simple frame.</span></span> <span data-ttu-id="28f8d-111">Outre les appels d’interface, le frame simple doit également gérer les messages Windows qui peuvent provenir de contrôles qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="28f8d-111">Besides interface calls, the simple frame also has to deal with Windows messages that potentially come from controls within it.</span></span> <span data-ttu-id="28f8d-112">Pour cette raison, un conteneur fournit des [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) pour permettre à ces contrôles Frame simples de transmettre des messages vers le conteneur.</span><span class="sxs-lookup"><span data-stu-id="28f8d-112">For this reason, a container supplies [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) to allow such simple frame controls to pass messages up to the container.</span></span> <span data-ttu-id="28f8d-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) traite le message en premier ; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) est appelé après que le frame simple a traité le message lui-même.</span><span class="sxs-lookup"><span data-stu-id="28f8d-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) processes the message first; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) is called after the simple frame has processed the message itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28f8d-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28f8d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f8d-115">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="28f8d-115">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




