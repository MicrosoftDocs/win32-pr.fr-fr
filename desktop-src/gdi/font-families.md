---
description: Une famille de polices est un ensemble de polices ayant des caractéristiques de largeur de trait et d’empattement communes. Il existe cinq familles de polices. Une sixième famille permet à une application d’utiliser la police par défaut. Le tableau suivant décrit les familles de polices.
ms.assetid: 3c462000-4f65-43d0-8937-059081a8c417
title: Familles de polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfda200967b5efbf773fadc17d5093a856d0317
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521560"
---
# <a name="font-families"></a>Familles de polices

Une *famille de polices* est un ensemble de polices ayant des caractéristiques de largeur de trait et d’empattement communes. Il existe cinq familles de polices. Une sixième famille permet à une application d’utiliser la police par défaut. Le tableau suivant décrit les familles de polices.



| Famille de polices | Description                                                                                                                                   |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Décoratif  | Spécifie une police fantaisie. Par exemple, l’ancien est l’anglais.                                                                                          |
| Dontcare    | Spécifie un nom de famille générique. Ce nom est utilisé lorsque les informations sur une police n’existent pas ou n’ont pas d’importance. La police par défaut est utilisée. |
| Moderne      | Spécifie une police à espacement fixe avec ou sans empattements. Les polices à espacement fixe sont généralement modernes ; les exemples sont PICA, Elite et Courier New.         |
| $       | Spécifie une police proportionnelle avec empattements. Par exemple, Times New Roman.                                                                     |
| Script      | Spécifie une police conçue pour ressembler à l’écriture manuscrite. exemples : script et Cursive.                                              |
| Suisse       | Spécifie une police proportionnelle sans serifs. Par exemple, Arial.                                                                            |



 

Ces familles de polices correspondent à des constantes trouvées dans le fichier WinGDI. h : FF \_ décoratif, FF \_ dontcare, FF \_ moderne, FF \_ roman, FF \_ script et FF \_ Suisse. Une application utilise ces constantes lorsqu’elle crée une police, sélectionne une police ou récupère des informations sur une police.

Les polices au sein d’une famille se distinguent par leur taille (10 points, 24 points, etc.) et le style (normal, italique, etc.).

 

 



