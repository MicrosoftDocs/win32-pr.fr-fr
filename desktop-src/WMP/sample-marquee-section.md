---
title: Exemple de section de texte défilant
description: Exemple de section de texte défilant
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Windows Media Player Mobile Skins, palissades
- apparences, rectangles de sélection
- informations de référence sur les habillages, les cadres
- textes défilant dans les enveloppes, section de texte défilant
- fichiers de définition d’apparence, section de texte défilant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462387"
---
# <a name="sample-marquee-section"></a>Exemple de section de texte défilant

Les lignes suivantes affichent une section de texte défilant standard d’un fichier de définition d’apparence :


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



Cela définit une zone d’affichage de texte défilant qui affiche le titre et l’auteur si les deux sont définis, le titre si seul le titre est défini, ou le nom de l’auteur si seul l’auteur est défini. Si aucun n’est défini, rien ne s’affiche.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Chapiteau**](marquee.md)
</dt> </dl>

 

 




