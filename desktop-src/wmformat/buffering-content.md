---
title: Mise en mémoire tampon du contenu
description: Mise en mémoire tampon du contenu
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media Format SDK, mise en mémoire tampon du contenu
- mise en mémoire tampon du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511202"
---
# <a name="buffering-content"></a>Mise en mémoire tampon du contenu

Lorsque l’objet lecteur ouvre un fichier de diffusion en continu, il détermine la taille de la mémoire tampon en fonction des paramètres de l’en-tête du fichier. Vous pouvez considérer la mémoire tampon comme un compartiment avec un trou dans le bas, ce qui entraîne une fuite à une vitesse constante. Tant que la vitesse à laquelle le compartiment est rempli n’est pas, en moyenne, supérieure à la vitesse à laquelle elle subit des fuites, le compartiment ne risque jamais de déborder.

La vitesse à laquelle le compartiment imaginaire perd est la vitesse de transmission du flux. La vitesse de remplissage du compartiment correspond à la vitesse de transmission en continu réelle. Les données d’un flux compressé varient en fonction de la taille de l’échantillon à échantillonner en fonction du volume de compression atteint. Ainsi, même si la vitesse de transmission du flux est définie dans le profil, elle représente la vitesse de transmission moyenne, et non une constante.

L’autre paramètre de flux important pour le processus de mise en mémoire tampon est la fenêtre de mémoire tampon. La fenêtre de mémoire tampon est mesurée dans le temps et spécifie la quantité de contenu qui peut être mise en mémoire tampon. La capacité du compartiment imaginaire peut être trouvée à l’aide de la fenêtre de mémoire tampon. Par exemple, si vous avez un flux avec une vitesse de transmission de 32 kbit/s et une fenêtre de mémoire tampon de 3 secondes, la mémoire tampon est dimensionnée de façon à contenir 3 secondes de contenu de 32 kbps, soit 12 000 octets (32 000 bits par seconde x 3 secondes/8 bits par octet). Le codec limite la variation entre la vitesse de transmission en continu réelle des échantillons encodés afin qu’au cours d’une période égale à la fenêtre de la mémoire tampon, la vitesse de transmission moyenne ne soit pas supérieure à la vitesse de transmission du flux.

Normalement, vous définissez la vitesse de transmission et la fenêtre de mémoire tampon d’un flux dans un profil, et l’enregistreur gère le reste. Toutefois, lorsque vous passez des échantillons compressés au lecteur, vous devez vous assurer que les valeurs correctes sont transférées vers le nouveau fichier en définissant la vitesse de transmission et la fenêtre de mémoire tampon pour le flux du profil de destination sur les valeurs du flux compressé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](concepts.md)
</dt> <dt>

[**Exemples de supports**](media-samples.md)
</dt> <dt>

[**Entrées, flux et sorties**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




