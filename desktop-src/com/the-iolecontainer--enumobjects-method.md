---
title: Méthode IOleContainer EnumObjects
description: Méthode IOleContainer EnumObjects
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190841"
---
# <a name="the-iolecontainerenumobjects-method"></a><span data-ttu-id="d987a-103">La méthode IOleContainer :: EnumObjects</span><span class="sxs-lookup"><span data-stu-id="d987a-103">The IOleContainer::EnumObjects Method</span></span>

<span data-ttu-id="d987a-104">Cette méthode est utilisée pour énumérer tous les objets OLE contenus dans un document ou un formulaire, en retournant un pointeur d’interface pour chaque objet OLE.</span><span class="sxs-lookup"><span data-stu-id="d987a-104">This method is used to enumerate over all the OLE objects contained in a document or form, returning an interface pointer for each OLE object.</span></span> <span data-ttu-id="d987a-105">Le conteneur doit renvoyer des pointeurs vers chaque objet OLE qui partage le même conteneur.</span><span class="sxs-lookup"><span data-stu-id="d987a-105">The container must return pointers to each OLE object that shares the same container.</span></span> <span data-ttu-id="d987a-106">Les formulaires imbriqués ou les contrôles imbriqués doivent également être énumérés.</span><span class="sxs-lookup"><span data-stu-id="d987a-106">Nested forms or nested controls must also be enumerated.</span></span>

<span data-ttu-id="d987a-107">Certains conteneurs implémentent des contrôles d’extendeur, qui encapsulent des contrôles non ActiveX, puis retournent des pointeurs vers ces contrôles d’extendeur au fur et à mesure qu’un formulaire est énuméré.</span><span class="sxs-lookup"><span data-stu-id="d987a-107">Some containers implement extender controls, which wrap non-ActiveX controls, and then return pointers to these extender controls as a form is enumerated.</span></span> <span data-ttu-id="d987a-108">Ce comportement permet aux contrôles ActiveX et aux conteneurs de contrôles ActiveX de s’intégrer parfaitement aux contrôles non ActiveX. il est donc recommandé, mais pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d987a-108">This behavior enables ActiveX controls and ActiveX control containers to integrate well with non-ActiveX controls, and is thus recommended, but not required.</span></span>

 

 




