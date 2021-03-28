---
description: L’attribut pattern spécifie le modèle d’un stylet géométrique.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Modèle Pen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528299"
---
# <a name="pen-pattern"></a><span data-ttu-id="c3174-103">Modèle Pen</span><span class="sxs-lookup"><span data-stu-id="c3174-103">Pen Pattern</span></span>

<span data-ttu-id="c3174-104">L’attribut pattern spécifie le modèle d’un stylet géométrique.</span><span class="sxs-lookup"><span data-stu-id="c3174-104">The pattern attribute specifies the pattern of a geometric pen.</span></span>

<span data-ttu-id="c3174-105">L’illustration suivante montre des lignes dessinées avec différents stylets géométriques.</span><span class="sxs-lookup"><span data-stu-id="c3174-105">The following illustration shows lines drawn with different geometric pens.</span></span> <span data-ttu-id="c3174-106">Chaque stylo a été créé à l’aide d’un attribut de modèle différent.</span><span class="sxs-lookup"><span data-stu-id="c3174-106">Each pen was created using a different pattern attribute.</span></span>

![Illustration montrant quatre lignes, chacune remplie d’un stylet différent](images/cspen-02.png)

<span data-ttu-id="c3174-108">La première ligne de l’illustration précédente est dessinée à l’aide de l’un des six modèles de hachures disponibles ; Pour plus d’informations sur les modèles de hachurage, consultez [Pen Hatch](pen-hatch.md).</span><span class="sxs-lookup"><span data-stu-id="c3174-108">The first line in the previous illustration is drawn using one of the six available hatch patterns; for more information about hatch patterns, see [Pen Hatch](pen-hatch.md).</span></span> <span data-ttu-id="c3174-109">La ligne suivante est dessinée à l’aide du modèle creux, identique au modèle null.</span><span class="sxs-lookup"><span data-stu-id="c3174-109">The next line is drawn using the hollow pattern, identical to the null pattern.</span></span> <span data-ttu-id="c3174-110">La troisième ligne est dessinée à l’aide d’un modèle personnalisé créé à partir d’une bitmap de 8 par 8 pixels.</span><span class="sxs-lookup"><span data-stu-id="c3174-110">The third line is drawn using a custom pattern created from an 8-by-8-pixel bitmap.</span></span> <span data-ttu-id="c3174-111">(Pour plus d’informations sur les bitmaps et leur création, consultez [bitmaps](bitmaps.md).) La dernière ligne est dessinée à l’aide d’un modèle Uni.</span><span class="sxs-lookup"><span data-stu-id="c3174-111">(For more information about bitmaps and their creation, see [Bitmaps](bitmaps.md).) The last line is drawn using a solid pattern.</span></span> <span data-ttu-id="c3174-112">La création d’un pinceau et le passage de son handle à la fonction [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) créent un modèle.</span><span class="sxs-lookup"><span data-stu-id="c3174-112">Creating a brush and passing its handle to the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function creates a pattern.</span></span>

 

 



