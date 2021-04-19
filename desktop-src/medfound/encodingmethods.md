---
description: Méthodes d’encodage
ms.assetid: 17ab5ecc-0173-4c5c-9d65-40e506ab7e07
title: Méthodes d’encodage (Microsoft Media Foundation)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4366f11ea9d120d638c5600f84fc16f6c5320f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514557"
---
# <a name="encoding-methods-microsoft-media-foundation"></a>Méthodes d’encodage (Microsoft Media Foundation)

La plupart des codecs Windows Media Audio et vidéo prennent en charge plusieurs méthodes d’encodage. Savoir quand et comment utiliser chaque méthode peut vous aider à créer du contenu compressé de haute qualité.

Les méthodes d’encodage se concentrent sur la mémoire tampon utilisée par le décodeur pour gérer les données d’entrée compressées. Cette mémoire tampon est définie par la vitesse de transmission du flux, en bits par seconde, et la fenêtre de mémoire tampon, en millisecondes. Lors de l’encodage, le codec respecte les contraintes de la mémoire tampon. Pour plus d’informations sur la mémoire tampon, consultez [le modèle de tampon de compartiment avec fuite](the-leaky-bucket-buffer-model.md).

## <a name="constant-bit-rate-encoding"></a>Encodage à vitesse binaire constante

La vitesse de transmission de tout flux encodé par l’un des codecs Windows Media Audio et vidéo n’est pas constante. L’encodage CBR (constant bit rate) est, par conséquent, un terme trompeur. La fonctionnalité distinctive d’un flux encodé CBR est une petite fenêtre de mémoire tampon qui limite la variation de la taille des échantillons. L’encodage CBR est principalement utilisé pour le contenu diffusé en continu sur un réseau jusqu’à sa destination. Dans ce type de scénario, il est important de pouvoir s’appuyer sur une utilisation cohérente de la bande passante.

Du point de vue de la configuration, l’encodage CBR diffère des autres modes en ce sens qu’avant de commencer à encoder, vous définissez la vitesse de transmission moyenne du contenu de sortie et la fenêtre de mémoire tampon qui s’applique à cette vitesse de transmission. Dans d’autres modes, une de ces valeurs, ou les deux, est inconnue lorsque vous configurez l’encodeur, et est calculée par le codec lors de son codage. CBR est le mode d’encodage standard utilisé par l’encodeur Windows Media DMOs.

## <a name="two-pass-constant-bit-rate-encoding"></a>Encodage à vitesse binaire constante Two-Pass

Le CBR standard utilise une seule passe d’encodage. Vous fournissez votre contenu comme des exemples d’entrée, et le codec compresse le contenu et retourne des exemples de sortie. Il est également possible de traiter deux fois les exemples d’entrée. Lors du premier passage, le codec effectue des calculs pour optimiser l’encodage de votre contenu. Lors de la deuxième passe, le codec utilise les données collectées lors de la première passe pour encoder le contenu.

L’encodage CBR à deux passes présente de nombreux avantages. Elle génère souvent des gains de qualité significatifs par rapport à l’encodage CBR standard sans modifier les exigences de mise en mémoire tampon. Ce mode d’encodage est donc idéal pour le contenu diffusé en continu sur un réseau. La seule situation où le CBR à deux passes n’est pas faisable est lorsque vous encodez du contenu à partir d’une source active et que vous ne pouvez pas utiliser une deuxième passe.

Le type de média de sortie d’un flux CBR à deux passes est identique à celui d’un flux CBR standard. vous pouvez toujours spécifier la vitesse de transmission et la fenêtre de mémoire tampon à utiliser. Lors de la configuration de l’DMO, vous devez le configurer pour qu’il effectue deux passes. Et vous devez notifier la réinitialisation à DMO lorsque vous avez terminé d’envoyer des exemples pour la première passe.

## <a name="quality-based-variable-bit-rate-encoding"></a>Encodage à vitesse de transmission variable Quality-Based

Étant donné que l’encodage CBR ne maintient pas réellement une vitesse binaire constante, la distinction entre les deux et l’encodage à débit binaire variable (VBR) peut sembler un peu floue. La principale différence entre CBR et VBR est la taille de la fenêtre de mémoire tampon utilisée. Les flux encodés VBR ont généralement des fenêtres de tampon volumineuses par rapport aux flux encodés CBR. La fonction VBR basée sur la qualité n’est pas une exception, car vous ne définissez ni la vitesse de transmission ni la fenêtre de mémoire tampon pour celle-ci. Au lieu de cela, vous définissez une valeur de qualité. Le codec tente ensuite de compresser les données afin que la qualité du média encodé soit cohérente tout au long de sa durée, indépendamment des exigences de mémoire tampon du flux résultant.

