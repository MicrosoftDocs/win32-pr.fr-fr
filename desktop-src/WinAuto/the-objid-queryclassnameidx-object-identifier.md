---
title: Identificateur de l’objet OBJID_QUERYCLASSNAMEIDX
description: Microsoft Active Accessibility utilise l' \_ identificateur d’objet objid QUERYCLASSNAMEIDX avec le \_ message WM GETOBJECT pour déterminer la classe à laquelle appartient un contrôle Windows standard ou un contrôle commun.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512230"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a><span data-ttu-id="40cbb-103">Identificateur d' \_ objet QUERYCLASSNAMEIDX objid</span><span class="sxs-lookup"><span data-stu-id="40cbb-103">The OBJID\_QUERYCLASSNAMEIDX Object Identifier</span></span>

<span data-ttu-id="40cbb-104">Microsoft Active Accessibility utilise l’identificateur d’objet [**objID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) avec le message [**WM \_ GETOBJECT**](wm-getobject.md) pour déterminer la classe à laquelle appartient un contrôle Windows standard ou un contrôle commun.</span><span class="sxs-lookup"><span data-stu-id="40cbb-104">Microsoft Active Accessibility uses the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier with the [**WM\_GETOBJECT**](wm-getobject.md) message to determine the class to which a standard Windows control or common control belongs.</span></span> <span data-ttu-id="40cbb-105">Un contrôle répond à ce message en retournant une valeur que Microsoft Active Accessibility mappe au nom de classe du contrôle.</span><span class="sxs-lookup"><span data-stu-id="40cbb-105">A control responds to this message by returning a value that Microsoft Active Accessibility maps to the class name of the control.</span></span> <span data-ttu-id="40cbb-106">Microsoft Active Accessibility utilise ces informations pour fournir une prise en charge de l’accessibilité pour les contrôles Windows standard et les contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="40cbb-106">Microsoft Active Accessibility uses this information to provide accessibility support for standard Windows controls and common controls.</span></span>

<span data-ttu-id="40cbb-107">En règle générale, seuls les contrôles Windows standard et les contrôles communs répondent à l’identificateur d’objet [**objID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="40cbb-107">Generally, only the standard Windows controls and the common controls respond to the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="40cbb-108">Toutefois, un contrôle personnalisé peut également répondre s’il comprend toutes les mêmes fonctionnalités qu’un contrôle Windows standard ou un contrôle commun existant.</span><span class="sxs-lookup"><span data-stu-id="40cbb-108">However, a custom control can also respond if it includes all of the same functionality as an existing standard Windows control or common control.</span></span> <span data-ttu-id="40cbb-109">Cela permet au contrôle personnalisé d’être pris en charge par l’un des objets proxy standard fournis par Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="40cbb-109">This enables the custom control to be supported by one of the standard proxy objects provided by Microsoft Active Accessibility.</span></span>

<span data-ttu-id="40cbb-110">Pour plus d’informations, consultez [annexe F : valeurs de l’identificateur d’objet pour objid \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span><span class="sxs-lookup"><span data-stu-id="40cbb-110">For more information, see [Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span></span>

 

 




