---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379789"
---
# <a name="tabbedtounknownelement"></a><span data-ttu-id="ae2dd-103">TabbedToUnknownElement</span><span class="sxs-lookup"><span data-stu-id="ae2dd-103">TabbedToUnknownElement</span></span>

## <a name="text"></a><span data-ttu-id="ae2dd-104">Texte</span><span class="sxs-lookup"><span data-stu-id="ae2dd-104">Text</span></span>

<span data-ttu-id="ae2dd-105">La tabulation est passée à un élément en dehors du HWND cible.</span><span class="sxs-lookup"><span data-stu-id="ae2dd-105">Tabbing has gone to an element outside the target hwnd.</span></span>

## <a name="type"></a><span data-ttu-id="ae2dd-106">Type</span><span class="sxs-lookup"><span data-stu-id="ae2dd-106">Type</span></span>

<span data-ttu-id="ae2dd-107">Error</span><span class="sxs-lookup"><span data-stu-id="ae2dd-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="ae2dd-108">Description</span><span class="sxs-lookup"><span data-stu-id="ae2dd-108">Description</span></span>

<span data-ttu-id="ae2dd-109">L’utilisation de la navigation au clavier standard (Tab ou Maj + Tab) entraîne le déplacement du focus en dehors du HWND de la cible de vérification.</span><span class="sxs-lookup"><span data-stu-id="ae2dd-109">Using standard keyboard navigation (Tab or Shift+Tab) causes focus to shift outside the HWND of the verification target.</span></span>

<span data-ttu-id="ae2dd-110">AccChecker déplace l’arborescence d’éléments vers le HWND de niveau supérieur pour la cible de vérification choisie avant d’exécuter des tâches de vérification.</span><span class="sxs-lookup"><span data-stu-id="ae2dd-110">AccChecker moves up the element tree to the top-level HWND for the chosen verification target before running any verification tasks.</span></span> <span data-ttu-id="ae2dd-111">Cela réduit le nombre d’erreurs fausses générées si un HWND choisi pour la vérification fait partie d’une zone client plus complexe.</span><span class="sxs-lookup"><span data-stu-id="ae2dd-111">This reduces the number of spurious errors generated if an HWND chosen for verification is part of a more complex client area.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ae2dd-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="ae2dd-112">Possible causes</span></span>

-   <span data-ttu-id="ae2dd-113">La cible de vérification n’a pas besoin d’une implémentation de tabulation pour fournir des fonctionnalités complètes.</span><span class="sxs-lookup"><span data-stu-id="ae2dd-113">The verification target doesn't require a tabbing implementation to provide full functionality.</span></span>
-   <span data-ttu-id="ae2dd-114">L’interaction de l’utilisateur pendant la vérification, telle que le déplacement du focus vers un HWND non cible, interfère avec le processus de vérification.</span><span class="sxs-lookup"><span data-stu-id="ae2dd-114">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>

 

 




