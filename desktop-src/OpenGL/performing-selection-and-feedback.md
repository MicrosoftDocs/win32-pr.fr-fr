---
title: Sélection et commentaires
description: Sélection et commentaires
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, sélection
- OpenGL, commentaires
- OpenGL, rendu
- mode de sélection OpenGL
- mode Commentaires OpenGL
- mode de rendu OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310038"
---
# <a name="performing-selection-and-feedback"></a><span data-ttu-id="811bc-109">Sélection et commentaires</span><span class="sxs-lookup"><span data-stu-id="811bc-109">Performing Selection and Feedback</span></span>

<span data-ttu-id="811bc-110">La sélection, les commentaires et le rendu sont des modes d’opération qui s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="811bc-110">Selection, feedback, and rendering are mutually exclusive modes of operation.</span></span> <span data-ttu-id="811bc-111">Le rendu est le mode par défaut normal pendant lequel les fragments sont produits par pixellisation.</span><span class="sxs-lookup"><span data-stu-id="811bc-111">Rendering is the normal, default mode during which fragments are produced by rasterization.</span></span>

<span data-ttu-id="811bc-112">En mode de sélection et de commentaires, aucun fragment n’est produit. par conséquent, aucune modification de trame ne se produit.</span><span class="sxs-lookup"><span data-stu-id="811bc-112">In selection and feedback modes, no fragments are produced; therefore, no framebuffer modification occurs.</span></span> <span data-ttu-id="811bc-113">En mode de sélection, vous pouvez déterminer les primitives qui seront dessinées dans une région d’une fenêtre. en mode commentaires, les informations sur les primitives qui seront pixellisées sont renvoyées à l’application.</span><span class="sxs-lookup"><span data-stu-id="811bc-113">In selection mode, you can determine which primitives will be drawn into some region of a window; in feedback mode, information about primitives that will be rasterized is fed back to the application.</span></span>

<span data-ttu-id="811bc-114">Vous pouvez choisir parmi ces trois modes avec [**glRenderMode**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="811bc-114">You select among these three modes with [**glRenderMode**](glrendermode.md).</span></span>

-   [<span data-ttu-id="811bc-115">Sélection</span><span class="sxs-lookup"><span data-stu-id="811bc-115">Selection</span></span>](selection.md)
-   [<span data-ttu-id="811bc-116">Commentaires</span><span class="sxs-lookup"><span data-stu-id="811bc-116">Feedback</span></span>](feedback.md)
-   [<span data-ttu-id="811bc-117">Référence de sélection et de commentaires</span><span class="sxs-lookup"><span data-stu-id="811bc-117">Selection and Feedback Reference</span></span>](selection-and-feedback-reference.md)

 

 




