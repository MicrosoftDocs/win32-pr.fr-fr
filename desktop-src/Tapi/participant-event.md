---
description: L' \_ énumération d’événement participant décrit les événements participants.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: Énumération PARTICIPANT_EVENT (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523589"
---
# <a name="participant_event-enumeration"></a>\_Énumération des événements participants

\[ Cette énumération n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’énumération d' **\_ événement participant** décrit les événements participants. La méthode d' [**\_ événement ITParticipantEvent :: obtenir**](itparticipantevent-get-event.md) retourne un membre de cette énumération pour indiquer le type d’événement participant à la Conférence qui s’est produit. Cette énumération est utilisée par les applications qui accèdent au [MSP ipconf](ipconf-msp.md).

## <a name="syntax"></a>Syntaxe


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_nouveau \_ participant PE**
</dt> <dd>

Un nouveau participant a été ajouté à la Conférence.

</dd> <dt>

<span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_modification des informations PE \_**
</dt> <dd>

Les informations sur un participant ont été modifiées.

</dd> <dt>

<span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_absence de participant PE \_**
</dt> <dd>

Un participant a quitté la Conférence.

</dd> <dt>

<span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**nouveau sous- \_ \_ flux PE**
</dt> <dd>

Un nouveau sous-flux a été ajouté au participant.

</dd> <dt>

<span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**sous- \_ flux PE \_ supprimé**
</dt> <dd>

Un nouveau sous-flux a été supprimé du participant.

</dd> <dt>

<span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**sous- \_ flux PE \_ mappé**
</dt> <dd>

Un participant a été mappé à un sous-flux.

</dd> <dt>

<span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**sous-flux PE non \_ \_ mappé**
</dt> <dd>

Un participant a été démappé d’un sous-flux.

</dd> <dt>

<span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**\_ \_ délai d’attente des participants PE**
</dt> <dd>

Un participant a été supprimé de la Conférence en raison d’un délai d’attente.

</dd> <dt>

<span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**\_participant PE \_ récupéré**
</dt> <dd>

Un participant supprimé est de nouveau visible. En règle générale, il s’agit d’un participant qui a dépassé le délai d’attente, mais les signaux sont maintenant reçus.

</dd> <dt>

<span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**\_participant PE \_ actif**
</dt> <dd>

Le participant est devenu actif dans la Conférence.

</dd> <dt>

<span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**\_participant PE \_ inactif**
</dt> <dd>

Le participant est devenu inactif dans la Conférence.

</dd> <dt>

<span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_communication locale \_ PE**
</dt> <dd>

Le participant local a commencé à parler.

</dd> <dt>

<span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ local en \_ mode silencieux**
</dt> <dd>

Le participant local est devenu silencieux dans la Conférence.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                              |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipantEvent :: obtient l' \_ événement**](itparticipantevent-get-event.md)
</dt> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> <dt>

[Interfaces MSP IPConf](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




