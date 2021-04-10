---
title: Objets incorporés (COM)
description: Objets incorporés
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102692"
---
# <a name="embedded-objects-com"></a><span data-ttu-id="c30cd-103">Objets incorporés (COM)</span><span class="sxs-lookup"><span data-stu-id="c30cd-103">Embedded Objects (COM)</span></span>

<span data-ttu-id="c30cd-104">Un objet incorporé est stocké physiquement dans le document composé, ainsi que toutes les informations nécessaires pour gérer l’objet.</span><span class="sxs-lookup"><span data-stu-id="c30cd-104">An embedded object is physically stored in the compound document, along with all the information needed to manage the object.</span></span> <span data-ttu-id="c30cd-105">En d’autres termes, l’objet incorporé fait partie du document composé dans lequel il réside.</span><span class="sxs-lookup"><span data-stu-id="c30cd-105">In other words, the embedded object is actually a part of the compound document in which it resides.</span></span> <span data-ttu-id="c30cd-106">Cette configuration présente quelques inconvénients.</span><span class="sxs-lookup"><span data-stu-id="c30cd-106">This arrangement has a couple of disadvantages.</span></span> <span data-ttu-id="c30cd-107">Tout d’abord, un document composé contenant des objets incorporés est plus grand que l’autre contenant les mêmes objets que les liens.</span><span class="sxs-lookup"><span data-stu-id="c30cd-107">First, a compound document containing embedded objects will be larger than one containing the same objects as links.</span></span> <span data-ttu-id="c30cd-108">Deuxièmement, les modifications apportées à la source d’un objet incorporé ne sont pas automatiquement répliquées dans la copie incorporée, et les modifications apportées à la copie incorporée ne sont pas reflétées dans la source, comme c’est le cas avec un lien.</span><span class="sxs-lookup"><span data-stu-id="c30cd-108">Second, changes made to the source of an embedded object will not be automatically replicated in the embedded copy, and changes in the embedded copy will not be reflected in the source, as they are with a link.</span></span>

<span data-ttu-id="c30cd-109">Toutefois, dans certains cas, l’incorporation offre plusieurs avantages par rapport aux liens.</span><span class="sxs-lookup"><span data-stu-id="c30cd-109">Still, for certain purposes, embedding offers several advantages over links.</span></span> <span data-ttu-id="c30cd-110">Tout d’abord, les utilisateurs peuvent transférer des documents composés avec des objets incorporés vers d’autres ordinateurs ou d’autres emplacements sur le même ordinateur, sans rompre de lien.</span><span class="sxs-lookup"><span data-stu-id="c30cd-110">First, users can transfer compound documents with embedded objects to other computers, or other locations on the same computer, without breaking a link.</span></span> <span data-ttu-id="c30cd-111">Deuxièmement, les utilisateurs peuvent modifier des objets incorporés sans modifier le contenu de l’original.</span><span class="sxs-lookup"><span data-stu-id="c30cd-111">Second, users can edit embedded objects without changing the content of the original.</span></span> <span data-ttu-id="c30cd-112">Parfois, cette séparation est précisément ce qui est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c30cd-112">Sometimes, this separation is precisely what is required.</span></span> <span data-ttu-id="c30cd-113">Troisièmement, les objets incorporés peuvent être activés sur place, ce qui signifie que l’utilisateur peut modifier ou manipuler l’objet sans avoir à travailler dans une fenêtre distincte de celle du conteneur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c30cd-113">Third, embedded objects can be activated in place, meaning that the user can edit or otherwise manipulate the object without having to work in a separate window from that of the object's container.</span></span> <span data-ttu-id="c30cd-114">Au lieu de cela, lorsque l’objet est activé, l’interface utilisateur de l’application conteneur change pour exposer les outils nécessaires à la gestion ou à la modification de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c30cd-114">Instead, when the object is activated, the container application's user interface changes to expose those tools that are necessary to manage or modify the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c30cd-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c30cd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c30cd-116">Création d’objets liés et incorporés à partir de données existantes</span><span class="sxs-lookup"><span data-stu-id="c30cd-116">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




