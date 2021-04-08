---
title: Vue d'ensemble technique
description: Microsoft Active Accessibility améliore la façon dont les aides à l’accessibilité (programmes spécialisés qui aident les personnes handicapées à utiliser les ordinateurs de manière plus efficace) fonctionnent avec les applications qui s’exécutent sur Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674830"
---
# <a name="technical-overview"></a><span data-ttu-id="50491-103">Vue d'ensemble technique</span><span class="sxs-lookup"><span data-stu-id="50491-103">Technical Overview</span></span>

<span data-ttu-id="50491-104">Microsoft Active Accessibility améliore la façon dont les aides à l’accessibilité (programmes spécialisés qui aident les personnes handicapées à utiliser les ordinateurs de manière plus efficace) fonctionnent avec les applications qui s’exécutent sur Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="50491-104">Microsoft Active Accessibility improves the way accessibility aids (specialized programs that help people with disabilities use computers more effectively) work with applications running on Microsoft Windows.</span></span>

<span data-ttu-id="50491-105">Microsoft Active Accessibility est basé sur le modèle COM (Component Object Model), qui a été développé par Microsoft et est une norme de l’industrie qui définit une méthode courante pour la communication entre les applications et les systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="50491-105">Microsoft Active Accessibility is based on the Component Object Model (COM), which was developed by Microsoft and is an industry standard that defines a common way for applications and operating systems to communicate.</span></span> <span data-ttu-id="50491-106">Microsoft Active Accessibility comprend les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="50491-106">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="50491-107">L’interface COM [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), qui expose des informations sur les éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="50491-107">The COM interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), which exposes information about UI elements.</span></span> <span data-ttu-id="50491-108">**IAccessible** possède également des propriétés et des méthodes pour obtenir des informations sur et manipuler cet élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="50491-108">**IAccessible** also has properties and methods for obtaining information about and manipulating that UI element.</span></span>
-   <span data-ttu-id="50491-109">WinEvents, un système d’événement qui permet aux serveurs de notifier les clients lorsqu’un objet accessible change.</span><span class="sxs-lookup"><span data-stu-id="50491-109">WinEvents, an event system that allows servers to notify clients when an accessible object changes.</span></span>
-   <span data-ttu-id="50491-110">Oleacc.dll, une DLL de prise en charge ou d’exécution.</span><span class="sxs-lookup"><span data-stu-id="50491-110">Oleacc.dll, a support or run-time DLL.</span></span>

<span data-ttu-id="50491-111">La DLL Microsoft Active Accessibility, Oleacc.dll, est constituée des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="50491-111">The Microsoft Active Accessibility DLL, Oleacc.dll, consists of the following components:</span></span>

-   <span data-ttu-id="50491-112">Fonctions qui permettent aux clients de demander un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (par exemple, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span><span class="sxs-lookup"><span data-stu-id="50491-112">Functions that allow clients to request an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer (for example, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span></span>
-   <span data-ttu-id="50491-113">Fonctions permettant aux serveurs de retourner un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à un client (par exemple, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span><span class="sxs-lookup"><span data-stu-id="50491-113">Functions that allow servers to return an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to a client (for example, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span></span>
-   <span data-ttu-id="50491-114">Fonctions permettant d’obtenir du texte localisé pour le rôle et les codes d’État (par exemple, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) et [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span><span class="sxs-lookup"><span data-stu-id="50491-114">Functions for getting localized text for the role and state codes (for example, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) and [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span></span>
-   <span data-ttu-id="50491-115">Certaines fonctions d’assistance ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span><span class="sxs-lookup"><span data-stu-id="50491-115">Some helper functions ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span></span>
-   <span data-ttu-id="50491-116">Code qui fournit l’implémentation par défaut de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour les contrôles utilisateur standard et COMCTL.</span><span class="sxs-lookup"><span data-stu-id="50491-116">Code that provides the default implementation of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) for standard USER and COMCTL controls.</span></span> <span data-ttu-id="50491-117">Étant donné qu’elles implémentent **IAccessible** pour le compte des contrôles système, elles sont appelées *proxys*.</span><span class="sxs-lookup"><span data-stu-id="50491-117">Because these implement **IAccessible** on behalf of the system controls, they are known as *proxies*.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="50491-118">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="50491-118">In this section</span></span>

-   [<span data-ttu-id="50491-119">Fonctionnement de Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="50491-119">How Active Accessibility Works</span></span>](how-active-accessibility-works.md)
-   [<span data-ttu-id="50491-120">Notions de base Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="50491-120">Active Accessibility Basics</span></span>](active-accessibility-basics.md)
-   [<span data-ttu-id="50491-121">Instructions du serveur</span><span class="sxs-lookup"><span data-stu-id="50491-121">Server Guidelines</span></span>](server-guidelines.md)
-   [<span data-ttu-id="50491-122">Instructions du client</span><span class="sxs-lookup"><span data-stu-id="50491-122">Client Guidelines</span></span>](client-guidelines.md)
-   [<span data-ttu-id="50491-123">Directives COM et Unicode</span><span class="sxs-lookup"><span data-stu-id="50491-123">COM and Unicode Guidelines</span></span>](com-and-unicode-guidelines.md)

 

 




