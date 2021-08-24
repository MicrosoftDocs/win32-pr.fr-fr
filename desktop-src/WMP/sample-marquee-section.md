---
title: Exemple de section de texte défilant
description: Exemple de section de texte défilant
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Lecteur Windows Media Habillages mobiles, rectangles de sélection
- apparences, rectangles de sélection
- informations de référence sur les habillages, les cadres
- textes défilant dans les enveloppes, section de texte défilant
- fichiers de définition d’apparence, section de texte défilant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f8a3e013bb3a09a06f03715f0e7c4914e8e8d344c55843a643d5b8a9bf0479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508119"
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

 

 




