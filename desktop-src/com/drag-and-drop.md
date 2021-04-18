---
title: Glisser-déposer
description: Le glisser-déplacer fait référence aux transferts de données dans lesquels une souris ou un autre dispositif de pointage est utilisé pour spécifier la source de données et sa destination.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509389"
---
# <a name="drag-and-drop"></a><span data-ttu-id="e2dbf-103">Glisser-déposer</span><span class="sxs-lookup"><span data-stu-id="e2dbf-103">Drag and Drop</span></span>

<span data-ttu-id="e2dbf-104">Le *glisser-déplacer* fait référence aux transferts de données dans lesquels une souris ou un autre dispositif de pointage est utilisé pour spécifier la source de données et sa destination.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-104">*Drag and drop* refers to data transfers in which a mouse or other pointing device is used to specify both the data source and its destination.</span></span> <span data-ttu-id="e2dbf-105">Dans une opération de glisser-déplacer classique, un utilisateur sélectionne l’objet à transférer en positionnant le pointeur de la souris sur celui-ci et en maintenant le bouton gauche ou un autre bouton désigné à cet effet.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-105">In a typical drag and drop operation, a user selects the object to be transferred by moving the mouse pointer to it and holding down either the left button or some other button designated for this purpose.</span></span> <span data-ttu-id="e2dbf-106">Tout en continuant à maintenir le bouton enfoncé, l’utilisateur lance le transfert en faisant glisser l’objet vers sa destination, qui peut être n’importe quel conteneur OLE.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-106">While continuing to hold down the button, the user initiates the transfer by dragging the object to its destination, which can be any OLE container.</span></span> <span data-ttu-id="e2dbf-107">Le glisser-déplacer fournit exactement les mêmes fonctionnalités que le presse-papiers OLE copier et coller, mais ajoute des commentaires visuels et élimine le besoin de menus.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-107">Drag and drop provides exactly the same functionality as the OLE clipboard copy and paste but adds visual feedback and eliminates the need for menus.</span></span> <span data-ttu-id="e2dbf-108">En fait, si une application prend en charge le copier-coller du presse-papiers, il est très utile de prendre en charge le glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-108">In fact, if an application supports clipboard copy and paste, little extra is needed to support drag and drop.</span></span>

<span data-ttu-id="e2dbf-109">Au cours d’une opération de glisser-déplacer OLE, les trois éléments de code suivants sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-109">During an OLE drag and drop operation, the following three separate pieces of code are used.</span></span>



| <span data-ttu-id="e2dbf-110">Glisser-déplacer la source du code</span><span class="sxs-lookup"><span data-stu-id="e2dbf-110">Drag-and-drop code source</span></span>                               | <span data-ttu-id="e2dbf-111">Implémentation et utilisation</span><span class="sxs-lookup"><span data-stu-id="e2dbf-111">Implementation and use</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2dbf-112">Interface [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)</span><span class="sxs-lookup"><span data-stu-id="e2dbf-112">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interface</span></span><br/> | <span data-ttu-id="e2dbf-113">Implémenté par l’objet contenant les données glissées, appelées « *source de glissement*».</span><span class="sxs-lookup"><span data-stu-id="e2dbf-113">Implemented by the object containing the dragged data, referred to as the *drag source*.</span></span><br/>                                                                                         |
| <span data-ttu-id="e2dbf-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) , interface</span><span class="sxs-lookup"><span data-stu-id="e2dbf-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interface</span></span><br/> | <span data-ttu-id="e2dbf-115">Implémenté par l’objet qui est destiné à accepter la suppression, appelée *cible de déplacement*.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-115">Implemented by the object that is intended to accept the drop, referred to as the *drop target*.</span></span><br/>                                                                                 |
| <span data-ttu-id="e2dbf-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) , fonction</span><span class="sxs-lookup"><span data-stu-id="e2dbf-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function</span></span><br/>    | <span data-ttu-id="e2dbf-117">Implémenté par OLE et utilisé pour initier une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-117">Implemented by OLE and used to initiate a drag and drop operation.</span></span> <span data-ttu-id="e2dbf-118">Une fois l’opération en cours, elle facilite la communication entre la source de glissement et la cible de déplacement.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-118">After the operation is in progress, it facilitates communication between the drag source and the drop target.</span></span><br/> |



 

