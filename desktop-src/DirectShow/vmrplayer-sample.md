---
description: Exemple VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Exemple VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6281147e2c140541ade480e5b2a5e0f0a1d4146dde59b4871441b68fec6f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071913"
---
# <a name="vmrplayer-sample"></a>Exemple VMRPlayer

## <a name="description"></a>Description

Cet exemple utilise le filtre de mixage vidéo 9 (VMR-9) pour mélanger alpha une ou deux vidéos en cours d’exécution et une image statique.

## <a name="usage"></a>Usage

Pour ouvrir la première vidéo, choisissez **ouvrir le flux principal** dans le menu **fichier** . Pour ouvrir une deuxième vidéo, choisissez **ouvrir un flux secondaire** dans le menu **fichier** (vous devez d’abord ouvrir le flux de données principal). Pour lire la vidéo, cliquez sur le bouton **lecture** .

Vous pouvez définir la position, la taille et les valeurs alpha des vidéos en sélectionnant **flux principal** ou **flux Secondard** dans le menu **Propriétés de VMR** .

Pour ajouter une image bitmap statique sur la vidéo, choisissez **image d’application statique** dans le menu **Propriétés de VMR** , puis cliquez sur la zone afficher l’image de l' **application** . Vous pouvez utiliser la même boîte de dialogue pour contrôler la position, la taille et la valeur alpha de la bitmap.

Pour capturer l’image vidéo fusionnée, choisissez **capturer l’image bitmap** dans le menu **Propriétés de VMR** .

Vous pouvez également spécifier le flux de l’image principale à partir de la ligne de commande :

**VMRPlayer** **/p** *nom_fichier*

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Extraits](directshow-samples.md)
</dt> </dl>

 

 



