---
title: Codes de contrôle d’e/s de périphérique
description: Codes de contrôle d’e/s de périphérique
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player, codes de contrôle d’e/s de périphérique
- Windows Media Player, codes de contrôle
- Gestionnaire de périphériques Windows Media
- codes de contrôle d’e/s de périphérique
- codes de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517966"
---
# <a name="device-io-control-codes"></a>Codes de contrôle d’e/s de périphérique

Le lecteur Windows Media 10 ou version ultérieure définit les codes de contrôle d’e/s des appareils Windows Media Gestionnaire de périphériques. Le tableau suivant contient les codes de contrôle et leurs descriptions.



| Code de contrôle d’e/s                      | Valeur      | Description                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **aller \_ - \_ retour des métadonnées IOCTL WMP \_ \_** | 0x31504d57 | Gère le transfert des informations relatives aux modifications apportées aux valeurs de métadonnées. Consultez [extensions de périphérique pour le transfert de métadonnées accéléré](device-extensions-for-accelerated-metadata-transfer.md).                                                                                                                                                                          |
| **synchronisation de l' \_ appareil WMP avec IOCTL \_ \_ \_**     | 0x32504d57 | Indique si un périphérique portable prend en charge la synchronisation automatique. Le lecteur Windows Media 10 ou version ultérieure ne fournit aucune mémoire tampon d’entrée. La mémoire tampon de sortie doit retourner une valeur **DWORD** . La valeur 1 signifie que l’appareil prend en charge la synchronisation. La valeur 0 signifie que l’appareil ne prend pas en charge la synchronisation automatique.<br/> Pour plus d'informations, consultez la section Notes.<br/> |



 

## <a name="remarks"></a>Notes

Ces codes de contrôle sont définis dans wmpdevices. h.

Si l’appareil ne prend pas en charge la synchronisation des **appareils par IOCTL \_ WMP \_ \_ \_**, le lecteur Windows Media 10 ou version ultérieure suppose que l’appareil prend en charge la synchronisation automatique. Notez que même si cette valeur peut interdire la synchronisation automatique, des critères supplémentaires sont utilisés pour déterminer si l’appareil prend en charge la synchronisation automatique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extensions d’appareil pour le transfert de métadonnées accéléré**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Lecteur Windows Media**](windows-media-player.md)
</dt> </dl>

 

 





