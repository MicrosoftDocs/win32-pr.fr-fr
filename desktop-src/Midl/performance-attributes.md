---
title: Attributs de performance
description: Utilisez les attributs suivants dans un fichier IDL pour réduire la taille du code stub ou pour améliorer les performances.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- IDL MIDL, attributs, performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029849"
---
# <a name="performance-attributes"></a><span data-ttu-id="079cd-104">Attributs de performance</span><span class="sxs-lookup"><span data-stu-id="079cd-104">Performance Attributes</span></span>

<span data-ttu-id="079cd-105">Utilisez les attributs suivants dans un fichier IDL pour réduire la taille du code stub ou pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="079cd-105">Use the following attributes in an IDL file to reduce the size of the stub code or otherwise improve performance.</span></span>



| <span data-ttu-id="079cd-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="079cd-106">Attribute</span></span>                             | <span data-ttu-id="079cd-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="079cd-107">Usage</span></span>                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="079cd-108">**tenir**</span><span class="sxs-lookup"><span data-stu-id="079cd-108">**ignore**</span></span>](ignore.md)              | <span data-ttu-id="079cd-109">Désigne un pointeur contenu dans une structure ou une Union, et l’objet indiqué par le pointeur ne doit pas être transmis.</span><span class="sxs-lookup"><span data-stu-id="079cd-109">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span>                        |
| [<span data-ttu-id="079cd-110">**localisé**</span><span class="sxs-lookup"><span data-stu-id="079cd-110">**local**</span></span>](local.md)                | <span data-ttu-id="079cd-111">Désigne une fonction qui est locale à l’application pour laquelle MIDL n’a pas besoin de générer de code stub.</span><span class="sxs-lookup"><span data-stu-id="079cd-111">Designates a function that is local to the application for which MIDL does not need to generate stub code.</span></span>                                           |
| [<span data-ttu-id="079cd-112">**Marshal de câble \_**</span><span class="sxs-lookup"><span data-stu-id="079cd-112">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="079cd-113">Définit un type de données comme type plus simple pour la transmission sur un réseau et vous permet d’implémenter des routines de marshaling et de démarshaling pour le type.</span><span class="sxs-lookup"><span data-stu-id="079cd-113">Defines a data type as a simpler type for transmission over a network and allows you to implement marshaling and unmarshaling routines for the type.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="079cd-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="079cd-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="079cd-115">Attributs ACF de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="079cd-115">Memory Management ACF Attributes</span></span>](memory-management-acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="079cd-116">Attributs ACF d’optimisation du stub</span><span class="sxs-lookup"><span data-stu-id="079cd-116">Stub Optimization ACF Attributes</span></span>](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




