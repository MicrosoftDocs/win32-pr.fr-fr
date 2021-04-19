---
description: Les \_ constantes LINEMEDIAMODE décrivent les types de média (ou modes) d’une session ou d’un appel de communication.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: Constantes LINEMEDIAMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539999"
---
# <a name="linemediamode_-constants"></a>\_Constantes LINEMEDIAMODE

Les constantes **LINEMEDIAMODE \_** décrivent les types de média (ou modes) d’une session ou d’un appel de communication.

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**
</dt> <dd> <dl> <dt>



L’énergie vocale a été détectée lors de l’appel et la voix est gérée localement par une application automatisée telle qu’une application de machine de réponse. Lorsqu’un fournisseur de services ne peut pas faire la distinction entre l’interactivité et la voix automatisée sur un appel entrant, il signale l’appel comme interactif vocal.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAMODEM**
</dt> <dd> <dl> <dt>



Une session de modem de données sur l’appel. Les protocoles de modem actuels requièrent la station appelée pour initier le protocole de transfert. Pour un appel de modem de données entrant, l’application ne peut généralement pas effectuer de détection positive. La manière dont le fournisseur de services effectue cette détermination est son choix. Par exemple, une période de silence juste après avoir répondu à un appel entrant peut être utilisée comme heuristique pour décider qu’il peut s’agir d’un appel de modem de données.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**
</dt> <dd> <dl> <dt>



Session ADSI (ANALOG DISPLAY services interface) sur l’appel. ADSI améliore les appels vocaux avec des informations alphanumériques téléchargées sur le téléphone et l’utilisation de boutons logiciels sur le téléphone.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**
</dt> <dd> <dl> <dt>



Flux de données numériques d’un format non spécifié.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**
</dt> <dd> <dl> <dt>



Une télécopie de groupe 3 est envoyée ou reçue via l’appel.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**
</dt> <dd> <dl> <dt>



Une télécopie de groupe 4 est en cours d’envoi ou de réception sur l’appel.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**
</dt> <dd> <dl> <dt>



L’énergie vocale a été détectée lors de l’appel, et l’appel est traité comme un appel vocal interactif avec des humains aux deux extrémités.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ mixte**
</dt> <dd> <dl> <dt>



Session mixte sur l’appel. Mixed est l’un des services télématiques RNIS.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**
</dt> <dd> <dl> <dt>



Une session TDD (appareils de téléphonie pour les sourds) sur l’appel.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ TELETEX**
</dt> <dd> <dl> <dt>



Session TELETEX sur l’appel. Teletex est l’un des services télématiques.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**\_télex LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



Session de télex sur l’appel. Le télex est l’un des services télématiques.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**\_vidéo LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



Le type de média de l’appel est vidéo. (TAPI versions 2,1 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**
</dt> <dd> <dl> <dt>



Une session Videotex sur l’appel. Videotex est l’un des services télématiques.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**
</dt> <dd> <dl> <dt>



Le type de média de l’appel est VoiceView. (TAPI versions 1,4 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ inconnu**
</dt> <dd> <dl> <dt>



Un flux de média existe mais son mode n’est pas actuellement connu et peut devenir connu ultérieurement. Cela correspond à un appel avec un type de média non classifié. Dans les environnements de téléphonie analogique classiques, le type de média d’un appel entrant peut être inconnu jusqu’à ce que l’appel ait répondu et que le flux de média ait été filtré pour effectuer une détermination.

Si l’indicateur de mode multimédia inconnu est défini, d’autres indicateurs multimédias peuvent également être définis. Cela permet d’indiquer que le média est inconnu, mais qu’il est susceptible d’être l’un des autres types de médias sélectionnés.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Tous les 32 bits sont réservés.

Notez que le mode porteur et le type de média sont des notions différentes. Le mode de support d’un appel est une indication de la qualité de la connexion téléphonique, comme fourni principalement par le réseau. Le type de média d’un appel est une indication du type de flux d’informations échangé sur cet appel. Le modem de télécopie ou de données de groupe 3 est un type de support qui utilise un appel avec un mode de support vocal 3,1 kHz.

Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser cette \_ valeur LINEMEDIAMODE si elle n’est pas prise en charge sur la version négociée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




