---
description: Les cinq transformations de la page universelle peuvent être combinées en une seule matrice 3 par 3.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Transformations de l’espace universel vers la page combinées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972738"
---
# <a name="combined-world-to-page-space-transformations"></a><span data-ttu-id="c2287-103">Transformations de l’espace universel vers la page combinées</span><span class="sxs-lookup"><span data-stu-id="c2287-103">Combined World-to-Page Space Transformations</span></span>

<span data-ttu-id="c2287-104">Les cinq transformations de la page universelle peuvent être combinées en une seule matrice 3 par 3.</span><span class="sxs-lookup"><span data-stu-id="c2287-104">The five world-to-page transformations can be combined into a single 3-by-3 matrix.</span></span> <span data-ttu-id="c2287-105">La fonction [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) peut être utilisée pour combiner deux espaces universels avec les transformations d’espace de page.</span><span class="sxs-lookup"><span data-stu-id="c2287-105">The [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) function can be used to combine two world-space to page-space transformations.</span></span> <span data-ttu-id="c2287-106">Les transformations combinées peuvent être utilisées pour modifier la sortie associée à un contexte de périphérique (DC) particulier en appelant la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) et en fournissant les éléments de cette matrice.</span><span class="sxs-lookup"><span data-stu-id="c2287-106">The combined transformations can be used to alter output associated with a particular device context (DC) by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function and supplying the elements for this matrix.</span></span> <span data-ttu-id="c2287-107">Quand une application appelle **SetWorldTransform**, elle stocke les éléments de la matrice 3 par 3 dans une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="c2287-107">When an application calls **SetWorldTransform**, it stores the elements of the 3-by-3 matrix in an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span> <span data-ttu-id="c2287-108">Les membres de cette structure correspondent aux deux premières colonnes d’une matrice 3 par 3 ; la dernière colonne de la matrice n’est pas requise, car ses valeurs sont constantes.</span><span class="sxs-lookup"><span data-stu-id="c2287-108">The members of this structure correspond to the first two columns of a 3-by-3 matrix; the last column of the matrix is not required because its values are constant.</span></span>

<span data-ttu-id="c2287-109">Les éléments de la matrice de transformation universelle actuelle peuvent être réactifs en appelant la fonction [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) et en fournissant un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="c2287-109">The elements of the current world transformation matrix can be revived by calling the [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) function and supplying a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

 



