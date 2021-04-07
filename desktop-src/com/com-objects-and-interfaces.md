---
title: Objets et interfaces COM
description: Objets et interfaces COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671390"
---
# <a name="com-objects-and-interfaces"></a><span data-ttu-id="c6a7a-103">Objets et interfaces COM</span><span class="sxs-lookup"><span data-stu-id="c6a7a-103">COM Objects and Interfaces</span></span>

<span data-ttu-id="c6a7a-104">COM est une technologie qui permet d’interagir avec des objets à travers les limites des processus et des ordinateurs aussi facilement qu’au sein d’un même processus.</span><span class="sxs-lookup"><span data-stu-id="c6a7a-104">COM is a technology that allows objects to interact across process and computer boundaries as easily as within a single process.</span></span> <span data-ttu-id="c6a7a-105">COM active cela en spécifiant que la seule façon de manipuler les données associées à un objet est d’utiliser une *interface* sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="c6a7a-105">COM enables this by specifying that the only way to manipulate the data associated with an object is through an *interface* on the object.</span></span> <span data-ttu-id="c6a7a-106">Quand ce terme est utilisé dans cette documentation, il fait référence à une implémentation dans le code d’une interface COM compatible binaire qui est associée à un objet.</span><span class="sxs-lookup"><span data-stu-id="c6a7a-106">When this term is used in this documentation, it refers to an implementation in code of a COM binary-compliant interface that is associated with an object.</span></span>

<span data-ttu-id="c6a7a-107">COM utilise l' *interface* de mot dans un sens différent de celui généralement utilisé dans la programmation de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c6a7a-107">COM uses the word *interface* in a sense different from that typically used in Visual C++ programming.</span></span> <span data-ttu-id="c6a7a-108">Une interface C++ fait référence à toutes les fonctions prises en charge par une classe et que les clients d’un objet peuvent appeler pour interagir avec elle.</span><span class="sxs-lookup"><span data-stu-id="c6a7a-108">A C++ interface refers to all of the functions that a class supports and that clients of an object can call to interact with it.</span></span> <span data-ttu-id="c6a7a-109">Une interface COM fait référence à un groupe prédéfini de fonctions associées qu’une classe COM implémente, mais une interface spécifique ne représente pas nécessairement toutes les fonctions prises en charge par la classe.</span><span class="sxs-lookup"><span data-stu-id="c6a7a-109">A COM interface refers to a predefined group of related functions that a COM class implements, but a specific interface does not necessarily represent all the functions that the class supports.</span></span>

<span data-ttu-id="c6a7a-110">La référence à un objet qui *implémente* une interface signifie que l’objet utilise du code qui implémente chaque méthode de l’interface et fournit des pointeurs conformes com à ces fonctions vers la bibliothèque com.</span><span class="sxs-lookup"><span data-stu-id="c6a7a-110">Referring to an object *implementing* an interface means that the object uses code that implements each method of the interface and provides COM binary-compliant pointers to those functions to the COM library.</span></span> <span data-ttu-id="c6a7a-111">COM rend ensuite ces fonctions disponibles à tout client qui demande un pointeur vers l’interface, que le client se trouve à l’intérieur ou à l’extérieur du processus qui implémente ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="c6a7a-111">COM then makes those functions available to any client who asks for a pointer to the interface, whether the client is inside or outside of the process that implements those functions.</span></span>

<span data-ttu-id="c6a7a-112">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6a7a-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="c6a7a-113">Interfaces et implémentations d’interface</span><span class="sxs-lookup"><span data-stu-id="c6a7a-113">Interfaces and Interface Implementations</span></span>](interfaces-and-interface-implementations.md)
-   [<span data-ttu-id="c6a7a-114">Pointeurs d’interface et interfaces</span><span class="sxs-lookup"><span data-stu-id="c6a7a-114">Interface Pointers and Interfaces</span></span>](interface-pointers-and-interfaces.md)
-   [<span data-ttu-id="c6a7a-115">IUnknown et héritage d’interface</span><span class="sxs-lookup"><span data-stu-id="c6a7a-115">IUnknown and Interface Inheritance</span></span>](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a><span data-ttu-id="c6a7a-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6a7a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6a7a-117">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c6a7a-117">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 




