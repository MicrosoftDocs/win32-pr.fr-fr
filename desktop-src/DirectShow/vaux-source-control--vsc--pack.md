---
description: Pack de contrôle de code source VAUX (VSC)
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: Pack de contrôle de code source VAUX (VSC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed51363a15c0024dcaf3edca5d21217cb29396d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866445"
---
# <a name="vaux-source-control-vsc-pack"></a>Pack de contrôle de code source VAUX (VSC)

Les tableaux suivants répertorient les valeurs utilisées par le pilote MSDV pour remplir le membre **dwDVVAuxCtl** de la structure [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Pour plus d’informations, consultez [paramètres de champ DVINFO dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

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



 

**Paramètres DVCPRO 100 (planifié)**



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



 

## <a name="remarks"></a>Notes

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

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Paramètres de champ DVINFO dans le pilote MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



