---
title: Codes de contrôle d’e/s de périphérique
description: Codes de contrôle d’e/s de périphérique
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Lecteur Windows Media, codes de contrôle d’e/s de périphérique
- Lecteur Windows Media, codes de contrôle
- Windows Gestionnaire de périphériques de média
- codes de contrôle d’e/s de périphérique
- codes de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d610b396125cf190764b53106ca6535a214e2c8166f4e69de884c113fd77ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935848"
---
# <a name="device-io-control-codes"></a>Codes de contrôle d’e/s de périphérique

Lecteur Windows Media 10 ou une version ultérieure définit des codes de contrôle d’e/s de périphérique Windows Media Gestionnaire de périphériques. Le tableau suivant contient les codes de contrôle et leurs descriptions.



| Code de contrôle d’e/s                      | Valeur      | Description                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **aller \_ - \_ retour des métadonnées IOCTL WMP \_ \_** | 0x31504d57 | Gère le transfert des informations relatives aux modifications apportées aux valeurs de métadonnées. Consultez [extensions de périphérique pour le transfert de métadonnées accéléré](device-extensions-for-accelerated-metadata-transfer.md).                                                                                                                                                                          |
| **synchronisation de l' \_ appareil WMP avec IOCTL \_ \_ \_**     | 0x32504d57 | Indique si un périphérique portable prend en charge la synchronisation automatique. Lecteur Windows Media 10 ou version ultérieure ne fournit aucune mémoire tampon d’entrée. La mémoire tampon de sortie doit retourner une valeur **DWORD** . La valeur 1 signifie que l’appareil prend en charge la synchronisation. La valeur 0 signifie que l’appareil ne prend pas en charge la synchronisation automatique.<br/> Pour plus d'informations, consultez la section Notes.<br/> |



 

## <a name="remarks"></a>Remarques

Ces codes de contrôle sont définis dans wmpdevices. h.

si l’appareil ne prend pas en charge la synchronisation des **appareils par IOCTL \_ WMP \_ \_ \_**, Lecteur Windows Media 10 ou ultérieur suppose que l’appareil prend en charge la synchronisation automatique. Notez que même si cette valeur peut interdire la synchronisation automatique, des critères supplémentaires sont utilisés pour déterminer si l’appareil prend en charge la synchronisation automatique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extensions d’appareil pour le transfert de métadonnées accéléré**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Lecteur Windows Media**](windows-media-player.md)
</dt> </dl>

 

 





