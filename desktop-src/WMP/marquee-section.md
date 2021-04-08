---
title: Section de texte défilant
description: Section de texte défilant
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Windows Media Player Mobile Skins, palissades
- apparences, rectangles de sélection
- création d’apparences, section de texte défilant
- écriture de code pour les apparences, section de texte défilant
- textes défilant dans les enveloppes, section de texte défilant
- fichiers de définition d’apparence, section de texte défilant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675878"
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
> Pour assurer la compatibilité avec les versions de Windows Media Player Mobile antérieures à Windows Media Player 10 mobile, l’utilisation de « marquis » dans un fichier de définition d’apparence est toujours considérée comme valide.

 

Pour plus d’informations sur la section de texte défilant, consultez [texte défilant](marquee.md) dans la référence d’apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture du code**](writing-the-code.md)
</dt> </dl>

 

 