<span data-ttu-id="e2dbf-119">Les interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) et [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) peuvent être implémentées dans un conteneur ou dans une application d’objet.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-119">The [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interfaces can be implemented in either a container or in an object application.</span></span> <span data-ttu-id="e2dbf-120">Le rôle de la source de glissement ou de la cible de déplacement n’est pas limité à un type d’application OLE.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-120">The role of drag source or drop target is not limited to any one type of OLE application.</span></span>

<span data-ttu-id="e2dbf-121">La fonction OLE [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implémente une boucle qui effectue le suivi du mouvement de la souris et du clavier jusqu’à ce que l’opération glisser soit annulée ou qu’une suppression se produise.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-121">The OLE function [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implements a loop that tracks mouse and keyboard movement until such time as the drag is canceled or a drop occurs.</span></span> <span data-ttu-id="e2dbf-122">**DoDragDrop** est la fonction clé dans le processus de glisser-déplacer, qui facilite la communication entre la source du glissement et la cible du déplacement.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-122">**DoDragDrop** is the key function in the drag and drop process, facilitating communication between the drag source and drop target.</span></span>

<span data-ttu-id="e2dbf-123">Au cours d’une opération de glisser-déplacer, trois types de commentaires peuvent être affichés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-123">During a drag and drop operation, three types of feedback can be displayed to the user.</span></span>



| <span data-ttu-id="e2dbf-124">Type de commentaires</span><span class="sxs-lookup"><span data-stu-id="e2dbf-124">Type of feedback</span></span>            | <span data-ttu-id="e2dbf-125">Description</span><span class="sxs-lookup"><span data-stu-id="e2dbf-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2dbf-126">Commentaires sur la source</span><span class="sxs-lookup"><span data-stu-id="e2dbf-126">Source feedback</span></span><br/>  | <span data-ttu-id="e2dbf-127">Fourni par la source de glissement, la rétroaction source indique que les données sont glissées et qu’elles ne changent pas au cours de l’opération de glissement.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-127">Provided by the drag source, the source feedback indicates the data is being dragged and does not change during the course of the drag.</span></span> <span data-ttu-id="e2dbf-128">En règle générale, les données sont mises en surbrillance pour signaler qu’elles ont été sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-128">Typically, the data is highlighted to signal it has been selected.</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="e2dbf-129">Commentaires sur le pointeur</span><span class="sxs-lookup"><span data-stu-id="e2dbf-129">Pointer feedback</span></span><br/> | <span data-ttu-id="e2dbf-130">Fourni par la source de glissement, les commentaires du pointeur indiquent ce qui se passe si la souris est relâchée à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-130">Provided by the drag source, the pointer feedback indicates what happens if the mouse is released at any given moment.</span></span> <span data-ttu-id="e2dbf-131">Les commentaires des pointeurs changent continuellement lorsque l’utilisateur déplace la souris et/ou appuie sur une touche de modification.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-131">Pointer feedback changes continually as the user moves the mouse and/or presses a modifier key.</span></span> <span data-ttu-id="e2dbf-132">Par exemple, si le pointeur est déplacé dans une fenêtre qui ne peut pas accepter une suppression, le pointeur se transforme en symbole « non autorisé ».</span><span class="sxs-lookup"><span data-stu-id="e2dbf-132">For example, if the pointer is moved into a window that cannot accept a drop, the pointer changes to the "not allowed" symbol.</span></span><br/> |
| <span data-ttu-id="e2dbf-133">Commentaires sur la cible</span><span class="sxs-lookup"><span data-stu-id="e2dbf-133">Target feedback</span></span><br/>  | <span data-ttu-id="e2dbf-134">Fourni par la cible de déplacement, les commentaires ciblés indiquent où la suppression doit se produire.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-134">Provided by the drop target, target feedback indicates where the drop is to occur.</span></span><br/>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="e2dbf-135">Pour plus d’informations, consultez [faire glisser les responsabilités](drag-source-responsibilities.md)de la source.</span><span class="sxs-lookup"><span data-stu-id="e2dbf-135">For more information, see [Drag Source Responsibilities](drag-source-responsibilities.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2dbf-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2dbf-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2dbf-137">Transfert de données</span><span class="sxs-lookup"><span data-stu-id="e2dbf-137">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 





