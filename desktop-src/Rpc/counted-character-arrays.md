---
title: Tableaux de caractères comptés
description: L’attribut \ size \_ is \ indique la limite supérieure du tableau, tandis que l' \_ attribut \ length est \ indique le nombre d’éléments de tableau à transmettre.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463410"
---
# <a name="counted-character-arrays"></a><span data-ttu-id="14142-103">Tableaux de caractères comptés</span><span class="sxs-lookup"><span data-stu-id="14142-103">Counted Character Arrays</span></span>

<span data-ttu-id="14142-104">L' \[ attribut [size \_ is](/windows/desktop/Midl/size-is) \] indique la limite supérieure du tableau, tandis que la \[ [longueur \_ est](/windows/desktop/Midl/length-is) \] attribute indique le nombre d’éléments de tableau à transmettre.</span><span class="sxs-lookup"><span data-stu-id="14142-104">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute indicates the upper bound of the array while the \[ [length\_is](/windows/desktop/Midl/length-is)\] attribute indicates the number of array elements to transmit.</span></span> <span data-ttu-id="14142-105">En plus du tableau, le prototype de procédure distante doit inclure toutes les variables représentant la longueur ou la taille qui déterminent les éléments du tableau transmis (ils peuvent être des paramètres distincts ou regroupés avec la chaîne dans une structure).</span><span class="sxs-lookup"><span data-stu-id="14142-105">In addition to the array, the remote procedure prototype must include any variables representing length or size that determine the transmitted array elements (they can be separate parameters or bundled with the string in a structure).</span></span> <span data-ttu-id="14142-106">Ces attributs peuvent être utilisés avec des tableaux de caractères à caractères larges ou codés sur un octet de la même manière qu’avec des tableaux d’autres types.</span><span class="sxs-lookup"><span data-stu-id="14142-106">These attributes can be used with wide-character or single-byte character arrays just as they would be with arrays of other types.</span></span>

<span data-ttu-id="14142-107">Les informations contenues dans cette section décrivent les prototypes de paramètres de procédure distante pour les tableaux de caractères.</span><span class="sxs-lookup"><span data-stu-id="14142-107">The information in this section describes remote procedure parameter prototypes for character arrays.</span></span> <span data-ttu-id="14142-108">Elle est composée des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="14142-108">It is divided into the following topics:</span></span>

-   <span data-ttu-id="14142-109">[\[in, out, la taille \_ est un \] prototype](-in-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="14142-109">[\[in, out, size\_is\] Prototype](-in-out-size-is-prototype.md)</span></span>
-   <span data-ttu-id="14142-110">[\[dans, la taille \_ est et sortante, la taille \_ est un \] prototype](-in-size-is-and-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="14142-110">[\[in, size\_is and out, size\_is\] Prototype](-in-size-is-and-out-size-is-prototype.md)</span></span>

 

 