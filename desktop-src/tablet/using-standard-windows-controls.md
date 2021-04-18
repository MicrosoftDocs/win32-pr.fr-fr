---
description: Utilisez des contrôles Windows standard chaque fois que cela est possible, car ils sont entièrement compatibles avec les recommandations de Microsoft Active Accessibility. Cela comprend les contrôles fournis par Windows (User32.dll) et la bibliothèque de contrôles communs Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Utilisation des contrôles Windows standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318290"
---
# <a name="using-standard-windows-controls"></a><span data-ttu-id="7b0f5-104">Utilisation des contrôles Windows standard</span><span class="sxs-lookup"><span data-stu-id="7b0f5-104">Using Standard Windows Controls</span></span>

<span data-ttu-id="7b0f5-105">Utilisez des contrôles Windows standard chaque fois que cela est possible, car ils sont entièrement compatibles avec les recommandations de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="7b0f5-105">Use standard Windows controls whenever possible, because they are fully compatible with Microsoft Active Accessibility guidelines.</span></span> <span data-ttu-id="7b0f5-106">Cela comprend les contrôles fournis par Windows (User32.dll) et la bibliothèque de contrôles communs Windows (Comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="7b0f5-106">This includes controls provided by Windows (User32.dll) and the Windows common controls library (Comctl32.dll).</span></span>

<span data-ttu-id="7b0f5-107">Chaque contrôle Windows standard est une fenêtre distincte d’une classe spécifique. l’aide à l’accessibilité est donc notifiée lorsque le focus se déplace vers un nouveau contrôle.</span><span class="sxs-lookup"><span data-stu-id="7b0f5-107">Each standard Windows control is a separate window of a specific class, so the accessibility aid is notified when the focus moves to a new control.</span></span> <span data-ttu-id="7b0f5-108">L’aide peut déterminer la classe de fenêtre de contrôles et tous les messages supplémentaires qu’elle peut envoyer pour interroger ou modifier l’état des contrôles.</span><span class="sxs-lookup"><span data-stu-id="7b0f5-108">The aid can determine the controls window class, and any additional messages it can send to query or alter the controls state.</span></span> <span data-ttu-id="7b0f5-109">L’aide peut également identifier tous les contrôles enfants contenus dans une fenêtre parente et identifier le parent de n’importe quel contrôle.</span><span class="sxs-lookup"><span data-stu-id="7b0f5-109">The aid can also identify all of the child controls contained within a parent window and identify the parent of any control.</span></span>

<span data-ttu-id="7b0f5-110">Certains contrôles communs sont extrêmement flexibles et peuvent souvent remplacer des contrôles personnalisés moins accessibles et des contrôles owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="7b0f5-110">Some common controls are extremely flexible and can often substitute for less-accessible custom controls and owner-drawn controls.</span></span> <span data-ttu-id="7b0f5-111">Par exemple, un affichage de liste peut remplacer une zone de liste owner-drawn pour afficher une case à cocher en regard de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="7b0f5-111">For example, a list view can replace an owner-drawn list box to display a check box next to each item.</span></span> <span data-ttu-id="7b0f5-112">En guise d’autre exemple, le contrôle de bouton amélioré peut afficher à la fois des images et du texte.</span><span class="sxs-lookup"><span data-stu-id="7b0f5-112">As another example, the enhanced button control can display both images and text.</span></span> <span data-ttu-id="7b0f5-113">Auparavant, cela nécessitait l’utilisation d’un contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7b0f5-113">Previously, this required the use of a custom control.</span></span>

 

 



