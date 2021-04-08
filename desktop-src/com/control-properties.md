---
title: Propriétés du contrôle
description: Propriétés du contrôle
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840785"
---
# <a name="control-properties"></a><span data-ttu-id="ccaee-103">Propriétés du contrôle</span><span class="sxs-lookup"><span data-stu-id="ccaee-103">Control Properties</span></span>

<span data-ttu-id="ccaee-104">En plus des propriétés définies et implémentées par le contrôle lui-même, la technologie des contrôles ActiveX implique également :</span><span class="sxs-lookup"><span data-stu-id="ccaee-104">In addition to properties defined and implemented by the control itself, ActiveX controls technology also involves:</span></span>

<dl> <dt>

<span data-ttu-id="ccaee-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Propriétés ambiantes</span><span class="sxs-lookup"><span data-stu-id="ccaee-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Ambient properties</span></span>
</dt> <dd>

<span data-ttu-id="ccaee-106">Celles-ci sont exposées par le conteneur via un site client de contrôle afin de fournir des valeurs environnementales qui s’appliquent à tous les contrôles incorporés dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="ccaee-106">These are exposed by the container through a control client site to provide environmental values that apply to all controls embedded in the container.</span></span> <span data-ttu-id="ccaee-107">Par exemple, un conteneur peut fournir une couleur d’arrière-plan par défaut ou une police par défaut que le contrôle peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="ccaee-107">For example, a container can provide a default background color or a default font that the control can use.</span></span> <span data-ttu-id="ccaee-108">Les propriétés ambiantes sont exposées par le biais de **IDispatch** implémenté sur l’objet site d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="ccaee-108">Ambient properties are exposed through **IDispatch** implemented on a container's site object.</span></span> <span data-ttu-id="ccaee-109">Le conteneur appelle la méthode [**IOleControl :: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) du contrôle quand l’une de ses propriétés ambiantes change la valeur.</span><span class="sxs-lookup"><span data-stu-id="ccaee-109">The container calls the control's [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) method when any of its ambient properties change value.</span></span> <span data-ttu-id="ccaee-110">En réponse, un contrôle peut avoir besoin de mettre à jour son propre état interne ou visuel en réponse.</span><span class="sxs-lookup"><span data-stu-id="ccaee-110">In response, a control may need to update its own internal or visual state in response.</span></span> <span data-ttu-id="ccaee-111">Le conteneur indique la propriété ambiante qui a changé avec le paramètre DISPID ou peut passer DISPID \_ Unknown pour indiquer que plusieurs propriétés ambiantes ont changé.</span><span class="sxs-lookup"><span data-stu-id="ccaee-111">The container indicates which ambient property changed with the DISPID parameter or may pass DISPID\_UNKNOWN to indicate that multiple ambient properties changed.</span></span>

</dd> <dt>

<span data-ttu-id="ccaee-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Propriétés étendues</span><span class="sxs-lookup"><span data-stu-id="ccaee-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Extended properties</span></span>
</dt> <dd>

<span data-ttu-id="ccaee-113">Ils sont implémentés par un conteneur pour encapsuler les contrôles qu’il contient pour fournir des propriétés gérées par le conteneur qui s’affichent comme s’il s’agissait de propriétés de contrôle natif.</span><span class="sxs-lookup"><span data-stu-id="ccaee-113">These are actually implemented by a container to wrap the controls it contains to provide container-managed properties that appear as if they were native control properties.</span></span> <span data-ttu-id="ccaee-114">Le conteneur peut agréger le contrôle, en ajoutant les propriétés étendues pour compléter ou substituer les propriétés du contrôle.</span><span class="sxs-lookup"><span data-stu-id="ccaee-114">The container can aggregate the control, adding the extended properties to supplement or override the control's properties.</span></span> <span data-ttu-id="ccaee-115">L’objet agrégé est appelé un contrôle étendu.</span><span class="sxs-lookup"><span data-stu-id="ccaee-115">The aggregated object is called an extended control.</span></span> <span data-ttu-id="ccaee-116">Pour le conteneur, le contrôle étendu apparaît comme le contrôle lui-même et les propriétés étendues semblent être exposées par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ccaee-116">To the container, the extended control appears as the control itself and extended properties appear to be exposed by the control.</span></span> <span data-ttu-id="ccaee-117">Le conteneur prend en charge un contrôle étendu par le biais de sa méthode de site client [**IOleControlSite :: GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span><span class="sxs-lookup"><span data-stu-id="ccaee-117">The container supports an extended control through its client site method [**IOleControlSite::GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span></span> <span data-ttu-id="ccaee-118">La méthode **GetExtendedControl** permet aux contrôles de naviguer dans le site jusqu’à l’objet de contrôle étendu fourni pour eux par le conteneur, si le conteneur prend en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ccaee-118">The **GetExtendedControl** method allows controls to navigate through the site to the extended control object provided for them by the container, if the container supports this feature.</span></span> <span data-ttu-id="ccaee-119">Un conteneur peut également choisir d’afficher les pages de propriétés de ses contrôles étendus, en plus des pages qu’un contrôle spécifie normalement par le biais de [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span><span class="sxs-lookup"><span data-stu-id="ccaee-119">A container can also choose to show property pages for its extended controls in addition to those pages that a control would normally specify through [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span></span> <span data-ttu-id="ccaee-120">Pour cette raison, un contrôle doit demander à un conteneur d’afficher un frame de propriété avant que le contrôle ne tente de le faire.</span><span class="sxs-lookup"><span data-stu-id="ccaee-120">Because of this, a control has to ask a container to show a property frame before the control attempts to do so itself.</span></span> <span data-ttu-id="ccaee-121">Le contrôle appelle [**IOleControlSite :: ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="ccaee-121">The control calls [**IOleControlSite::ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) to do this.</span></span> <span data-ttu-id="ccaee-122">Si le conteneur implémente cette fonction, il affiche le frame de propriété lui-même ; Si la méthode retourne une erreur, le contrôle peut afficher le frame de propriété.</span><span class="sxs-lookup"><span data-stu-id="ccaee-122">If the container implements this function then it shows the property frame itself; if the method returns an error then the control can show the property frame.</span></span>

</dd> </dl>

<span data-ttu-id="ccaee-123">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ccaee-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ccaee-124">Propriétés standard</span><span class="sxs-lookup"><span data-stu-id="ccaee-124">Standard Properties</span></span>](standard-properties.md)
-   [<span data-ttu-id="ccaee-125">Objet de police standard</span><span class="sxs-lookup"><span data-stu-id="ccaee-125">Standard Font Object</span></span>](standard-font-object.md)
-   [<span data-ttu-id="ccaee-126">Objet image standard</span><span class="sxs-lookup"><span data-stu-id="ccaee-126">Standard Picture Object</span></span>](standard-picture-object.md)

## <a name="related-topics"></a><span data-ttu-id="ccaee-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccaee-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccaee-128">Méthodes de contrôle</span><span class="sxs-lookup"><span data-stu-id="ccaee-128">Control Methods</span></span>](control-methods.md)
</dt> </dl>

 

 




