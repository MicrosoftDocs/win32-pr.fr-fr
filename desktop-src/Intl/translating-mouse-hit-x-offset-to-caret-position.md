---
description: De façon conventionnelle, l’utilisateur peut sélectionner la position du signe insertion (CP) en cliquant sur la moitié de caractères de fin &\# 0034 ; CP-1&\# 0034 ; ou sur la moitié de caractères de début &\# 0034 ; CP&\# 0034 ;.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Translation de l’offset X de l’accès à la souris à la position du signe insertion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f993de35ebffac4740b367927d1a8edf864a813e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865485"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a><span data-ttu-id="2b397-103">Translation de l’offset X de l’accès à la souris à la position du signe insertion</span><span class="sxs-lookup"><span data-stu-id="2b397-103">Translating Mouse Hit X Offset to Caret Position</span></span>

<span data-ttu-id="2b397-104">De façon conventionnelle, l’utilisateur peut sélectionner la position du signe insertion (CP) en cliquant soit sur la moitié de caractères de fin du caractère « CP-1 », soit sur la moitié du caractère « CP ».</span><span class="sxs-lookup"><span data-stu-id="2b397-104">Conventionally, the user can select caret position (cp) by clicking either the trailing half of character "cp-1" or the leading half of character "cp".</span></span> <span data-ttu-id="2b397-105">Une application peut implémenter la translation de l’offset de la souris x à l’emplacement du signe insertion comme suit :</span><span class="sxs-lookup"><span data-stu-id="2b397-105">An application can implement the translation of mouse hit x offset to caret position as follows:</span></span>


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



<span data-ttu-id="2b397-106">Pour les scripts qui alignent le signe insertion sur les limites du cluster, un appel à [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) retourne avec *fTrailing* défini sur 0 ou sur la largeur du cluster en points de code.</span><span class="sxs-lookup"><span data-stu-id="2b397-106">For scripts that snap the caret to cluster boundaries, a call to [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) returns with *fTrailing* set to either 0 or the width of the cluster in code points.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b397-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b397-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b397-108">Utilisation de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="2b397-108">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



