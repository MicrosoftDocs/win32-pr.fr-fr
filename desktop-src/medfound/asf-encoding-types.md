---
description: Types d’encodage ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Types d’encodage ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530861"
---
# <a name="asf-encoding-types"></a>Types d’encodage ASF

Les méthodes d’encodage se concentrent sur la mémoire tampon utilisée par l’encodeur pour gérer les données d’entrée non compressées. Cette mémoire tampon est définie par la vitesse de transmission du flux, en bits par seconde, et la fenêtre de mémoire tampon, en millisecondes. lors de l’encodage de fichiers ASF, les encodeurs de média Windows respectent les contraintes de la mémoire tampon. Pour plus d’informations sur la fenêtre de mémoire tampon, consultez [le modèle de tampon de compartiment](the-leaky-bucket-buffer-model.md)perdu. Savoir quand et comment utiliser chaque méthode peut vous aider à créer du contenu compressé de haute qualité. Le tableau suivant contient des liens vers des rubriques relatives à chacune des méthodes d’encodage disponibles qu’une application peut utiliser pour encoder les données multimédias en ASF.



| Méthode de codage                                                                                      | Description                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Encodage à vitesse binaire constante](constant-bit-rate-encoding.md)                                         | L’encodeur compresse les données à une vitesse de transmission spécifiée.                                                                                                                                                     |
| [Encodage de la vitesse de transmission variable basée sur la qualité](quality-based-variable-bit-rate--vbr--encoding.md)       | L’encodeur compresse les données à une valeur de qualité particulière afin que la qualité du média encodé soit cohérente tout au long de sa durée, indépendamment des exigences de mémoire tampon du flux résultant. |
| [Encodage de la vitesse de transmission variable sans contrainte](unconstrained-variable-bit-rate--vbr--encoding.md)       | L’encodeur compresse les données à la meilleure qualité possible tout en conservant une vitesse de transmission spécifiée. Ce mode est également appelé encodage VBR (variable bit rate) à 2 passes.                                    |
| [Chiffrement à vitesse de transmission variable à forte limite](peak-constrained-variable-bit-rate--vbr--encoding.md) | L’encodeur compresse les données à une vitesse de transmission spécifiée tout en conservant les valeurs de mémoire tampon dans la fenêtre de mémoire tampon maximale et la vitesse de transmission spécifiées. Ce mode est également appelé 2-passe pic VBR.                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Encodeurs multimédias](windows-media-encoders.md)
</dt> </dl>

 

 



