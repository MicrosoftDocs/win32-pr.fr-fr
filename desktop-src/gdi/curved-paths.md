---
description: Chemins courbés
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Chemins courbés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58018b7ef95b30c5ae2751ed963caefee7b9313ca86a8c6a2a4fee246908f8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849179"
---
# <a name="curved-paths"></a>Chemins courbés

Une application peut aplatir les courbes dans un chemin d’accès en appelant la fonction [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) . Cette fonction est particulièrement utile pour les applications qui tiennent du texte sur le contour d’un tracé qui contient des courbes. Pour ajuster le texte, l’application doit effectuer les étapes suivantes :

1.  Créez le chemin d’accès où le texte s’affiche.
2.  Appelez la fonction [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) pour convertir les courbes d’un tracé en segments de ligne.
3.  Appelez la fonction [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) pour récupérer ces segments de ligne.
4.  Calculez la longueur de chaque ligne et la largeur de chaque caractère de la chaîne.
5.  Utilisez les données de largeur de ligne et de largeur de caractère pour positionner chaque caractère le long de la courbe.

 

 



