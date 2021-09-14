---
title: Marqueurs
description: Marqueurs
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK, marqueurs
- ASF (Advanced Systems Format), marqueurs
- ASF (format des systèmes avancés), marqueurs
- marqueurs, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234605"
---
# <a name="markers"></a>Marqueurs

Les marqueurs sont des emplacements nommés sur la chronologie d’un fichier ASF. Chaque marqueur a un nom et une heure de présentation que vous attribuez. Vous pouvez spécifier autant de marqueurs que nécessaire pour un fichier.

Les marqueurs sont utiles pour fractionner des fichiers ASF volumineux en éléments logiques. Une application qui utilise l’objet lecteur pour lire des fichiers ASF peut fournir à l’utilisateur la possibilité de passer d’un marqueur à un marqueur, ce qui simplifie la navigation dans les médias numériques. Par exemple, si vous créez un fichier ASF en dehors d’une présentation, vous pouvez placer des marqueurs dans la chronologie pour chaque sujet principal abordé. Lors de la lecture, au lieu d’obtenir une chronologie longue et de deviner à l’emplacement à rechercher, un utilisateur peut simplement choisir une rubrique dans une liste et aller directement à la partie pertinente du fichier.

Les marqueurs sont manipulés par l’objet de l’éditeur de métadonnées. Vous pouvez ajouter, supprimer et afficher les marqueurs dans un fichier à tout moment une fois que le fichier a été écrit.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Pour rechercher des marqueurs**](to-seek-to-markers.md)
</dt> <dt>

[**Utilisation des marqueurs**](using-markers.md)
</dt> </dl>

 

 




