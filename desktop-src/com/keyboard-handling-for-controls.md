---
title: Gestion du clavier pour les contrôles
description: Un contrôle répond aux accélérateurs de clavier afin que l’utilisateur final puisse lancer des actions effectuées par le contrôle.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311401"
---
# <a name="keyboard-handling-for-controls"></a><span data-ttu-id="7e4f0-103">Gestion du clavier pour les contrôles</span><span class="sxs-lookup"><span data-stu-id="7e4f0-103">Keyboard Handling for Controls</span></span>

<span data-ttu-id="7e4f0-104">Un contrôle répond aux accélérateurs de clavier afin que l’utilisateur final puisse lancer des actions effectuées par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-104">A control responds to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="7e4f0-105">Le conteneur gère l’activité du clavier pour tous ses contrôles incorporés.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-105">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="7e4f0-106">Avec les documents composés, les accélérateurs de clavier s’appliquent uniquement à l’objet actuellement actif.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-106">With compound documents, keyboard accelerators apply only to the currently active object.</span></span> <span data-ttu-id="7e4f0-107">Avec les contrôles, un mécanisme a été ajouté de manière à ce qu’un contrôle puisse répondre à ses mnémoniques de clavier, même s’il n’est pas actuellement actif dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-107">With controls, a mechanism has been added so that a control can respond to its keyboard mnemonics even if it is not currently UI-active.</span></span>

<span data-ttu-id="7e4f0-108">Les méthodes [**IOleControl :: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) et [**IOleControl :: OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) et la méthode [**IOleControlSite :: OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) gèrent les mnémoniques du clavier d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-108">The [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) methods and the [**IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) method handle a control's keyboard mnemonics.</span></span> <span data-ttu-id="7e4f0-109">Une structure [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) décrit les accélérateurs mnémoniques d’un contrôle, et les indicateurs renvoyés avec celle-ci via la méthode **GetControlInfo** décrivent le comportement des contrôles avec les touches entrée et ÉCHAP.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-109">A [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) structure describes a control's mnemonic accelerators, and the flags passed back with it through the **GetControlInfo** method describe the controls behavior with the Enter and Esc keys.</span></span> <span data-ttu-id="7e4f0-110">Lorsqu’un contrôle modifie ses mnémoniques, il appelle **OnControlInfoChanged** afin que le conteneur puisse recharger la structure si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-110">When a control changes its mnemonics, it calls **OnControlInfoChanged** so the container can reload the structure if necessary.</span></span>

<span data-ttu-id="7e4f0-111">Lorsqu’un contrôle est activé par l’interface utilisateur, il s’agit également du contrôle avec le focus.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-111">When a control is UI active, it is also the control with the focus.</span></span> <span data-ttu-id="7e4f0-112">À mesure que les contrôles sont activés et désactivés entre les États active et active de l’interface utilisateur sur place, le contrôle appelle [**IOleControlSite :: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) pour indiquer au conteneur de telles modifications.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-112">As controls are activated and deactivated between the in-place active and the UI active states, the control calls [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) to tell the container of such changes.</span></span>

<span data-ttu-id="7e4f0-113">En outre, lorsqu’un contrôle est activé par l’interface utilisateur, il aura la possibilité de traiter toutes les séquences de touches.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-113">In addition, when a control is UI active, it will have first chance to process any keystrokes.</span></span> <span data-ttu-id="7e4f0-114">Pour permettre à un conteneur de traiter la séquence de touches avant le contrôle, le contrôle appelle [**IOleControlSite :: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span><span class="sxs-lookup"><span data-stu-id="7e4f0-114">To give a container the opportunity to process the keystroke before the control, the control calls [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span></span> <span data-ttu-id="7e4f0-115">Si le conteneur ne gère pas la séquence de touches, le contrôle le traite.</span><span class="sxs-lookup"><span data-stu-id="7e4f0-115">If the container does not handle the keystroke, the control then processes it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e4f0-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e4f0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e4f0-117">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="7e4f0-117">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




