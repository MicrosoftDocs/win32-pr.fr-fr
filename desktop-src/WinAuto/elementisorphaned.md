---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512281"
---
# <a name="elementisorphaned"></a><span data-ttu-id="76b26-103">ElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="76b26-103">ElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="76b26-104">Texte</span><span class="sxs-lookup"><span data-stu-id="76b26-104">Text</span></span>

<span data-ttu-id="76b26-105">L’élément est un IAccessible orphelin dans l’arborescence</span><span class="sxs-lookup"><span data-stu-id="76b26-105">Element is an orphaned IAccessible in the tree</span></span>

## <a name="type"></a><span data-ttu-id="76b26-106">Type</span><span class="sxs-lookup"><span data-stu-id="76b26-106">Type</span></span>

<span data-ttu-id="76b26-107">Error</span><span class="sxs-lookup"><span data-stu-id="76b26-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="76b26-108">Description</span><span class="sxs-lookup"><span data-stu-id="76b26-108">Description</span></span>

<span data-ttu-id="76b26-109">L’adresse de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’objet obtenue pour les coordonnées données est une référence à un élément orphelin dans l’arborescence d’éléments.</span><span class="sxs-lookup"><span data-stu-id="76b26-109">The address of the object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="76b26-110">Ce problème est un problème pour les personnes qui s’appuient sur un lecteur d’écran et un clavier pour la navigation, car les éléments sont traités comme invisibles et ne sont pas annoncés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="76b26-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="76b26-111">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="76b26-111">Possible causes</span></span>

-   <span data-ttu-id="76b26-112">L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.</span><span class="sxs-lookup"><span data-stu-id="76b26-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="76b26-113">Implémentation MSAA incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="76b26-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76b26-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76b26-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b26-115">Navigation via le test de positionnement et l’emplacement à l’écran</span><span class="sxs-lookup"><span data-stu-id="76b26-115">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[<span data-ttu-id="76b26-116">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="76b26-116">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




