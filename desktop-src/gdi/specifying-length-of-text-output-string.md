---
description: Plusieurs fonctions de police et de sortie de texte ont un paramètre qui spécifie la longueur de la chaîne de sortie de texte. Un exemple typique est le paramètre cchText de DrawTextEx.
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: Spécification de la longueur de la chaîne de sortie de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c120026d1b65170b6fe35bc65400280f6f1ffa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518492"
---
# <a name="specifying-length-of-text-output-string"></a>Spécification de la longueur de la chaîne de sortie de texte

Plusieurs fonctions de police et de sortie de texte ont un paramètre qui spécifie la longueur de la chaîne de sortie de texte. Un exemple typique est le paramètre *cchText* de [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa).

Chacune de ces fonctions a une version « ANSI » et une version Unicode (par exemple, [**DrawTextExA**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) et **DrawTextExW**, respectivement). Pour la version « ANSI » de chaque fonction, la longueur est spécifiée sous la forme d’un nombre d’octets et pour la fonction Unicode, elle est spécifiée en tant que nombre de mots.

Il est traditionnel de considérer qu’il s’agit d’un « nombre de caractères ». Cela est généralement précis pour de nombreuses langues, y compris l’anglais, mais elle n’est pas précise en général. Dans les chaînes « ANSI », les caractères des pages de codes [SBCS](../intl/single-byte-character-sets.md) prennent un octet chacun, mais la plupart des caractères des pages de codes [DBCS](../intl/double-byte-character-sets.md) prennent deux octets. De même, les caractères Unicode les plus couramment définis résident dans le plan multilingue de base (BMP) et leurs représentations UTF-16 tiennent dans un mot, mais les caractères supplémentaires sont représentés en Unicode par des « substituts », qui requièrent deux mots.

Chacune de ces fonctions prend un nombre de longueur. Pour la version « ANSI » de chaque fonction, la longueur est spécifiée en tant que longueur du nombre d’octets d’une chaîne qui n’inclut pas la marque de fin **null** . Pour la fonction Unicode, le nombre de longueur est le nombre d’octets divisé par sizeof (WCHAR), qui est 2, à l’exclusion de la marque de fin **null** . Le nombre de caractères est le nombre de caractères, qui peut ne pas être égal au nombre de longueur de la chaîne. Dans certains cas, les caractères prennent plus d’un octet pour ANSI (par exemple, un caractère [DBCS](../intl/double-byte-character-sets.md) ) et plus d’un mot pour Unicode (par exemple, des caractères de substitution). En outre, le nombre de glyphes peut ne pas être égal au nombre de caractères, car plusieurs caractères peuvent être composés pour créer un glyphe. Le nombre de durées correspond à la quantité de données. Le nombre de caractères est le nombre d’unités traitées comme une entité unique. Les glyphes sont les éléments rendus. Par exemple, dans Unicode, vous pouvez avoir une chaîne dont la longueur est égale à 3, ce qui correspond à 2 caractères et qui entraîne le rendu de 1 glyphe. Toutefois, en général, la plupart des chaînes Unicode, le nombre de caractères et le nombre de glyphes rendus sont égaux.

Vous pouvez utiliser \_ tcslen () pour récupérer la longueur de chaîne. Pour ANSI, \_ tcslen () retourne le nombre d’octets. Pour Unicode, \_ tcslen () retourne le nombre de WCHARs (autrement dit, des mots).

Les caractères de traitement spéciaux, tels que les tabulations et les traits d’union conditionnels qui ne sont pas toujours dessinés, peuvent affecter la sortie dessinée. Ils sont inclus dans la longueur de chaîne et les nombres de caractères, mais ils ne peuvent pas être représentés directement par un glyphe rendu.

Certaines de ces fonctions permettent à l’appelant de spécifier une longueur de-1 pour indiquer que la chaîne se termine par un caractère null ; dans ce cas, la fonction calcule automatiquement le nombre de caractères. Toutes les fonctions ne proposent pas cette fonctionnalité. Spécifié sur une base fonction par fonction ; consultez la documentation de chaque fonction.

 

 
