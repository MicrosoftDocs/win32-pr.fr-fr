---
title: Accessibilité des contrôles ActiveX sans fenêtre
description: Cette section décrit comment utiliser l’API d’accessibilité Windows pour s’assurer que les contrôles Microsoft ActiveX sans fenêtre sont accessibles.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382345"
---
# <a name="windowless-activex-control-accessibility"></a><span data-ttu-id="a18e3-103">Accessibilité des contrôles ActiveX sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="a18e3-103">Windowless ActiveX Control Accessibility</span></span>

<span data-ttu-id="a18e3-104">Cette section décrit comment utiliser l’API d’accessibilité Windows pour s’assurer que les contrôles Microsoft ActiveX sans fenêtre sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="a18e3-104">This section describes how to use the Windows Accessibility API to ensure that windowless Microsoft ActiveX controls are accessible.</span></span>

<span data-ttu-id="a18e3-105">Windows 8 comprend de nouvelles interfaces API d’accessibilité Windows qui simplifient la tâche d’implémentation de l’accessibilité pour les contrôles ActiveX sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a18e3-105">Windows 8 includes new Windows Accessibility API interfaces that simplify the task of implementing accessibility for windowless ActiveX controls.</span></span> <span data-ttu-id="a18e3-106">L’API comprend des interfaces qui sont implémentées sur un contrôle sans fenêtre et sur le conteneur de contrôle, ce qui permet au contrôle sans fenêtre et à son conteneur de travailler ensemble pour fournir des informations d’accessibilité sur le contrôle sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a18e3-106">The API includes interfaces that are implemented on a windowless control and on the control container, enabling the windowless control and its container to work together to provide accessibility information about the windowless control.</span></span> <span data-ttu-id="a18e3-107">L’API prend en charge les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="a18e3-107">The API supports the following scenarios:</span></span>

-   <span data-ttu-id="a18e3-108">Microsoft Active Accessibility les contrôles sans fenêtre hébergés dans un conteneur de contrôle Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="a18e3-108">Microsoft Active Accessibility windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="a18e3-109">Microsoft Active Accessibility les contrôles sans fenêtre hébergés dans un conteneur de contrôle Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="a18e3-109">Microsoft Active Accessibility windowless controls hosted in a Microsoft UI Automation control container.</span></span>
-   <span data-ttu-id="a18e3-110">Contrôles sans fenêtre UI Automation hébergés dans un conteneur de contrôle Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="a18e3-110">UI Automation windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="a18e3-111">Contrôles sans fenêtre UI Automation hébergés dans un conteneur de contrôle UI Automation.</span><span class="sxs-lookup"><span data-stu-id="a18e3-111">UI Automation windowless controls hosted in a UI Automation control container.</span></span>

<span data-ttu-id="a18e3-112">Le tableau suivant répertorie les interfaces qui prennent en charge les contrôles ActiveX sans fenêtre et identifie les objets qui implémentent les interfaces.</span><span class="sxs-lookup"><span data-stu-id="a18e3-112">The following table lists the interfaces that support windowless ActiveX controls and identifies the objects that implement the interfaces.</span></span>



| <span data-ttu-id="a18e3-113">Object</span><span class="sxs-lookup"><span data-stu-id="a18e3-113">Object</span></span>              | <span data-ttu-id="a18e3-114">MSAA</span><span class="sxs-lookup"><span data-stu-id="a18e3-114">MSAA</span></span>                                                                             | <span data-ttu-id="a18e3-115">UI Automation</span><span class="sxs-lookup"><span data-stu-id="a18e3-115">UI automation</span></span>                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a18e3-116">Objet de contrôle</span><span class="sxs-lookup"><span data-stu-id="a18e3-116">Control object</span></span>      | [<span data-ttu-id="a18e3-117">**IAccessibleHandler**</span><span class="sxs-lookup"><span data-stu-id="a18e3-117">**IAccessibleHandler**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| <span data-ttu-id="a18e3-118">Site de contrôle</span><span class="sxs-lookup"><span data-stu-id="a18e3-118">Control site</span></span>        | [<span data-ttu-id="a18e3-119">**IAccessibleWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="a18e3-119">**IAccessibleWindowlessSite**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [<span data-ttu-id="a18e3-120">**IRawElementProviderWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="a18e3-120">**IRawElementProviderWindowlessSite**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| <span data-ttu-id="a18e3-121">Racine de la fenêtre hôte</span><span class="sxs-lookup"><span data-stu-id="a18e3-121">Root of host window</span></span> | [<span data-ttu-id="a18e3-122">**IAccessibleHostingElementProviders**</span><span class="sxs-lookup"><span data-stu-id="a18e3-122">**IAccessibleHostingElementProviders**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [<span data-ttu-id="a18e3-123">**IRawElementProviderHostingAccessibles**</span><span class="sxs-lookup"><span data-stu-id="a18e3-123">**IRawElementProviderHostingAccessibles**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a><span data-ttu-id="a18e3-124">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a18e3-124">In this section</span></span>

-   [<span data-ttu-id="a18e3-125">Comment utiliser UI Automation pour rendre un contrôle ActiveX sans fenêtre accessible</span><span class="sxs-lookup"><span data-stu-id="a18e3-125">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="a18e3-126">Comment utiliser MSAA pour rendre un contrôle ActiveX sans fenêtre accessible</span><span class="sxs-lookup"><span data-stu-id="a18e3-126">How to Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="a18e3-127">Comment héberger un contrôle ActiveX UI Automation sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="a18e3-127">How to Host a UI Automation Windowless ActiveX Control</span></span>](host-a-ui-automation-windowless-activex-control.md)
-   [<span data-ttu-id="a18e3-128">Comment héberger un contrôle ActiveX sans fenêtre MSAA</span><span class="sxs-lookup"><span data-stu-id="a18e3-128">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)

 

 