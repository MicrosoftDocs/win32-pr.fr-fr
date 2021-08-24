---
title: Windows Extensions de périphérique Media Gestionnaire de périphériques pour le transfert de métadonnées
description: Windows Extensions de périphérique Media Gestionnaire de périphériques pour le transfert de métadonnées
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Lecteur Windows Media, extensions de périphérique
- Lecteur Windows Media, extensions
- Lecteur Windows Media, métadonnées
- Lecteur Windows Media, transfert de métadonnées accéléré
- Lecteur Windows Media, transfert accéléré des métadonnées
- métadonnées, extensions de périphérique
- métadonnées, extensions
- extensions d’appareils, transfert de métadonnées
- extensions, transfert de métadonnées
- transfert de métadonnées accéléré
- métadonnées, transfert accéléré
- extensions d’appareils, transfert de métadonnées accéléré
- extensions, transfert de métadonnées accéléré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9b37271fc9714bf3665dccf1475da1a5840c429d7df9136a50fe95789f7a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571633"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>Windows Extensions de périphérique Media Gestionnaire de périphériques pour le transfert de métadonnées

Pour activer le transfert de métadonnées accéléré, les fabricants d’appareils qui ne prennent pas en charge MTP doivent effectuer les opérations suivantes dans le code source :

-   Définir **la \_ \_ \_ prise en charge des appareils WMDM WMP**.
-   incluez wmpdevices. h, qui est installé dans le cadre du kit de développement logiciel (SDK) Lecteur Windows Media.

Wmpdevices. h définit les structures suivantes.



| Structure                                                                                 | Description                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMP \_ WMDM \_ métadonnées aller- \_ \_ retour \_ PC2DEVICE](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Structure utilisée par Lecteur Windows Media pour demander des informations de synchronisation des métadonnées accélérées à partir d’appareils portables qui ne prennent pas en charge MTP. |
| [WMP \_ WMDM \_ métadonnées aller- \_ \_ retour \_ DEVICE2PC](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Structure utilisée par Lecteur Windows Media pour recevoir des informations de synchronisation des métadonnées accélérées à partir d’appareils portables qui ne prennent pas en charge MTP. |



 

pour demander des informations à partir de l’appareil sur les métadonnées qui ont changé, Lecteur Windows Media 10 ou ultérieur appelle la méthode Windows Media Gestionnaire de périphériques **IWMDMDevice3 ::D eviceiocontrol**. Lorsque vous effectuez cet appel, le lecteur suit des étapes spécifiques, comme suit :

-   Le premier paramètre, *dwIoControlCode*, contient l’aller **- \_ \_ \_ \_ retour de métadonnées IOCTL WMP** constant. Cette constante est définie dans wmpdevices. h.
-   Le deuxième paramètre, *lpInBuffer*, pointe vers une structure de **\_ WMDM de \_ métadonnées d’aller- \_ \_ retour \_ WMP** .
-   Le troisième paramètre, *nInBufferSize*, contient la taille de la mémoire tampon d’entrée.
-   Le quatrième paramètre, *lpOutBuffer*, pointe vers une structure de boucles de **\_ WMDM de \_ métadonnées \_ \_ \_ WMP** . L’appareil doit remplir cette structure avec des informations sur les modifications.
-   Le cinquième paramètre, *pnOutBufferSize*, reçoit la taille de la mémoire tampon de sortie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extensions d’appareil pour le transfert de métadonnées accéléré**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




