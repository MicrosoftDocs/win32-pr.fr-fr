---
title: Attributs de structure et d’Union
description: Utilisez les \_ attributs Switch \ pour spécifier la caractéristique d’une Union dans un appel de procédure distante. Utilisez l’attribut ignore pour désigner certains membres de structure ou d’Union comme locaux pour l’application cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL MIDL, attributs, structure et Union
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462158"
---
# <a name="structure-and-union-attributes"></a><span data-ttu-id="913c0-105">Attributs de structure et d’Union</span><span class="sxs-lookup"><span data-stu-id="913c0-105">Structure and Union Attributes</span></span>

<span data-ttu-id="913c0-106">Utilisez les attributs de **commutateur \_** \* pour spécifier la caractéristique d’une Union dans un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="913c0-106">Use the **switch\_**\* attributes to specify the characteristic of a union in a remote procedure call.</span></span> <span data-ttu-id="913c0-107">Utilisez l’attribut [**ignore**](ignore.md) pour désigner certains membres de structure ou d’Union comme locaux pour l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="913c0-107">Use the [**ignore**](ignore.md) attribute to designate certain structure or union members as local to the client application.</span></span>



| <span data-ttu-id="913c0-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="913c0-108">Attribute</span></span>                           | <span data-ttu-id="913c0-109">Utilisation</span><span class="sxs-lookup"><span data-stu-id="913c0-109">Usage</span></span>                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="913c0-110">**Utilisez**</span><span class="sxs-lookup"><span data-stu-id="913c0-110">**switch**</span></span>](switch.md)            | <span data-ttu-id="913c0-111">Sélectionne le discriminante pour une Union encapsulée.</span><span class="sxs-lookup"><span data-stu-id="913c0-111">Selects the discriminant for an encapsulated union.</span></span>                                                                           |
| [<span data-ttu-id="913c0-112">**le commutateur \_ est**</span><span class="sxs-lookup"><span data-stu-id="913c0-112">**switch\_is**</span></span>](switch-is.md)     | <span data-ttu-id="913c0-113">Identifie le discriminante pour une Union qui n’est pas encapsulée.</span><span class="sxs-lookup"><span data-stu-id="913c0-113">Identifies the discriminant for a nonencapsulated union.</span></span>                                                                      |
| [<span data-ttu-id="913c0-114">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="913c0-114">**switch\_type**</span></span>](switch-type.md) | <span data-ttu-id="913c0-115">Identifie le type du discriminante pour une Union non encapsulée.</span><span class="sxs-lookup"><span data-stu-id="913c0-115">Identifies the type of the discriminant for a nonencapsulated union.</span></span>                                                          |
| [<span data-ttu-id="913c0-116">**tenir**</span><span class="sxs-lookup"><span data-stu-id="913c0-116">**ignore**</span></span>](ignore.md)            | <span data-ttu-id="913c0-117">Désigne un pointeur contenu dans une structure ou une Union, et l’objet indiqué par le pointeur ne doit pas être transmis.</span><span class="sxs-lookup"><span data-stu-id="913c0-117">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span> |



 

<span data-ttu-id="913c0-118">Vous pouvez également utiliser les [attributs de pointeur de tableau et de dimensionnement](array-and-sized-pointer-attributes.md) pour spécifier les caractéristiques des membres de structure ou d’Union.</span><span class="sxs-lookup"><span data-stu-id="913c0-118">You can also use the [array and sized pointer attributes](array-and-sized-pointer-attributes.md) to specify characteristics of structure or union members.</span></span>

 

 




