---
description: Comment créer une DLL de filtre DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Comment créer une DLL de filtre DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514301"
---
# <a name="how-to-create-a-directshow-filter-dll"></a><span data-ttu-id="5f8a7-103">Comment créer une DLL de filtre DirectShow</span><span class="sxs-lookup"><span data-stu-id="5f8a7-103">How to Create a DirectShow Filter DLL</span></span>

<span data-ttu-id="5f8a7-104">Cet article explique comment implémenter un composant en tant que bibliothèque de liens dynamiques (DLL) dans Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-104">This article describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span> <span data-ttu-id="5f8a7-105">Cet article est une suite de la [procédure d’implémentation de IUnknown](how-to-implement-iunknown.md), qui décrit comment implémenter l’interface **IUnknown** en dérivant votre composant de la classe de base [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="5f8a7-105">This article is a continuation from [How to Implement IUnknown](how-to-implement-iunknown.md), which describes how to implement the **IUnknown** interface by deriving your component from the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="5f8a7-106">Cet article contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-106">This article contains the following sections.</span></span>

-   [<span data-ttu-id="5f8a7-107">Fabriques de classes et modèles de fabrique</span><span class="sxs-lookup"><span data-stu-id="5f8a7-107">Class Factories and Factory Templates</span></span>](class-factories-and-factory-templates.md)
-   [<span data-ttu-id="5f8a7-108">Tableau de modèles de fabrique</span><span class="sxs-lookup"><span data-stu-id="5f8a7-108">Factory Template Array</span></span>](factory-template-array.md)
-   [<span data-ttu-id="5f8a7-109">Fonctions DLL</span><span class="sxs-lookup"><span data-stu-id="5f8a7-109">DLL Functions</span></span>](dll-functions.md)

<span data-ttu-id="5f8a7-110">L’inscription d’un filtre DirectShow (par opposition à un objet COM générique) requiert des étapes supplémentaires qui ne sont pas traitées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="5f8a7-110">Registering a DirectShow filter (as opposed to a generic COM object) requires some additional steps that are not covered in this article.</span></span> <span data-ttu-id="5f8a7-111">Pour plus d’informations sur l’enregistrement des filtres, voir [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5f8a7-111">For information on registering filters, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f8a7-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f8a7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f8a7-113">DirectShow et COM</span><span class="sxs-lookup"><span data-stu-id="5f8a7-113">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



