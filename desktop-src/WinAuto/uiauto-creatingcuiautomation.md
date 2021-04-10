---
title: Création de l’objet CUIAutomation
description: Cette section décrit comment prendre en main l’écriture d’une application cliente UI Automation Microsoft en instanciant un objet qui implémente IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- clients, création d’un objet CUIAutomation
- clients, objet CUIAutomation
- UI Automation, objet CUIAutomation
- UI Automation, création d’un objet CUIAutomation
- création de l’objet CUIAutomation
- Objet CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941049"
---
# <a name="creating-the-cuiautomation-object"></a><span data-ttu-id="b8b7f-109">Création de l’objet CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="b8b7f-109">Creating the CUIAutomation Object</span></span>

<span data-ttu-id="b8b7f-110">Cette section décrit comment prendre en main l’écriture d’une application cliente UI Automation Microsoft en instanciant un objet qui implémente [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="b8b7f-110">This section describes how to get started writing a Microsoft UI Automation client application by instantiating an object that implements [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>

<span data-ttu-id="b8b7f-111">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-111">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b8b7f-112">Objet CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="b8b7f-112">The CUIAutomation Object</span></span>](#the-cuiautomation-object)
-   [<span data-ttu-id="b8b7f-113">Création de l’objet</span><span class="sxs-lookup"><span data-stu-id="b8b7f-113">Creating the Object</span></span>](#creating-the-object)
-   [<span data-ttu-id="b8b7f-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8b7f-114">Related topics</span></span>](#related-topics)

## <a name="the-cuiautomation-object"></a><span data-ttu-id="b8b7f-115">Objet CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="b8b7f-115">The CUIAutomation Object</span></span>

<span data-ttu-id="b8b7f-116">La première étape de l’utilisation d’UI Automation consiste à créer un objet de la classe [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8b7f-116">The first step in using UI Automation is to create an object of the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) class.</span></span> <span data-ttu-id="b8b7f-117">Cet objet expose l’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , qui est la passerelle vers tous les autres objets et interfaces utilisés par les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-117">This object exposes the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface, which is the gateway to all the other objects and interfaces that are used by client applications.</span></span> <span data-ttu-id="b8b7f-118">Entre autres choses, **IUIAutomation** est utilisé pour les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8b7f-118">Among other things, **IUIAutomation** is used for the following tasks:</span></span>

-   <span data-ttu-id="b8b7f-119">Abonnement à des événements.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-119">Subscribing to events.</span></span>
-   <span data-ttu-id="b8b7f-120">Création de conditions.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-120">Creating conditions.</span></span> <span data-ttu-id="b8b7f-121">Les conditions sont des objets utilisés pour limiter l’étendue des recherches d’éléments UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-121">Conditions are objects used to narrow the scope of searches for UI Automation elements.</span></span>
-   <span data-ttu-id="b8b7f-122">Obtention d’éléments UI Automation directement à partir du Bureau (élément racine), ou à partir de coordonnées d’écran ou de handles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-122">Obtaining UI Automation elements directly from the desktop (the root element), or from screen coordinates or window handles.</span></span>
-   <span data-ttu-id="b8b7f-123">Création d’objets de l’Explorateur d’arborescence qui peuvent être utilisés pour naviguer dans la hiérarchie des éléments UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-123">Creating tree walker objects that can be used to navigate the hierarchy of UI Automation elements.</span></span>
-   <span data-ttu-id="b8b7f-124">Conversion des types de données.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-124">Converting data types.</span></span>

## <a name="creating-the-object"></a><span data-ttu-id="b8b7f-125">Création de l’objet</span><span class="sxs-lookup"><span data-stu-id="b8b7f-125">Creating the Object</span></span>

<span data-ttu-id="b8b7f-126">Pour commencer à utiliser UI Automation dans votre application, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b8b7f-126">To get started using UI Automation in your application, take the following steps:</span></span>

-   <span data-ttu-id="b8b7f-127">Incluez UIAutomation. h dans les en-têtes de votre projet.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-127">Include UIAutomation.h in your project headers.</span></span> <span data-ttu-id="b8b7f-128">UIAutomation. h apporte les autres en-têtes qui définissent l’API.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-128">UIAutomation.h brings in the other headers that define the API.</span></span>
-   <span data-ttu-id="b8b7f-129">Déclarez un pointeur vers [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="b8b7f-129">Declare a pointer to [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>
-   <span data-ttu-id="b8b7f-130">Initialisez le modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="b8b7f-130">Initialize the Component Object Model (COM).</span></span>
-   <span data-ttu-id="b8b7f-131">Créez une instance de [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) et récupérez l’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) dans votre pointeur.</span><span class="sxs-lookup"><span data-stu-id="b8b7f-131">Create an instance of [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) and retrieve the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in your pointer.</span></span>

<span data-ttu-id="b8b7f-132">L’exemple de fonction suivant initialise COM, puis crée l’objet [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , en extrayant l’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) dans le pointeur *ppAutomation* .</span><span class="sxs-lookup"><span data-stu-id="b8b7f-132">The following example function initializes COM, and then creates the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) object, retrieving the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in the *ppAutomation* pointer.</span></span>


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a><span data-ttu-id="b8b7f-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8b7f-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b8b7f-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b8b7f-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b8b7f-135">Vue d'ensemble des événements UI Automation</span><span class="sxs-lookup"><span data-stu-id="b8b7f-135">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="b8b7f-136">Obtention d'éléments UI Automation</span><span class="sxs-lookup"><span data-stu-id="b8b7f-136">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> </dl>

 

 