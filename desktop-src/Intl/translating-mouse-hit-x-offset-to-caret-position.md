---
description: De façon conventionnelle, l’utilisateur peut sélectionner la position du signe insertion (CP) en cliquant sur la moitié de caractères de fin &\# 0034 ; CP-1&\# 0034 ; ou sur la moitié de caractères de début &\# 0034 ; CP&\# 0034 ;.
ms.assetid: 36b6ff00-7ea8-40e5-90f7-917cef117d4a
title: Translation de l’offset X de l’accès à la souris à la position du signe insertion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f993de35ebffac4740b367927d1a8edf864a813e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121813"
---
# <a name="translating-mouse-hit-x-offset-to-caret-position"></a>Translation de l’offset X de l’accès à la souris à la position du signe insertion

De façon conventionnelle, l’utilisateur peut sélectionner la position du signe insertion (CP) en cliquant soit sur la moitié de caractères de fin du caractère « CP-1 », soit sur la moitié du caractère « CP ». Une application peut implémenter la translation de l’offset de la souris x à l’emplacement du signe insertion comme suit :


```C++
int iCharPos;
int iCaretPos;
int fTrailing;
ScriptXtoCP(iMouseX, cChars, cGlyphs, pwLogClust, psva, piAdvance, psa,
            &iCharPos, &fTrailing);
iCaretPos = iCharPos + fTrailing;
```



Pour les scripts qui alignent le signe insertion sur les limites du cluster, un appel à [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) retourne avec *fTrailing* défini sur 0 ou sur la largeur du cluster en points de code.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



