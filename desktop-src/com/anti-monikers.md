---
title: Anti-monikers
description: OLE fournit une implémentation d’un type spécial de moniker appelé anti-moniker.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029349"
---
# <a name="anti-monikers"></a><span data-ttu-id="74c22-103">Anti-monikers</span><span class="sxs-lookup"><span data-stu-id="74c22-103">Anti-Monikers</span></span>

<span data-ttu-id="74c22-104">OLE fournit une implémentation d’un type spécial de moniker appelé *anti-moniker*.</span><span class="sxs-lookup"><span data-stu-id="74c22-104">OLE provides an implementation of a special type of moniker called an *anti-moniker*.</span></span> <span data-ttu-id="74c22-105">Vous utilisez ce moniker dans la création de nouvelles classes de moniker.</span><span class="sxs-lookup"><span data-stu-id="74c22-105">You use this moniker in the creation of new moniker classes.</span></span> <span data-ttu-id="74c22-106">Vous l’utilisez comme inverse du moniker sur lequel il est composé, en annulant efficacement ce moniker, de la même façon que l’opérateur « .. » déplace un niveau de répertoire dans une commande de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="74c22-106">You use it as the inverse of the moniker that it is composed onto, effectively canceling that moniker, in much the same way that the ".." operator moves up a directory level in a file system command.</span></span>

<span data-ttu-id="74c22-107">Il est nécessaire d’avoir un anti-moniker disponible, car une fois qu’un moniker composite est créé, il n’est pas possible de supprimer des parties du moniker si, par exemple, un objet est déplacé.</span><span class="sxs-lookup"><span data-stu-id="74c22-107">It is necessary to have an anti-moniker available, because once a composite moniker is created, it is not possible to delete parts of the moniker if, for example, an object moves.</span></span> <span data-ttu-id="74c22-108">Au lieu de cela, vous utilisez un anti-moniker pour supprimer une ou plusieurs entrées d’un moniker composite.</span><span class="sxs-lookup"><span data-stu-id="74c22-108">Instead, you use an anti-moniker to remove one or more entries from a composite moniker.</span></span>

<span data-ttu-id="74c22-109">Les anti-monikers sont une classe de moniker explicitement conçue pour une utilisation en tant qu’inverse.</span><span class="sxs-lookup"><span data-stu-id="74c22-109">Anti-monikers are a moniker class explicitly intended for use as an inverse.</span></span> <span data-ttu-id="74c22-110">COM définit la fonction [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) nommée, qui retourne un anti-moniker.</span><span class="sxs-lookup"><span data-stu-id="74c22-110">COM defines the named [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) function, which returns an anti-moniker.</span></span> <span data-ttu-id="74c22-111">Cette fonction est généralement utilisée pour implémenter la méthode [**IMoniker :: inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) .</span><span class="sxs-lookup"><span data-stu-id="74c22-111">You generally use this function to implement the [**IMoniker::Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) method.</span></span>

<span data-ttu-id="74c22-112">Un anti-moniker est uniquement un inverse pour les types de monikers implémentés pour traiter les anti-monikers comme un inverse.</span><span class="sxs-lookup"><span data-stu-id="74c22-112">An anti-moniker is only an inverse for those types of monikers that are implemented to treat anti-monikers as an inverse.</span></span> <span data-ttu-id="74c22-113">Par exemple, si vous souhaitez supprimer la dernière partie d’un moniker composite, vous ne devez pas créer de anti-moniker et le composer à la fin du composite.</span><span class="sxs-lookup"><span data-stu-id="74c22-113">For example, if you want to remove the last piece of a composite moniker, you should not create an anti-moniker and compose it to the end of the composite.</span></span> <span data-ttu-id="74c22-114">Vous ne pouvez pas être sûr que la dernière pièce composite considère qu’un anti-moniker est son inverse.</span><span class="sxs-lookup"><span data-stu-id="74c22-114">You cannot be sure that the last piece of the composite considers an anti-moniker to be its inverse.</span></span> <span data-ttu-id="74c22-115">Au lieu de cela, vous devez appeler [**IMoniker :: enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) sur le moniker composite, en spécifiant **false** comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="74c22-115">Instead, you should call [**IMoniker::Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) on the composite moniker, specifying **FALSE** as the first parameter.</span></span> <span data-ttu-id="74c22-116">Cela crée un énumérateur qui retourne les monikers de composant dans l’ordre inverse.</span><span class="sxs-lookup"><span data-stu-id="74c22-116">This creates an enumerator that returns the component monikers in reverse order.</span></span> <span data-ttu-id="74c22-117">Utilisez l’énumérateur pour récupérer la dernière pièce du composite et appelez l' [**inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) sur ce moniker.</span><span class="sxs-lookup"><span data-stu-id="74c22-117">Use the enumerator to retrieve the last piece of the composite, and call [**Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) on that moniker.</span></span> <span data-ttu-id="74c22-118">Le moniker retourné par **inverse** est ce dont vous avez besoin pour supprimer la dernière partie du composite.</span><span class="sxs-lookup"><span data-stu-id="74c22-118">The moniker returned by **Inverse** is what you need to remove the last piece of the composite.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74c22-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74c22-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74c22-120">Monikers de classe</span><span class="sxs-lookup"><span data-stu-id="74c22-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="74c22-121">Monikers composites</span><span class="sxs-lookup"><span data-stu-id="74c22-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="74c22-122">Monikers de fichiers</span><span class="sxs-lookup"><span data-stu-id="74c22-122">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="74c22-123">Monikers d’élément</span><span class="sxs-lookup"><span data-stu-id="74c22-123">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="74c22-124">Monikers de pointeur</span><span class="sxs-lookup"><span data-stu-id="74c22-124">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




