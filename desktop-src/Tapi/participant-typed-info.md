---
description: "Les membres de l' \\_ \\_ énumération info typées participant identifient le type d’informations sur les participants récupérés par la méthode ITParticipant :: obten \\_ ParticipantTypedInfo. Cette énumération est utilisée par les applications qui accèdent au MSP IPConf."
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Énumération PARTICIPANT_TYPED_INFO (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528723"
---
# <a name="participant_typed_info-enumeration"></a>\_Énumération des informations typées du participant \_

\[**Participant \_ Les \_ informations typées** ne peuvent pas être utilisées dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Les membres de l’énumération **\_ \_ info typées participant** identifient le type d’informations sur les participants récupérés par la méthode [**ITParticipant :: obten \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) . Cette énumération est utilisée par les applications qui accèdent au [MSP ipconf](ipconf-msp.md).

## <a name="syntax"></a>Syntaxe


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CANONICALNAME**
</dt> <dd>

Nom canonique du participant, tel que someone@example.com .

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**nom de PTI \_**
</dt> <dd>

Nom affichable du participant.

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EMAILADDRESS**
</dt> <dd>

Adresse e-mail du participant.

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**
</dt> <dd>

Adresse de téléphone du participant.

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**\_emplacement PTI**
</dt> <dd>

Adresse géographique du participant.

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_outil PTI**
</dt> <dd>

Application du participant.

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI \_ Notes**
</dt> <dd>

Notes relatives au participant.

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ privé**
</dt> <dd>

Définit une extension de description source expérimentale ou spécifique à l’application (SDES). Pour plus d’informations, consultez la RFC 1889.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipant :: obtient \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> <dt>

[Interfaces MSP IPConf](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




