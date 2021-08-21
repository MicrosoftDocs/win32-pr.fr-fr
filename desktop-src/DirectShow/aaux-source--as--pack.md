---
description: Pack source AAUX (AS)
ms.assetid: 0e173fe5-0b9d-48e8-bcbd-403614d51558
title: Pack source AAUX (AS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a2d8aa11c9560b2aa59165afd9bdaae775be7755a7a7d2a5e87a80df412d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160260"
---
# <a name="aaux-source-as-pack"></a>Pack source AAUX (AS)

Les tableaux suivants répertorient les valeurs utilisées par le pilote MSDV pour remplir les membres **dwDVAAuxSrc** et **dwDVAAuxSrc1** de la structure [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . pour plus d’informations, consultez [DVINFO Field Paramètres dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

magnétoscope numérique Paramètres



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

LF (1)

1

1

1

1

Réservé (1)

1

1

1

1

TAILLE AF (6)

00:1111

01:0000

00:1111

01:0000

SM (1)

0

0

0

0

CHN (2)

01

01

01

01

PA (1)

1

1

1

1

MODE AUDIO (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0000

0000

1111

1111

Réservé (1)

1

1

1

1

ML (1)

1

1

1

1

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

EF (1)

1

1

1

1

TC (1)

1

1

1

1

SMP (3)

010

010

010

010

QU (3)

001

001

001

001

Pack AS

    Audio Block 1\*

0xD1C130CF

0xD1E130D0

0xD1C030CF

0xD1E030D0

    Audio Block 2\*

0x00000000

0x00000000

0xD1C03FCF

0xD1E03FD0



 

magnétoscope numérique 25 et DVCPRO 50 Paramètres (planifié)



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

LF (1)

0

0

0

0

Réservé (1)

1

1

1

1

TAILLE AF (6)

01:0110

01:1000

01:0110

01:1000

Réservé (1)

0

0

0

0

CHN (2)

00

00

00

00

Réservé (1)

1

1

1

1

MODE AUDIO (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0,001

0,001

0,001

0,001

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

0:0010

0:0010

Réservé (2)

11

11

11

11

SMP (3)

000

000

000

000

QU (3)

000

000

000

000

Pack AS

    Audio Block 1\*

0xC0C01056

0xC0E01058

0xC0C21056

0xC0E21058

    Audio Block 2\*

0xC0C01156

0xC0E01158

0xC0C21156

0xC0E21158



 

> [!Note]  
> \* La structure [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) contient deux AAUX As packs, pour les blocs audio 1 et 2. DV50 possède quatre blocs audio. les blocs 3 et 4 ne sont pas représentés dans la structure **DVINFO** .

 

magnétoscope 100 Paramètres (planifié)



Standard DV

DVCPRO 100 — planifié

FOURCC

dvh1

Système

1080-60i

720-60p

1080-50i

LF (1)

0

0

0

Réservé (1)

1

1

1

TAILLE AF (6)

01:0110

01:0110

01:1000

Réservé (1)

0

0

0

CHN (2)

00

00

00

Réservé (1)

1

1

1

MODE AUDIO (4)

    Audio Block 1\*

0000

0000

0000

    Audio Block 2\*

0,001

0,001

0,001

Réservé (2)

11

11

11

50/60 (1)

0

0

1

SSPÉCIFICATION (5)

0:0011

0:0011

0:0011

Réservé (2)

11

11

11

SMP (3)

000

000

000

QU (3)

000

000

000

Pack AS

    Audio Block 1\*

0xC0C31056

0xC0C31056

0xC0D31058

    Audio Block 2\*

0xC0C31156

0xC0C31156

0xC0D31158



 

> [!Note]  
> \* DVCPRO 100 a 8 blocs audio. les blocs 3 à 8 ne sont pas représentés dans la structure [DVINFO](dvinfo-field-settings-in-the-msdv-driver.md) .

 

## <a name="remarks"></a>Remarques

Les codes de champ suivants présentent un intérêt :

-   LF : indicateur de mode verrouillé. Indique si l’audio est verrouillé.
    -   0 = verrouillé
    -   1 = déverrouillé
-   AF SIZE : taille de trame audio. Spécifie le nombre d’échantillons audio par image.

    Définition IEC 61834 :

    -   00:1111 = 1068 échantillons par image
    -   01:0000 = 1280 échantillons par image

    Définition de 314M SMPTE :

    -   01:0110 = 1602 échantillons par image
    -   01:1000 = 1920 échantillons par image

    Selon la fréquence d’images, le nombre exact d’échantillons dans une trame peut varier. Par exemple, le format NTSC est de 30000/1001 images par seconde (29,97 fps). Avec un son 32-kHz, il y a environ 1067,73 audio samples per Frame. Le taux nominal est donc de 1068, mais le nombre réel varie selon le cadre. En outre, avec l’audio déverrouillé, le nombre d’échantillons audio par trame est autorisé à varier au fil du temps d’une certaine plage.

<!-- -->

-   SM : mode stéréo.
    -   0 = stéréo
    -   1 = mono
-   CHN : nombre de canaux audio par bloc audio.
    -   0 = un canal par bloc audio
    -   1 = deux canaux par bloc audio
-   MODE AUDIO : indique le contenu du signal audio sur chaque canal. L’interprétation de ce champ dépend des valeurs qui sont placées dans les champs SM et CHN. Les définitions fournies ci-dessous correspondent aux valeurs utilisées par MSDV. Pour plus d’informations, reportez-vous aux spécifications.

    Définition IEC 61834 :

    -   0000 = ch a/c/e/g est le canal gauche, ch b/d/f/h est le canal droit
    -   1111 = aucune donnée audio

    Définition de 314M SMPTE :

    -   0000 = CH1 (CH3)
    -   0001 = CH2 (CH4)

-   50/60 : nombre de champs.
    -   0 = 60 champs
    -   1 = 50 champs
-   SSPÉCIFICATION : type de système.

    Définition IEC 61834 :

    -   00000 = 525-60 ou 625-50, DVSD
    -   00001 = 525-60 ou 625-50, dvsl (voir IEC 61883-5)

    Définition SMPTE 314M/SPMTE 370 :

    -   00000 = 2 blocs audio par image vidéo
    -   00010 = 4 blocs audio par image vidéo
    -   00011 = 8 blocs audio par image vidéo

-   SMP : fréquence d’échantillonnage.
    -   000 = 48 kHz
    -   010 = 32 kHz
-   QU : quantification.
    -   0 = 16 bits linéaires
    -   1 = 12 bits non linéaires

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Paramètres du champ DVINFO dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



