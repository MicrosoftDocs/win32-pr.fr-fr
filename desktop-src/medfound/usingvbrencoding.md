---
description: Cette section décrit comment configurer les flux VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Utilisation de l’encodage VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313621"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>Utilisation de l’encodage VBR (Microsoft Media Foundation)

Comme indiqué dans la rubrique [méthodes d’encodage](encodingmethods.md) , l’encodage VBR (variable bit rate) est utilisé pour améliorer la cohérence de la qualité du contenu. Vous configurez les flux VBR de la même façon que vous encodez des flux à débit binaire constant (CBR), à l’exception des paramètres de mémoire tampon (vitesse de transmission et mémoire tampon). Cette section décrit comment configurer les flux VBR.

## <a name="configuring-quality-based-vbr"></a>Configuration du VBR basé sur la qualité

L’encodage à l’aide de la méthode VBR basée sur la qualité ne requiert pas de paramètres de mémoire tampon prédéfinis. Au lieu de cela, vous spécifiez un niveau de qualité (compris entre 0 et 100) que l’encodeur utilise pour déterminer dynamiquement les paramètres de mémoire tampon appropriés. Ce mode d’encodage n’utilise qu’un seul passe d’encodage.

Vous pouvez énumérer les types de sortie VBR basés sur la qualité pris en charge pour les codecs audio. vous devez utiliser l’un des types retournés par la DMO lors de la définition du type de sortie. Pour plus d’informations, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).

Pour configurer un flux vidéo VBR basé sur la qualité, vous devez définir les propriétés qui sont répertoriées dans le tableau suivant.



| Propriété                                            | Description                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | A la valeur VARIANT \_ true.                                                                                                                                   |
| [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md) | Définissez sur la valeur de qualité souhaitée, de 0 à 100. Toutes les valeurs de qualité ne représentent pas des paramètres discrets. Pour plus d’informations, consultez la description de la propriété. |



 

## <a name="configuring-unconstrained-vbr"></a>Configuration de la VBR sans contrainte

L’encodage VBR non restreint permet à l’encodeur de modifier la taille des échantillons individuels sans aucune limite de mémoire tampon explicite. Toutefois, la vitesse de transmission moyenne sur la durée du contenu résultant doit être inférieure ou égale à la valeur spécifiée. Le VBR sans contrainte requiert deux passes d’encodage.

Vous pouvez énumérer les types de sortie VBR en deux passes pris en charge pour les codecs audio. vous devez utiliser l’un des types retournés par la DMO lors de la définition du type de sortie. Pour plus d’informations, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).

Pour configurer un flux vidéo VBR non restreint, vous devez définir les propriétés répertoriées dans le tableau suivant.



| Propriété                                            | Description                          |
|-----------------------------------------------------|--------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | A la valeur VARIANT \_ true.                |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Défini sur 2.                            |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | Définissez sur la vitesse de transmission moyenne souhaitée. |



 

## <a name="configuring-peak-constrained-vbr"></a>Configuration de Peak-Constrained VBR

Le VBR limité au maximum est comme un VBR non restreint en ce qu’il est limité à un débit binaire moyen sur la durée du flux. En outre, le VBR maximal restreint est conforme à une mémoire tampon de pointe. Cette mémoire tampon est décrite à l’aide d’un taux binaire de pointe et d’une fenêtre de mémoire tampon de pointe, tout comme une mémoire tampon CBR est décrite par une vitesse de transmission moyenne et une fenêtre de mémoire tampon. Ce mode offre à la flexibilité de l’encodeur la manière dont il encode des exemples individuels tout en adhérant aux limitations de pointe. Cela s’avère particulièrement utile lorsque le décodage est effectué par une puce dans un appareil, comme un lecteur de DVD, où des limitations matérielles doivent être prises en compte.

Les types de sortie de l’encodeur audio VBR les plus pertenus pris en charge sont les mêmes que ceux énumérés pour le VBR sans contrainte. définissez les valeurs de pic sur la DMO et utilisez le type remis. Pour plus d’informations, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).

Pour configurer un flux vidéo VBR avec des pics de charge, vous devez définir les propriétés répertoriées dans le tableau suivant à l’aide de la méthode **IPropertyBag :: Write** .



| Propriété                                            | Description                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | A la valeur VARIANT \_ true.                                           |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Défini sur 2.                                                       |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | Définissez sur la vitesse de transmission moyenne souhaitée.                            |
| [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md)             | Définissez sur le taux binaire de pointe souhaité.                               |
| [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)             | Définissez sur la fenêtre de mémoire tampon qui correspond au taux de bits de pointe. |



 

> [!Note]  
> Il est recommandé de définir le taux de bits de pointe sur au moins deux fois la vitesse de transmission moyenne. Si vous affectez une valeur inférieure au taux de pic, le codec peut encoder le contenu en deux passes CBR au lieu du VBR maximal.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> <dt>

[Utilisation de l’encodage Two-Pass](usingtwoencodingpasses.md)
</dt> <dt>

[Utilisation de l’audio](workingwithaudio.md)
</dt> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 



