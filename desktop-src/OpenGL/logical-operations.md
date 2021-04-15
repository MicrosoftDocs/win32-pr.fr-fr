---
title: Opérations logiques
description: Une opération logique peut être appliquée entre le fragment et la valeur stockée à l’emplacement correspondant dans le trame ; le résultat remplace la valeur trame actuelle.
ms.assetid: 0d1ea309-e86b-4aff-87ac-9d9d5909c2ce
keywords:
- Pipeline de traitement OpenGL, opérations logiques
- opérations logiques OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3736f9a06892e652825a7232aa087eb8b4832f20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507167"
---
# <a name="logical-operations"></a><span data-ttu-id="aaf04-105">Opérations logiques</span><span class="sxs-lookup"><span data-stu-id="aaf04-105">Logical Operations</span></span>

<span data-ttu-id="aaf04-106">Une opération logique peut être appliquée entre le fragment et la valeur stockée à l’emplacement correspondant dans le trame ; le résultat remplace la valeur trame actuelle.</span><span class="sxs-lookup"><span data-stu-id="aaf04-106">A logical operation can be applied between the fragment and the value stored at the corresponding location in the framebuffer; the result replaces the current framebuffer value.</span></span> <span data-ttu-id="aaf04-107">Vous choisissez l’opération logique souhaitée avec [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="aaf04-107">You choose the desired logical operation with [**glLogicOp**](gllogicop.md).</span></span> <span data-ttu-id="aaf04-108">Les opérations logiques sont effectuées uniquement sur les index de couleur, jamais sur les valeurs RVBA.</span><span class="sxs-lookup"><span data-stu-id="aaf04-108">Logical operations are performed only on color indexes, never on RGBA values.</span></span>

 

 




