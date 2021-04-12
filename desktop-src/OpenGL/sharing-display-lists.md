---
title: Partage des listes d’affichage
description: Lorsque vous créez un contexte de rendu, il possède son propre espace de liste d’affichage.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL sur Windows, partage des listes d’affichage
- partage des listes d’affichage OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311074"
---
# <a name="sharing-display-lists"></a><span data-ttu-id="7a15e-105">Partage des listes d’affichage</span><span class="sxs-lookup"><span data-stu-id="7a15e-105">Sharing Display Lists</span></span>

<span data-ttu-id="7a15e-106">Lorsque vous créez un contexte de rendu, il possède son propre espace de liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="7a15e-106">When you create a rendering context, it has its own display-list space.</span></span> <span data-ttu-id="7a15e-107">La fonction [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) permet à un contexte de rendu de partager l’espace de liste d’affichage d’un autre contexte de rendu.</span><span class="sxs-lookup"><span data-stu-id="7a15e-107">The [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) function enables a rendering context to share the display-list space of another rendering context.</span></span> <span data-ttu-id="7a15e-108">Un nombre quelconque de contextes de rendu peut partager un seul espace de liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="7a15e-108">Any number of rendering contexts can share a single display-list space.</span></span>

 

 




