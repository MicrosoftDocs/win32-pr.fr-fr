---
description: Chemins courbés
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Chemins courbés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863674"
---
# <a name="curved-paths"></a>Chemins courbés

Une application peut aplatir les courbes dans un chemin d’accès en appelant la fonction [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) . Cette fonction est particulièrement utile pour les applications qui tiennent du texte sur le contour d’un tracé qui contient des courbes. Pour ajuster le texte, l’application doit effectuer les étapes suivantes :

1.  Créez le chemin d’accès où le texte s’affiche.
2.  Appelez la fonction [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) pour convertir les courbes d’un tracé en segments de ligne.
3.  Appelez la fonction [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) pour récupérer ces segments de ligne.
4.  Calculez la longueur de chaque ligne et la largeur de chaque caractère de la chaîne.
5.  Utilisez les données de largeur de ligne et de largeur de caractère pour positionner chaque caractère le long de la courbe.

 

 



