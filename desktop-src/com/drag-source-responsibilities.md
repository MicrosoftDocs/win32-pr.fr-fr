---
title: Faire glisser les responsabilités source
description: Faire glisser les responsabilités source
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106512530"
---
# <a name="drag-source-responsibilities"></a><span data-ttu-id="fb703-103">Faire glisser les responsabilités source</span><span class="sxs-lookup"><span data-stu-id="fb703-103">Drag Source Responsibilities</span></span>

<span data-ttu-id="fb703-104">La source de glissement est chargée des tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb703-104">The drag source is responsible for the following tasks:</span></span>

-   <span data-ttu-id="fb703-105">Fournir un objet de transfert de données pour la cible de déplacement qui expose les interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) et [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="fb703-105">Providing a data-transfer object for the drop target that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span>
-   <span data-ttu-id="fb703-106">Génération des commentaires du pointeur et de la source.</span><span class="sxs-lookup"><span data-stu-id="fb703-106">Generating pointer and source feedback.</span></span>
-   <span data-ttu-id="fb703-107">Détermination du moment où l’opération glisser a été annulée ou une opération de suppression s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fb703-107">Determining when the drag operation has been canceled or a drop operation has occurred.</span></span>
-   <span data-ttu-id="fb703-108">Effectuer une action sur les données d’origine provoquée par l’opération de déplacement, telle que la suppression des données ou la création d’un lien vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="fb703-108">Performing any action on the original data caused by the drop operation, such as deleting the data or creating a link to it.</span></span>

<span data-ttu-id="fb703-109">La tâche principale consiste à créer un objet de transfert de données qui expose les interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) et [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="fb703-109">The main task is creating a data-transfer object that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span> <span data-ttu-id="fb703-110">La source de glissement peut ou non inclure une copie des données sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="fb703-110">The drag source might or might not include a copy of the selected data.</span></span> <span data-ttu-id="fb703-111">L’inclusion n’est pas obligatoire, mais cela vous permet de vous protéger contre les modifications involontaires et permet au code des opérations du presse-papiers d’être identique au code de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="fb703-111">Including it is not mandatory, but doing so helps protect against inadvertent changes and allows the Clipboard operations code to be identical to the drag and drop code.</span></span>

<span data-ttu-id="fb703-112">Pendant qu’une opération glisser est en cours, la source de glissement est chargée de définir le pointeur de la souris et, le cas échéant, de fournir des commentaires sources supplémentaires à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb703-112">While a drag operation is in progress, the drag source is responsible for setting the mouse pointer and, if appropriate, for providing additional source feedback to the user.</span></span> <span data-ttu-id="fb703-113">La source de glissement ne peut pas fournir de commentaires qui suivent la position de la souris autrement qu’en définissant réellement le pointeur réel (consultez la fonction [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) ).</span><span class="sxs-lookup"><span data-stu-id="fb703-113">The drag source cannot provide any feedback that tracks the mouse position other than by actually setting the real pointer (see the [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) function).</span></span> <span data-ttu-id="fb703-114">Cette règle doit être appliquée pour éviter les conflits avec les commentaires fournis par la cible de déplacement.</span><span class="sxs-lookup"><span data-stu-id="fb703-114">This rule must be enforced to avoid conflicts with the feedback provided by the drop target.</span></span> <span data-ttu-id="fb703-115">(Une source de glissement peut également être une cible de déplacement.</span><span class="sxs-lookup"><span data-stu-id="fb703-115">(A drag source can also be a drop target.</span></span> <span data-ttu-id="fb703-116">En cas de suppression sur lui-même, la source/cible peut, bien sûr, fournir des commentaires ciblés pour suivre la position de la souris.</span><span class="sxs-lookup"><span data-stu-id="fb703-116">When dropping on itself, the source/target can, of course, provide target feedback to track the mouse position.</span></span> <span data-ttu-id="fb703-117">Dans ce cas, toutefois, il s’agit de la cible de déplacement qui effectue le suivi de la souris, et non de la source.) En fonction des commentaires offerts par la cible de déplacement, la source définit un pointeur approprié.</span><span class="sxs-lookup"><span data-stu-id="fb703-117">In this case, however, it is the drop target tracking the mouse, not the source.) Based on the feedback offered by the drop target, the source sets an appropriate pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb703-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb703-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb703-119">Glisser-déposer</span><span class="sxs-lookup"><span data-stu-id="fb703-119">Drag and Drop</span></span>](drag-and-drop.md)
</dt> </dl>

 

 