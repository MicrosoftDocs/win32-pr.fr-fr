---
title: Classes, objets et interfaces
description: Classes, objets et interfaces
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104463906"
---
# <a name="classes-objects-and-interfaces"></a><span data-ttu-id="298fa-103">Classes, objets et interfaces</span><span class="sxs-lookup"><span data-stu-id="298fa-103">Classes, Objects, and Interfaces</span></span>

<span data-ttu-id="298fa-104">Dans le langage de programmation C++, une *classe* se compose de *Propriétés* (ou de données membres) et de *méthodes* (ou de fonctions membres).</span><span class="sxs-lookup"><span data-stu-id="298fa-104">In the C++ programming language, a *class* consists of *properties* (or member data) and *methods* (or member functions).</span></span> <span data-ttu-id="298fa-105">Les propriétés sont des éléments de données, tels que ceux contenus dans une structure.</span><span class="sxs-lookup"><span data-stu-id="298fa-105">The properties are data elements, such as those contained in a structure.</span></span> <span data-ttu-id="298fa-106">Les méthodes sont utilisées à diverses fins, telles que l’initialisation, l’assignation, les opérations et l’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="298fa-106">The methods are used for a variety of purposes, such as initialization, assignment, operations, and data access.</span></span> <span data-ttu-id="298fa-107">Vous utilisez une déclaration de classe de la même façon que vous utilisez une déclaration de structure.</span><span class="sxs-lookup"><span data-stu-id="298fa-107">You use a class declaration in the same way that you use a structure declaration.</span></span> <span data-ttu-id="298fa-108">La mémoire est allouée pour une classe lorsque vous définissez un *objet* de classe.</span><span class="sxs-lookup"><span data-stu-id="298fa-108">Memory is allocated for a class when you define a class *object*.</span></span> <span data-ttu-id="298fa-109">Chaque objet de classe a une zone de données pour ses propriétés et un tableau de pointeurs vers les méthodes qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="298fa-109">Each class object has a data area for its properties and a table of pointers to the methods it supports.</span></span>

<span data-ttu-id="298fa-110">Dans OLE, un objet se compose de données et de méthodes, comme c’est le cas en C++.</span><span class="sxs-lookup"><span data-stu-id="298fa-110">In OLE, an object consists of data and methods, as it does in C++.</span></span> <span data-ttu-id="298fa-111">Toutefois, un objet OLE adhère à des règles plus strictes.</span><span class="sxs-lookup"><span data-stu-id="298fa-111">However, an OLE object adheres to stricter rules.</span></span> <span data-ttu-id="298fa-112">Les données sont strictement internes.</span><span class="sxs-lookup"><span data-stu-id="298fa-112">The data is strictly internal.</span></span> <span data-ttu-id="298fa-113">Un objet expose uniquement des interfaces.</span><span class="sxs-lookup"><span data-stu-id="298fa-113">An object only exposes interfaces.</span></span> <span data-ttu-id="298fa-114">Une *interface* est un ensemble de méthodes associées pour un objet.</span><span class="sxs-lookup"><span data-stu-id="298fa-114">An *interface* is a set of related methods for an object.</span></span> <span data-ttu-id="298fa-115">Chaque objet peut prendre en charge plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="298fa-115">Each object can support multiple interfaces.</span></span> <span data-ttu-id="298fa-116">Toutes les interfaces OLE prennent en charge l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="298fa-116">All OLE interfaces support the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

 

 




