---
title: Commentaires
description: En mode commentaires, chaque primitive à pixelliser génère un bloc de valeurs qui est copié dans le tableau de commentaires.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- mode commentaires, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531459"
---
# <a name="feedback-mode"></a><span data-ttu-id="14544-104">Mode Commentaires</span><span class="sxs-lookup"><span data-stu-id="14544-104">Feedback mode</span></span>

<span data-ttu-id="14544-105">En mode commentaires, chaque primitive à pixelliser génère un bloc de valeurs qui est copié dans le tableau de commentaires.</span><span class="sxs-lookup"><span data-stu-id="14544-105">In feedback mode, each primitive to be rasterized generates a block of values that is copied into the feedback array.</span></span> <span data-ttu-id="14544-106">Fournissez ce tableau avec [**glFeedbackBuffer**](glfeedbackbuffer.md), que vous devez appeler avant de placer OpenGL en mode commentaires.</span><span class="sxs-lookup"><span data-stu-id="14544-106">Supply this array with [**glFeedbackBuffer**](glfeedbackbuffer.md), which you must call before putting OpenGL into feedback mode.</span></span> <span data-ttu-id="14544-107">Chaque bloc de valeurs commence par un code qui indique le type primitif, suivi de valeurs qui décrivent les vertex de la primitive et les données associées.</span><span class="sxs-lookup"><span data-stu-id="14544-107">Each block of values begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="14544-108">Les entrées sont également écrites pour les bitmaps et les rectangles de pixels.</span><span class="sxs-lookup"><span data-stu-id="14544-108">Entries are also written for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="14544-109">Il n’est pas garanti que les valeurs soient écrites dans le tableau de commentaires tant que vous n’avez pas appelé [**glRenderMode**](glrendermode.md) pour prendre en charge l’extraction en mode feedback.</span><span class="sxs-lookup"><span data-stu-id="14544-109">Values are not guaranteed to be written into the feedback array until you call [**glRenderMode**](glrendermode.md) to take OpenGL out of feedback mode.</span></span> <span data-ttu-id="14544-110">Vous pouvez utiliser [**glPassThrough**](glpassthrough.md) pour fournir un marqueur renvoyé en mode Feedback comme s’il s’agissait d’une primitive.</span><span class="sxs-lookup"><span data-stu-id="14544-110">You can use [**glPassThrough**](glpassthrough.md) to supply a marker that is returned in feedback mode as if it were a primitive.</span></span>

 

 