La fonction VBR basée sur la qualité utilise une seule passe d’encodage et tend à créer des flux compressés volumineux. Lorsque l’encodage est terminé, le codec définit les exigences de la mémoire tampon afin que le décodeur puisse décompresser les données. Le flux VBR encodé n’est pas adapté à la diffusion en continu sur un réseau, de sorte que le VBR basé sur la qualité ne doit être utilisé que pour les scénarios de lecture locale (ou le téléchargement et la lecture).

## <a name="unconstrained-variable-bit-rate-encoding"></a>Encodage de la vitesse de transmission variable sans contrainte

Contrairement au VBR basé sur la qualité, le VBR sans contrainte n’encode pas à un niveau de qualité spécifique. Au lieu de cela, il encode le contenu avec la qualité la plus élevée possible tout en conservant une vitesse de transmission spécifiée. Le VBR sans contrainte utilise deux passes d’encodage et est semblable au CBR à deux passes, à ceci près que vous ne spécifiez pas de paramètre de fenêtre de mémoire tampon pour le flux. Cela signifie qu’il n’existe aucune limite à la taille des échantillons individuels dans le flux, tant que la vitesse de transmission moyenne est inférieure ou égale à la valeur que vous avez définie.

Le VBR sans contrainte est un peu utilisé, car il y a peu de scénarios de lecture qui ont des exigences en ce qui concerne les exigences de la mémoire tampon. Le codec peut définir la fenêtre de mémoire tampon sur la valeur requise après l’encodage, ce qui vous permet de contrôler la taille de la mémoire tampon. Dans la plupart des cas, si vous ne vous inquiétez pas de la taille de la mémoire tampon ou de la cohérence de l’utilisation de la bande passante, vous devez utiliser le VBR basé sur la qualité.

## <a name="peak-constrained-variable-bit-rate-encoding"></a>Encodage à vitesse de transmission variable Peak-Constrained

Le mode d’encodage final est le VBR avec une limite de pointe. À l’instar du VBR sans contrainte, ce mode utilise deux passes d’encodage et des encodages à une vitesse de transmission spécifiée. Toutefois, avec le VBR maximal restreint, vous configurez également la valeur de pic de l’encodage. Les valeurs de pic sont similaires aux valeurs de configuration de mémoire tampon normales : il y a une vitesse de pic et une fenêtre de mémoire tampon de pointe. Le fichier est encodé pour se conformer à une mémoire tampon décrite par les valeurs de pic, avec la condition que la vitesse de transmission moyenne globale du flux soit égale ou inférieure à la valeur de vitesse de transmission moyenne que vous spécifiez.

Le VBR restreint peut être difficile à conceptualiser. Voici le moyen le plus simple de considérer le modèle de mise en mémoire tampon utilisé. Supposons que le flux est un flux CBR avec la vitesse de pic et la fenêtre de mémoire tampon de pointe utilisées pour définir la mémoire tampon. En règle générale, le taux binaire de pointe est assez élevé. L’encodeur garantit que la valeur de la vitesse de transmission moyenne attendue que vous indiquez est conservée pendant la durée du flux. À un point particulier du flux, la vitesse de transmission moyenne est garantie pour être supérieure à la taille totale du flux en bits divisée par la durée du flux, en secondes.

Prenons l’exemple suivant : vous configurez un flux avec une vitesse de transmission moyenne de 16 000 bits par seconde, un taux de bits de pic de 48 000 bits par seconde et une fenêtre de mémoire tampon de pointe de 3 000 (3 secondes). La taille de la mémoire tampon utilisée pour le flux est de 144 000 bits (48 000 bits par seconde x 3 secondes), comme déterminé par les valeurs de pic. L’encodeur compresse les données pour se conformer à cette mémoire tampon. En outre, la vitesse de transmission moyenne du flux doit être inférieure ou égale à 16 000. Si l’encodeur doit faire des exemples très volumineux pour gérer un segment de contenu complexe, il peut tirer parti de la taille de la mémoire tampon volumineuse. Toutefois, d’autres parties du flux doivent être encodées à une vitesse de transmission inférieure pour ramener la moyenne au niveau spécifié.

L’encodage VBR maximal limité est utile pour les périphériques de lecture avec une capacité de mémoire tampon finie et certaines contraintes de débit de données. L’encodage utilisé pour les DVD en est un exemple courant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’encodage VBR](usingvbrencoding.md)
</dt> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



