---
title: Contrôle graphique OpenGL
description: Contrôle graphique OpenGL
ms.assetid: 327f2920-1bc9-4de7-aa12-3e9f74a94759
keywords:
- OpenGL, contrôle graphique
- contrôle graphique OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6bb138a2d8c597fae2d92a1d1394c8ff05b03cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673266"
---
# <a name="opengl-graphic-control"></a><span data-ttu-id="ed2d0-105">Contrôle graphique OpenGL</span><span class="sxs-lookup"><span data-stu-id="ed2d0-105">OpenGL Graphic Control</span></span>

<span data-ttu-id="ed2d0-106">OpenGL vous offre un contrôle relativement direct sur les opérations fondamentales des graphiques en deux et trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="ed2d0-106">OpenGL provides you with fairly direct control over the fundamental operations of two- and three-dimensional graphics.</span></span> <span data-ttu-id="ed2d0-107">Cela comprend la spécification des paramètres tels que les matrices de transformation, les coefficients d’équation d’éclairage, les méthodes d’anticrénelage et les opérateurs de mise à jour de pixels.</span><span class="sxs-lookup"><span data-stu-id="ed2d0-107">This includes specification of such parameters as transformation matrices, lighting equation coefficients, antialiasing methods, and pixel-update operators.</span></span> <span data-ttu-id="ed2d0-108">Toutefois, il ne vous fournit aucun moyen de décrire ou de modéliser des objets géométriques complexes.</span><span class="sxs-lookup"><span data-stu-id="ed2d0-108">However, it doesn't provide you with a means for describing or modeling complex geometric objects.</span></span> <span data-ttu-id="ed2d0-109">Ainsi, les commandes OpenGL que vous émettez spécifient la façon dont un résultat donné doit être produit (quelle procédure doit être suivie) plutôt que ce qui doit ressembler exactement à ce résultat.</span><span class="sxs-lookup"><span data-stu-id="ed2d0-109">Thus, the OpenGL commands you issue specify how a certain result should be produced (what procedure should be followed) rather than what exactly that result should look like.</span></span> <span data-ttu-id="ed2d0-110">Autrement dit, OpenGL est fondamentalement procédural plutôt que descriptif.</span><span class="sxs-lookup"><span data-stu-id="ed2d0-110">That is, OpenGL is fundamentally procedural rather than descriptive.</span></span> <span data-ttu-id="ed2d0-111">Pour comprendre parfaitement comment utiliser OpenGL, il est utile de connaître l’ordre dans lequel il effectue ses opérations.</span><span class="sxs-lookup"><span data-stu-id="ed2d0-111">To fully understand how to use OpenGL, it helps to know the order in which it carries out its operations.</span></span>

 

 




