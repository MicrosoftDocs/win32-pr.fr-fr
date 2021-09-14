---
title: Encodage à débit binaire constant (CBR)
description: Encodage à débit binaire constant (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media Format SDK, encodage CBR
- Windows Media Format SDK, débit binaire constant (CBR)
- codecs, encodage CBR
- codecs, débit binaire constant (CBR)
- débit binaire constant (CBR)
- CBR (vitesse binaire constante)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219556"
---
# <a name="constant-bit-rate-cbr-encoding"></a>Encodage à débit binaire constant (CBR)

l’encodage à débit binaire Constant (CBR) est la méthode par défaut d’encodage avec le kit de développement logiciel (SDK) de Format multimédia Windows. Lorsque vous utilisez l’encodage CBR, vous spécifiez la vitesse de transmission cible d’un flux et le codec utilise la quantité de compression nécessaire pour l’obtenir.

Avec l’encodage CBR, la vitesse de transmission et la taille du flux encodé sont connues avant l’encodage. Par exemple, si vous encodez une chanson de trois minutes à 32 000 bits par seconde, vous savez que la taille du fichier est d’environ 704 kilo-octets (32 000 BPS x 180 secondes/8 bits par octet/1 024). Vous savez également que la bande passante requise pour diffuser le contenu encodé est environ 32 000 bits par seconde.

L’encodage à vitesse de transmission variable avec restriction (décrite dans la section suivante) vous permet également de connaître la vitesse de transmission avant l’encodage, mais étant donné que le taux est variable, le fichier résultant ne peut pas être diffusé en continu aussi efficacement qu’un fichier encodé en mode CBR. Avec CBR, le taux de bits dans le temps reste toujours proche de la vitesse de transmission moyenne ou cible, et la quantité de variation peut être spécifiée.

L’inconvénient de l’encodage CBR est que la qualité du contenu encodé n’est pas constante. Étant donné que le contenu est plus difficile à compresser, les parties d’un flux CBR auront une qualité inférieure à celle des autres. Par exemple, un film classique présente des scènes relativement statiques et des scènes qui sont pleines d’actions. Si vous encodez un film à l’aide de CBR, les scènes qui sont statiques et, par conséquent, faciles à coder efficacement, présentent une qualité supérieure à celle des scènes d’action, qui sont bien plus difficiles à coder efficacement.

L’encodage CBR peut également aboutir à une qualité incohérente d’un fichier à un autre. Si vous utilisez CBR pour encoder plusieurs chansons de différents genres à la même vitesse de transmission, vous pouvez remarquer une différence de qualité entre eux.

En général, les variations de la qualité d’un fichier CBR sont plus prononcées à des vitesses de transmission inférieures. À des vitesses de transmission supérieures, la qualité d’un fichier encodé CBR continuera à varier, mais les problèmes de qualité seront moins perceptibles pour l’utilisateur. Lorsque vous utilisez l’encodage CBR, vous devez définir la bande passante aussi élevée que possible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Choix d’une méthode d’encodage**](choosing-an-encoding-method.md)
</dt> <dt>

[**Fonctionnalités du codec**](codec-features.md)
</dt> <dt>

[**Encodage à vitesse de transmission variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




