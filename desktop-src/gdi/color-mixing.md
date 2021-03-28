---
description: La combinaison de couleurs permet à une application de créer de nouvelles couleurs en combinant le stylet ou la couleur du pinceau avec les couleurs de l’image existante.
ms.assetid: 4a5dff8c-f75f-41d2-8367-33d97d4fd010
title: Mélange de couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa85f6ea449fa13f7b7120160915ea72a0e3dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114698"
---
# <a name="color-mixing"></a><span data-ttu-id="48bd8-103">Mélange de couleurs</span><span class="sxs-lookup"><span data-stu-id="48bd8-103">Color Mixing</span></span>

<span data-ttu-id="48bd8-104">La combinaison de couleurs permet à une application de créer de nouvelles couleurs en combinant le stylet ou la couleur du pinceau avec les couleurs de l’image existante.</span><span class="sxs-lookup"><span data-stu-id="48bd8-104">Color mixing lets an application create new colors by combining the pen or brush color with colors in the existing image.</span></span> <span data-ttu-id="48bd8-105">L’application peut choisir de dessiner le stylet ou la couleur du pinceau en l’État (dessinant efficacement sur une image existante) ou de mélanger la couleur aux couleurs déjà présentes.</span><span class="sxs-lookup"><span data-stu-id="48bd8-105">The application can choose either to draw the pen or brush color as is (effectively drawing over any existing image) or to mix the color with the colors already present.</span></span>

<span data-ttu-id="48bd8-106">Le mode de combinaison de premier plan, parfois appelé opération Raster binaire, détermine la façon dont ces couleurs sont mélangées.</span><span class="sxs-lookup"><span data-stu-id="48bd8-106">The foreground mix mode, sometimes called the binary raster operation, determines how these colors are mixed.</span></span> <span data-ttu-id="48bd8-107">Une application peut fusionner des couleurs, en préservant tous les composants des deux couleurs ; masquer les couleurs, supprimer ou modérer les composants qui ne sont pas courants ; ou masquez exclusivement les couleurs, en supprimant ou en modérant les composants qui sont courants.</span><span class="sxs-lookup"><span data-stu-id="48bd8-107">An application can merge colors, preserving all components of both colors; mask colors, removing or moderating components that are not common; or exclusively mask colors, removing or moderating components that are common.</span></span> <span data-ttu-id="48bd8-108">Il existe plusieurs variantes de ces opérations de mixage de base.</span><span class="sxs-lookup"><span data-stu-id="48bd8-108">There are several variations on these basic mixing operations.</span></span>

<span data-ttu-id="48bd8-109">Le mélange des couleurs est soumis à une approximation des couleurs.</span><span class="sxs-lookup"><span data-stu-id="48bd8-109">Color mixing is subject to color approximation.</span></span> <span data-ttu-id="48bd8-110">Si le résultat du mixage des couleurs est une couleur que l’appareil ne peut pas générer, le système se rapproche du résultat, en utilisant une couleur qu’il peut générer.</span><span class="sxs-lookup"><span data-stu-id="48bd8-110">If the result of color mixing is a color that the device cannot generate, the system approximates the result, using a color it can generate.</span></span> <span data-ttu-id="48bd8-111">Si une application combine des couleurs digénérées, les couleurs individuelles utilisées pour créer la couleur décomposée sont mélangées et les résultats sont soumis à une approximation des couleurs.</span><span class="sxs-lookup"><span data-stu-id="48bd8-111">If an application mixes dithered colors, the individual colors used to create the dithered color are mixed, and the results are subject to color approximation.</span></span>

<span data-ttu-id="48bd8-112">Une application définit le mode de combinaison de premier plan à l’aide de la fonction [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) et récupère le mode actuel à l’aide de la fonction [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) .</span><span class="sxs-lookup"><span data-stu-id="48bd8-112">An application sets the foreground mix mode by using the [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) function and retrieves the current mode by using the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) function.</span></span>

<span data-ttu-id="48bd8-113">Bien qu’il y ait un mode mixte en arrière-plan, ce mode ne contrôle pas la combinaison de couleurs.</span><span class="sxs-lookup"><span data-stu-id="48bd8-113">Although there is a background mix mode, that mode does not control the mixing of colors.</span></span> <span data-ttu-id="48bd8-114">Au lieu de cela, il spécifie si une couleur d’arrière-plan est utilisée lors du dessin de lignes stylisées, de pinceaux hachurés et de texte.</span><span class="sxs-lookup"><span data-stu-id="48bd8-114">Instead, it specifies whether a background color is used when drawing styled lines, hatched brushes, and text.</span></span>

 

 



