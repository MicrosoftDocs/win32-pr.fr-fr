---
title: Section de texte défilant
description: Section de texte défilant
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Lecteur Windows Media Habillages mobiles, rectangles de sélection
- apparences, rectangles de sélection
- création d’apparences, section de texte défilant
- écriture de code pour les apparences, section de texte défilant
- textes défilant dans les enveloppes, section de texte défilant
- fichiers de définition d’apparence, section de texte défilant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ddb53edd3f1efbbcbc5491604fd4022673b1234038770fcf44cd29ef4f3aca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123439"
---
# <a name="marquee-section"></a>Section de texte défilant

La section Marquee contient des informations sur la zone de texte Marquee, qui affiche le texte de défilement :


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



Le titre et l’auteur de l’élément multimédia actuel s’affichent, même si vous pouvez afficher n’importe quel type de texte dans le texte défilant. Par exemple, vous pouvez également inclure le nom de fichier, l’État et la sélection dans votre texte défilant.

> [!Note]  
> pour assurer la compatibilité avec les versions de Lecteur Windows Media mobile antérieur à Lecteur Windows Media 10 mobile, l’utilisation de « Marquis » dans un fichier de définition d’apparence est toujours considérée comme valide.

 

Pour plus d’informations sur la section de texte défilant, consultez [texte défilant](marquee.md) dans la référence d’apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture du code**](writing-the-code.md)
</dt> </dl>

 

 




