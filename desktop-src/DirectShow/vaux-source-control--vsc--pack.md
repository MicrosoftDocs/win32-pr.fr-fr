---
description: Pack de contrôle de code source VAUX (VSC)
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: Pack de contrôle de code source VAUX (VSC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcdc91d5c4b2cea460c85b696c59bfce7799d39aed0a6bfcbc03f3d3c522a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072073"
---
# <a name="vaux-source-control-vsc-pack"></a>Pack de contrôle de code source VAUX (VSC)

Les tableaux suivants répertorient les valeurs utilisées par le pilote MSDV pour remplir le membre **dwDVVAuxCtl** de la structure [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . pour plus d’informations, consultez [DVINFO Field Paramètres dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

**magnétoscope numérique Paramètres**



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

Réservé (1)

1

1

1

1

MODE REC (2)

00

00

00

00

Réservé (1)

1

1

1

1

DISP (3)

000

000

000

000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

ST (1)

1

1

1

1

SC (1)

1

1

1

1

BCSYS (2)

00

01

00

01

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

Pack VSC

0xFFFCC83F

0xFFFDC83F

0xFFFCC83F

0xFFFDC83F



 

**dvcpro 25 et dvcpro 50 Paramètres (planifié)**



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

Réservé (6)

11:1111

11:1111

11:1111

11:1111

Réservé (2)

11

11

11

11

Réservé (2)

00

00

00

00

Réservé (1)

1

1

1

1

DISP (3)

000

000

000

000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

Réservé (2)

11

11

11

11

Réservé (2)

00

00

00

00

Réservé (8)

1111:1111

1111:1111

1111:1111

1111:1111

Pack VSC

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F



 

**DVCPRO 100 Paramètres (planifié)**



Standard DV

DVCPRO 100 — planifié

FOURCC

dvh1

Système

1080-60i

720p-60p

1080-50i

CGMS (2)

00

00

00

Réservé (6)

11:1111

11:1111

11:1111

Réservé (2)

11

11

11

Réservé (2)

00

00

00

Réservé (1)

1

1

1

DISP (3)

010

010

010

FF (1)

1

1

1

FS (1)

1

1

1

FC (1)

1

1

1

IL (1)

1

1

1

Réservé (2)

11

11

11

Réservé (2)

00

00

00

Réservé (8)

1111:1111

1111:1111

1111:1111

Pack VSC

0xFFFCCA3F

0xFFFCCA3F

0xFFFCCA3F



 

## <a name="remarks"></a>Remarques

Les codes de champ suivants présentent un intérêt :

-   **CGMS**: copie du système de gestion de la génération. 0 = copie autorisée sans restriction.

    Les packages VSC réels dans le flux DV peuvent contenir des valeurs différentes.

<!-- -->

-   **Mode REC**: mode d’enregistrement. 1 = original.
-   **DISP**: affiche le mode de sélection. 000 = proportions 4:3, formatage complet ; 010 = proportions 16:9.
-   **BCSYS**: système de diffusion. Ce champ définit le type d’informations de signalement à l’écran étendu.
    -   0 = type 0 (voir IEC 61880)
    -   1 = type 1 (voir ETSI en 300 294)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Paramètres du champ DVINFO dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



