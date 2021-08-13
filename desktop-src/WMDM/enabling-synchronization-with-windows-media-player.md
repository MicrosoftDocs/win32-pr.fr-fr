---
title: activation de la synchronisation avec Lecteur Windows Media
description: activation de la synchronisation avec Lecteur Windows Media
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Gestionnaire de périphériques de média, synchronisation avec Lecteur Windows Media
- Gestionnaire de périphériques, synchronisation avec Lecteur Windows Media
- guide de programmation, synchronisation avec Lecteur Windows Media
- fournisseurs de services, synchronisation avec Lecteur Windows Media
- création de fournisseurs de services, synchronisation avec Lecteur Windows Media
- synchronisation avec Lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef06dd0e32e0ea95674f54b94336ecb6882e8215775c857ee0780a58b71af75c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585007"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>activation de la synchronisation avec Lecteur Windows Media

vous pouvez autoriser un appareil à participer à la synchronisation automatique avec Lecteur Windows Media. la synchronisation automatique signifie que lorsqu’un appareil synchronisé défini par l’utilisateur se connecte à l’ordinateur, Lecteur Windows Media télécharge, met à jour ou supprime automatiquement des fichiers de l’appareil sans intervention supplémentaire de l’utilisateur.

par défaut, les appareils suivants sont synchronisés avec Lecteur Windows Media :

-   Appareils MTP
-   Périphériques de stockage de masse
-   appareils Windows CE (Lecteur Windows Media 10 Mobile et versions ultérieures)

pour qu’un autre appareil se synchronise avec Lecteur Windows Media, les conditions suivantes doivent être remplies :

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

 

 




