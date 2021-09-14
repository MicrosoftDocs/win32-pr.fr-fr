---
description: Pack de contrôle de code source AAUX (ASC)
ms.assetid: 3df80895-81e1-42a4-a095-913e77b199e5
title: Pack de contrôle de code source AAUX (ASC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab942ccff1cf38e6962d508c9c9bfc99ea9fed6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112442"
---
# <a name="aaux-source-control-asc-pack"></a>Pack de contrôle de code source AAUX (ASC)

Les tableaux suivants répertorient les valeurs utilisées par le pilote MSDV pour remplir le **dwDVAAuxCtl** et

**dwDVAAuxCtl1** membres de la structure [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . pour plus d’informations, consultez [DVINFO Field Paramètres dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

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

CGMS (2)

00

00

00

00

ISR (2)

11

11

11

11

CMP (2)

11

11

11

11

SS (2)

11

11

11

11

REC ST (1)

1

1

1

1

FIN DE L’ENREGISTREMENT (1)

1

1

1

1

MODE REC (3)

001

001

001

001

INSÉRER CH (3)

111

111

111

111

DRF (1)

1

1

1

1

VITESSE (7)

010:0000

010:0000

010:0000

010:0000

Réservé (1)

1

1

1

1

GENRE (7)

111:1111

111:1111

111:1111

111:1111

ASC Pack (blocs audio)\*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

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

CGMS (2)

00

00

00

00

Réservé (4)

1111

1111

1111

1111

EFC (2)

00

00

00

00

REC ST (1)

1

1

1

1

FIN DE L’ENREGISTREMENT (1)

1

1

1

1

FONDU GS (1)

1

1

1

1

FIN DE FONDU (1)

1

1

1

1

Réservé (4)

1111

1111

1111

1111

DRF (1)

1

1

1

1

VITESSE (7)

111:1000

110:0100

111:1000

110:0100

Réservé (8)

1111:1111

1111:1111

1111:1111

1111:1111

ASC Pack (blocs audio)\*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

\* La structure *DVINFO* contient deux AAUX As packs, pour les blocs audio 1 et 2. DV50 possède quatre blocs audio. les blocs 3 et 4 ne sont pas représentés dans la structure *DVINFO* .

magnétoscope 100 Paramètres (planifié)



Standard DV

DVCPRO 100 — planifié

FOURCC

dvh1

Système

1080-60i

720-60p

1080-50i

CGMS (2)

00

00

00

Réservé (4)

1111

1111

1111

EFC (2)

00

00

00

REC ST (1)

1

1

1

FIN DE L’ENREGISTREMENT (1)

1

1

1

FONDU GS (1)

1

1

1

FIN DE FONDU (1)

1

1

1

Réservé (4)

1111

1111

1111

DRF (1)

1

1

1

VITESSE (7)

111:1000

111:1000

110:0100

Réservé (8)

1111:1111

1111:1111

1111:1111

ASC Pack (blocs audio)\*

0xFFF8FF3C

0xFFF8FF3C

0xFFE4FF3C



 

\* DVCPRO 100 a 8 blocs audio. les blocs 3 à 8 ne sont pas représentés dans la structure *DVINFO* .

## <a name="remarks"></a>Notes

Les codes de champ suivants présentent un intérêt :

-   **CGMS**: copie du système de gestion de la génération. 0 = copie autorisée sans restriction.

    Les véritables packs ASC du flux DV peuvent contenir des valeurs différentes.

<!-- -->

-   **Mode REC**: mode d’enregistrement. 1 = original
-   **Vitesse**: vitesse de lecture des magnétoscopes.

    Définition IEC 61834 :

    -   010:0000 = vitesse normale, 525-60 ou 625-50

    Définition de 314M SMPTE :

    -   111:1000 = vitesse normale, 525-60
    -   110:0100 = vitesse normale, 625-50

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Paramètres du champ DVINFO dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



