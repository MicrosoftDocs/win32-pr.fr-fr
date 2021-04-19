---
description: Pack source VAUX (VS)
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: Pack source VAUX (VS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f7ad2a91f1be1291b564013041e6dfa23bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523287"
---
# <a name="vaux-source-vs-pack"></a>Pack source VAUX (VS)

Les tableaux suivants répertorient les valeurs utilisées par le pilote MSDV pour remplir le membre **dwDVVAuxSrc** de la structure [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Pour plus d’informations, consultez [paramètres de champ DVINFO dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

**Paramètres de magnétoscope numérique**



Standard DV

MAGNÉTOSCOPE NUMÉRIQUE (IEC 61834)

FOURCC

dvsl

dvsd

Système

525-60

625-50

525-60

625-50

CANAL TV (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

CANAL TV (4)

1111

1111

1111

1111

CODE SOURCE (2)

11

11

11

11

50/60 (1)

0

1

0

1

SSPÉCIFICATION (5)

0:0001

0:0001

0:0000

0:0000

CATÉGORIE DE TUNER (8)

1111:1111

1111:1111

1111:1111

1111:1111

Pack VS

0xFFC1FFFF

0xFFE1FFFF

0xFFC0FFFF

0xFFE0FFFF



 

**Paramètres DVCPRO 25 et DVCPRO 50 (planifié)**



Standard DV

DVCPRO (SMPTE 314M) — planifié

FOURCC

dv25

dv50

Système

525-60

625-50

525-60

625-50

Réservé (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

Réservé (4)

1111

1111

1111

1111

Réservé (2)

11

11

11

11

50/60 (1)

0

1

0

1

SSPÉCIFICATION (5)

0:0000

0:0000

0:0100

0:0100

VISC (8)

1111:1111

1111:1111

1111:1111

1111:1111

Pack VS

0x7FC0FFFF

0x7FE0FFFF

0x7FC4FFFF

0x7FE4FFFF



 

**Paramètres magnétoscope 100 (planifié)**



Standard DV

DVCPRO 100 — planifié

FOURCC

dvh1

Système

1080-60i

720-60p

1080-50i

Réservé (8)

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

EN (1)

1

1

1

CLF (2)

11

11

11

Réservé (4)

1111

1111

1111

Réservé (2)

11

11

11

50/60 (1)

0

0

1

SSPÉCIFICATION (5)

1:0100

1:1000

1:0100

VISC (8)

1111:1111

1111:1111

1111:1111

Pack VS

0x7FD4FFFF

0x7FD8FFFF

0x7FF4FFFF



 

## <a name="remarks"></a>Notes

Les codes de champ suivants présentent un intérêt :

-   **B/W**: indicateur noir et blanc. 1 = couleur.
-   **50/60**: nombre de champs.
    -   0 = 60 champs
    -   1 = 50 champs
-   **SSpécification**: type de signal.

    Définition IEC 61834 :

    -   0:0000 = 525-60 ou 625-50, DVSD
    -   0:0001 = 525-60 ou 625-50, dvsl (comme défini dans IEC 61883-5)

    Définition de 314M SMPTE :

    -   0:0000 = compression 4:1:1
    -   0:0100 = compression 4:2:2

    Définition SMPTE 370 :

    -   1:0100 = 1080/60i (60 Hz) ou 1080/50i (50 Hz)
    -   1:1000 = 720/60p

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Paramètres de champ DVINFO dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



