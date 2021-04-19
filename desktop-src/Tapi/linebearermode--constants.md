---
description: Les \_ constantes d’indicateur de bit LINEBEARERMODE décrivent les différents modes de support d’un appel.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: Constantes LINEBEARERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537884"
---
# <a name="linebearermode_-constants"></a>\_Constantes LINEBEARERMODE

Les constantes d’indicateur de bit **LINEBEARERMODE \_** décrivent les différents modes de support d’un appel. Lorsqu’une application effectue un appel, elle peut demander un mode de support spécifique. Ces modes permettent de sélectionner une certaine qualité de service pour la connexion demandée à partir du réseau téléphonique sous-jacent. Les modes de support disponibles sur une ligne donnée sont une fonctionnalité de l’appareil de la ligne.

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**
</dt> <dd> <dl> <dt>



Autre transfert de données vocales ou non restreintes sur le même appel (RNIS).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**\_données LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Transfert de données non restreintes sur l’appel. Le débit de données est spécifié séparément.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ Multiuse**
</dt> <dd> <dl> <dt>



Mode multi-multiple défini par RNIS.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**
</dt> <dd> <dl> <dt>



Cela correspond à une connexion de signal non associée à un appel entre l’application et le fournisseur de services ou le commutateur (traitée comme un flux de média par TAPI).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE \_ passthrough**
</dt> <dd> <dl> <dt>



Lorsqu’un appel est actif dans LINEBEARERMODE \_ passthrough, le fournisseur de services offre un accès direct au matériel attaché pour le contrôle par l’application. Ce mode est principalement utilisé par les applications qui souhaitent disposer d’un contrôle direct temporaire sur les modems asynchrones, accessibles via les [fonctions de communication](/windows/desktop/DevIO/communications-functions), afin de configurer ou d’utiliser des fonctionnalités spéciales non prises en charge par le fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**
</dt> <dd> <dl> <dt>



Service porteur pour les données numériques dans laquelle seuls les sept bits de poids faible de chaque octet peuvent contenir des données utilisateur (par exemple, pour un service 56Kbit/s commuté).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**\_parole LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Cela correspond à la transmission de la parole G. 711 sur l’appel. Le réseau peut utiliser des techniques de traitement telles que la transmission analogique, l’annulation de l’écho et la compression/décompression. L’intégrité des bits n’est pas assurée. La reconnaissance vocale n’est pas destinée à prendre en charge les types de média Fax et modem.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**\_voix LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Il s’agit d’un service de support analogique de niveau vocal 3,1 kHz standard. L’intégrité des bits n’est pas assurée. Voice peut prendre en charge les types de média Fax et modem.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil. Les 16 bits de poids faible sont réservés.

Notez que le mode porteur et le type de média sont des notions différentes. Le mode de support d’un appel est une indication de la qualité de la connexion téléphonique, comme fourni principalement par le réseau. Le type de média d’un appel est une indication du type de flux d’informations échangé sur cet appel. Le modem de télécopie ou de données de groupe 3 est un type de support qui utilise un appel avec un mode de support vocal 3,1 kHz.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

