---
title: Propriétés ambiantes pour les contrôles
description: Propriétés ambiantes pour les contrôles
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380063"
---
# <a name="ambient-properties-for-controls"></a><span data-ttu-id="63d32-103">Propriétés ambiantes pour les contrôles</span><span class="sxs-lookup"><span data-stu-id="63d32-103">Ambient Properties for Controls</span></span>

<span data-ttu-id="63d32-104">Si un contrôle prend en charge toutes les propriétés ambiantes, il doit au moins respecter les valeurs des propriétés ambiantes suivantes dans les conditions indiquées dans le tableau suivant en utilisant les DISPID standard.</span><span class="sxs-lookup"><span data-stu-id="63d32-104">If a control supports any ambient properties at all, it must at least respect the values of the following ambient properties under the conditions stated in the following table using the standard dispids.</span></span>



| <span data-ttu-id="63d32-105">Propriété ambiante</span><span class="sxs-lookup"><span data-stu-id="63d32-105">Ambient Property</span></span>            | <span data-ttu-id="63d32-106">Égal</span><span class="sxs-lookup"><span data-stu-id="63d32-106">Dispid</span></span>          | <span data-ttu-id="63d32-107">Commentaire/conditions d’utilisation</span><span class="sxs-lookup"><span data-stu-id="63d32-107">Comment/Conditions for Use</span></span>                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d32-108">LocaleID</span><span class="sxs-lookup"><span data-stu-id="63d32-108">LocaleID</span></span><br/>         | <span data-ttu-id="63d32-109">-705</span><span class="sxs-lookup"><span data-stu-id="63d32-109">-705</span></span><br/> | <span data-ttu-id="63d32-110">Si les paramètres régionaux sont significatifs pour le contrôle, par exemple pour la sortie de texte</span><span class="sxs-lookup"><span data-stu-id="63d32-110">If Locale is significant to the control, e.g. for text output</span></span><br/>                                                                                                                                                                                                                  |
| <span data-ttu-id="63d32-111">UserMode</span><span class="sxs-lookup"><span data-stu-id="63d32-111">UserMode</span></span> <br/>        | <span data-ttu-id="63d32-112">-709</span><span class="sxs-lookup"><span data-stu-id="63d32-112">-709</span></span><br/> | <span data-ttu-id="63d32-113">Si le contrôle se comporte différemment en mode utilisateur (conception) et en mode exécution</span><span class="sxs-lookup"><span data-stu-id="63d32-113">If the control behaves differently in user (design) mode and run mode</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="63d32-114">UIDead</span><span class="sxs-lookup"><span data-stu-id="63d32-114">UIDead</span></span><br/>           | <span data-ttu-id="63d32-115">-710</span><span class="sxs-lookup"><span data-stu-id="63d32-115">-710</span></span><br/> | <span data-ttu-id="63d32-116">Si le contrôle réagit aux événements d’interface utilisateur, il doit honorer cette propriété ambiante</span><span class="sxs-lookup"><span data-stu-id="63d32-116">If the control reacts to UI events, then it should honor this ambient property</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="63d32-117">ShowGrabHandles</span><span class="sxs-lookup"><span data-stu-id="63d32-117">ShowGrabHandles</span></span><br/>  | <span data-ttu-id="63d32-118">-711</span><span class="sxs-lookup"><span data-stu-id="63d32-118">-711</span></span><br/> | <span data-ttu-id="63d32-119">Si le contrôle prend en charge le redimensionnement sur place de lui-même</span><span class="sxs-lookup"><span data-stu-id="63d32-119">If the control support in-place resizing of itself</span></span><br/>                                                                                                                                                                                                                             |
| <span data-ttu-id="63d32-120">ShowHatching</span><span class="sxs-lookup"><span data-stu-id="63d32-120">ShowHatching</span></span><br/>     | <span data-ttu-id="63d32-121">-712</span><span class="sxs-lookup"><span data-stu-id="63d32-121">-712</span></span><br/> | <span data-ttu-id="63d32-122">Si le contrôle prend en charge l’activation sur place et l’activation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="63d32-122">If the control support in-place activation and UI activation</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="63d32-123">DisplayAsDefault</span><span class="sxs-lookup"><span data-stu-id="63d32-123">DisplayAsDefault</span></span><br/> | <span data-ttu-id="63d32-124">-713</span><span class="sxs-lookup"><span data-stu-id="63d32-124">-713</span></span><br/> | <span data-ttu-id="63d32-125">Uniquement si le contrôle est marqué OLEMISC \_ ACTSLIKEBUTTON (ce qui signifie que la prise en charge des mnémoniques de clavier est fournie, [**IOleControl :: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) et [**IOleControl :: OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) doivent être implémentés).</span><span class="sxs-lookup"><span data-stu-id="63d32-125">Only if the control is marked OLEMISC\_ACTSLIKEBUTTON (which means that support for keyboard mnemonics is provided, thus [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) must be implemented).</span></span><br/> |



 

<span data-ttu-id="63d32-126">Comme décrit précédemment, l’utilisation d’ambiances nécessite à la fois [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (pour [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) au minimum) et [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (pour [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) et [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span><span class="sxs-lookup"><span data-stu-id="63d32-126">As described previously, use of ambients requires both [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (for [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) as a minimum) as well as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (for [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) and [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span></span>

<span data-ttu-id="63d32-127">Le \_ bit OLEMISC SETCLIENTSITEFIRST peut ne pas nécessairement être pris en charge par un conteneur.</span><span class="sxs-lookup"><span data-stu-id="63d32-127">The OLEMISC\_SETCLIENTSITEFIRST bit may not necessarily be supported by a container.</span></span> <span data-ttu-id="63d32-128">Dans ces circonstances, un contrôle doit recourir à des valeurs par défaut pour les propriétés ambiantes dont il a besoin.</span><span class="sxs-lookup"><span data-stu-id="63d32-128">In these circumstances, a control must resort to default values for the ambient properties that it requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63d32-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63d32-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63d32-130">Contrôles</span><span class="sxs-lookup"><span data-stu-id="63d32-130">Controls</span></span>](controls.md)
</dt> </dl>

 

 





