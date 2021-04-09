---
title: Contrôles RichEdit sans fenêtre
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles RichEdit sans fenêtre.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028814"
---
# <a name="windowless-rich-edit-controls"></a><span data-ttu-id="dfdb5-103">Contrôles RichEdit sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="dfdb5-103">Windowless Rich Edit Controls</span></span>

<span data-ttu-id="dfdb5-104">Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles RichEdit sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dfdb5-104">This section contains information about the programming elements used with windowless rich edit controls.</span></span> <span data-ttu-id="dfdb5-105">Le modèle COM (Component Object Model) définit un jeu d’interfaces pour prendre en charge les objets sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dfdb5-105">The Component Object Model (COM) defines a set of interfaces to support windowless objects.</span></span> <span data-ttu-id="dfdb5-106">Les objets sans fenêtre peuvent accéder à l’état actif sur place sans avoir leur propre fenêtre, mais plutôt utiliser la fenêtre de leur conteneur.</span><span class="sxs-lookup"><span data-stu-id="dfdb5-106">Windowless objects can enter the in-place active state without having their own window, but rather use the window of their container.</span></span> <span data-ttu-id="dfdb5-107">Par conséquent, un objet sans fenêtre utilise moins de ressources système et offre de meilleures performances via une activation et une désactivation plus rapides.</span><span class="sxs-lookup"><span data-stu-id="dfdb5-107">Consequently, a windowless object uses fewer system resources and gives better performance through faster activation and deactivation.</span></span> <span data-ttu-id="dfdb5-108">En outre, les objets sans fenêtre peuvent être non rectangulaires et transparents.</span><span class="sxs-lookup"><span data-stu-id="dfdb5-108">In addition, windowless objects can be nonrectangular and transparent.</span></span>

### <a name="overviews"></a><span data-ttu-id="dfdb5-109">Vues d'ensemble</span><span class="sxs-lookup"><span data-stu-id="dfdb5-109">Overviews</span></span>



| <span data-ttu-id="dfdb5-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="dfdb5-110">Topic</span></span>                                                                          | <span data-ttu-id="dfdb5-111">Contenu</span><span class="sxs-lookup"><span data-stu-id="dfdb5-111">Contents</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfdb5-112">À propos des contrôles RichEdit sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="dfdb5-112">About Windowless Rich Edit Controls</span></span>](about-windowless-rich-edit-controls.md) | <span data-ttu-id="dfdb5-113">Un contrôle RichEdit sans fenêtre, également connu sous le nom d’objet de services de texte, est un objet qui fournit les fonctionnalités d’un [contrôle RichEdit](rich-edit-controls.md) sans fournir la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dfdb5-113">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="dfdb5-114">Fonctions</span><span class="sxs-lookup"><span data-stu-id="dfdb5-114">Functions</span></span>



| <span data-ttu-id="dfdb5-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="dfdb5-115">Topic</span></span>                                            | <span data-ttu-id="dfdb5-116">Contenu</span><span class="sxs-lookup"><span data-stu-id="dfdb5-116">Contents</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfdb5-117">**CreateTextServices**</span><span class="sxs-lookup"><span data-stu-id="dfdb5-117">**CreateTextServices**</span></span>](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | <span data-ttu-id="dfdb5-118">La fonction [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) crée une instance d’un objet de services de texte.</span><span class="sxs-lookup"><span data-stu-id="dfdb5-118">The [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function creates an instance of a text services object.</span></span> <span data-ttu-id="dfdb5-119">L’objet services de texte prend en charge une variété d’interfaces, notamment [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) et le modèle d’objet de texte (Tom).</span><span class="sxs-lookup"><span data-stu-id="dfdb5-119">The text services object supports a variety of interfaces, including [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and the Text Object Model (TOM).</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="dfdb5-120">Interfaces</span><span class="sxs-lookup"><span data-stu-id="dfdb5-120">Interfaces</span></span>



| <span data-ttu-id="dfdb5-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="dfdb5-121">Topic</span></span>                                  | <span data-ttu-id="dfdb5-122">Contenu</span><span class="sxs-lookup"><span data-stu-id="dfdb5-122">Contents</span></span>                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfdb5-123">**ITextHost**</span><span class="sxs-lookup"><span data-stu-id="dfdb5-123">**ITextHost**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | <span data-ttu-id="dfdb5-124">L’interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) est utilisée par un objet Text services pour obtenir des services d’hôte de texte.</span><span class="sxs-lookup"><span data-stu-id="dfdb5-124">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface is used by a text services object to obtain text host services.</span></span><br/> |
| [<span data-ttu-id="dfdb5-125">**ITextServices**</span><span class="sxs-lookup"><span data-stu-id="dfdb5-125">**ITextServices**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itextservices) | <span data-ttu-id="dfdb5-126">Étend TOM pour fournir des fonctionnalités supplémentaires pour une opération sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dfdb5-126">Extends the TOM to provide extra functionality for windowless operation.</span></span><br/>                                     |



 

 

 





