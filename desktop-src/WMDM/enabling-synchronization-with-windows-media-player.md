---
title: Activation de la synchronisation avec le lecteur Windows Media
description: Activation de la synchronisation avec le lecteur Windows Media
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Gestionnaire de périphériques Windows Media, synchronisation avec le lecteur Windows Media
- Gestionnaire de périphériques, synchronisation avec le lecteur Windows Media
- Guide de programmation, synchronisation avec le lecteur Windows Media
- fournisseurs de services, synchronisation avec le lecteur Windows Media
- création de fournisseurs de services, synchronisation avec le lecteur Windows Media
- synchronisation avec le lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509005"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>Activation de la synchronisation avec le lecteur Windows Media

Vous pouvez autoriser un appareil à participer à la synchronisation automatique avec le lecteur Windows Media. La synchronisation automatique signifie que lorsqu’un appareil synchronisé défini par l’utilisateur se connecte à l’ordinateur, le lecteur Windows Media télécharge, met à jour ou supprime automatiquement les fichiers de l’appareil sans nécessiter d’entrée d’utilisateur supplémentaire.

Par défaut, les appareils suivants sont synchronisés avec le lecteur Windows Media :

-   Appareils MTP
-   Périphériques de stockage de masse
-   Appareils Windows CE (Windows Media Player 10 mobile et versions ultérieures)

Pour qu’un autre appareil se synchronise avec le lecteur Windows Media, les conditions suivantes doivent être remplies :

-   L’appareil doit publier une interface d’appareil PAP qui est {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}
-   Les objets d’appareil retournés par le fournisseur de services doivent prendre en charge l’interface **IMDSPDevice3** .
-   Le paramètre d’appareil UseExtendedWmdm doit être défini sur une valeur **DWORD** égale à 1. Pour plus d’informations, consultez Paramètres de l' [appareil](device-parameters.md) .
-   Le fournisseur de services doit implémenter les interfaces suivantes :

    [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un fournisseur de services**](creating-a-service-provider.md)
</dt> <dt>

[**Paramètres de l’appareil**](device-parameters.md)
</dt> </dl>

 

 




