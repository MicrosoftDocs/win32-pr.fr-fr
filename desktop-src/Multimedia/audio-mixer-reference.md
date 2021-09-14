---
title: référence de Mixer Audio
description: référence de Mixer Audio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- audio multimédia, mixages audio
- audio, mixages audio
- audio multimédia, référence du mélangeur
- audio, référence du mélangeur
- mixages audio, référence
- mixageions, référence
- référence pour les mixages audio, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007261"
---
# <a name="audio-mixer-reference"></a>référence de Mixer Audio

Cette section décrit les fonctions, les structures et les messages associés aux mixages audio. Ces éléments sont regroupés comme suit.

## <a name="querying-devices"></a>Interrogation des appareils

-   [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>Ouverture et fermeture

-   [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>récupération des identificateurs de Mixer

-   [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>Récupération de contrôles Line

-   [**MIXERCONTROL**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>Modification des attributs de contrôle

-   [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**MIXERCONTROLDETAILS \_ booléen**](/previous-versions//dd757295(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ signé**](/previous-versions//dd757297(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ non signé**](/previous-versions//dd757298(v=vs.85))
-   [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>Récupération des informations de ligne

-   [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**\_modification du \_ contrôle \_ MIXM mm**](mm-mixm-control-change.md)
-   [**MM \_ \_ modification de ligne MIXM \_**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>Envoi de messages de User-Defined

-   [**mixerMessage**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[référence de Mixer Audio](audio-mixer-reference.md)
</dt> </dl>

 

 