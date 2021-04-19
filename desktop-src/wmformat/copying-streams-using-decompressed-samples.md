---
title: Copie de flux à l’aide d’exemples décompressés
description: Copie de flux à l’aide d’exemples décompressés
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows Media Format SDK, copie de flux
- ASF (Advanced Systems Format), copie de flux
- ASF (format de systèmes avancés), copie de flux
- flux, copie à l’aide de données décompressées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106544144"
---
# <a name="copying-streams-using-decompressed-samples"></a>Copie de flux à l’aide d’exemples décompressés

Il est fortement recommandé de ne pas copier les flux d’un fichier vers un autre à l’aide d’exemples décompressés. Le processus de décompression et de recompression des exemples entraîne une dégradation de la qualité de la sortie. Si vous avez besoin de décompresser vos exemples, puis de les copier dans un autre flux, vous risquez de rencontrer des difficultés avec les flux codés en fonction de la vitesse de transmission variable (VBR).

Lorsque le codec finit de compresser un flux VBR basé sur la qualité, il enregistre la vitesse de transmission et la fenêtre de mémoire tampon du contenu résultant. Quand vous lisez un fichier contenant un flux encodé à l’aide de la fonction VBR basée sur la qualité, le profil obtenu à partir du lecteur indique la vitesse de transmission et la fenêtre de mémoire tampon, ainsi que la vitesse de transmission maximale et la fenêtre de mémoire tampon maximale. Cette configuration dans le profil signifie normalement un flux de vitesse de transmission variable à vitesse de transmission. Par conséquent, lorsque vous définissez le profil sur le writer, il s’attend à obtenir une passe de prétraitement pour le flux, car les flux VBR à vitesse de transmission requièrent un encodage en deux passes. Vous devez traiter le flux comme s’il s’agissait d’un flux VBR à vitesse de transmission restreinte et remettre les exemples pour le prétraitement. Étant donné que vous utilisez les valeurs retournées après l’encodage du contenu à un niveau de qualité particulier, ces valeurs représentent le niveau de qualité souhaité. Bien entendu, la qualité de la sortie ré-encodée sera tout de même dégradée, en raison de la nouvelle encodage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Copie de données d’un fichier vers un autre**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copie de flux sans décompression des données**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




