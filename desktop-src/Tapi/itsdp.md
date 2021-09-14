---
description: L’interface ITSdp fournit des méthodes pour la manipulation d’un protocole SDP (session descripteur), consultez le composant objet blob de conférence RFC 2327.
ms.assetid: 77c1e302-6290-4eeb-b7c9-462a13b29dcd
title: Interface ITSdp (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401dbe2548375227be2ca024ee75de3054fa6f6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013487"
---
# <a name="itsdp-interface"></a>Interface ITSdp

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITSdp** fournit des méthodes pour la manipulation d’un protocole SDP (session descripteur), consultez le composant objet blob de conférence RFC 2327. Il présente les caractéristiques suivantes :

-   Fournit l’accès à certaines propriétés qui sont communes à tous les médias. Celles-ci incluent des attributs se rapportant aux informations personnelles, à la description de session et aux informations de type d’adresse du créateur.
-   Fournit le point de départ pour accéder au temps et aux collections multimédias par le biais de propriétés.

L’interface **ITSdp** est créée en appelant **QueryInterface** sur [**ITConferenceBlob**](itconferenceblob.md).

## <a name="members"></a>Membres

L’interface **ITSdp** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITSdp** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITSdp** possède ces méthodes.



| Méthode                                                    | Description                                                                                         |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**récupérer la \_ Description**](itsdp-get-description.md)         | Obtient la description de la session.<br/>                                                            |
| [**Obtient \_ IsValid**](itsdp-get-isvalid.md)                 | Valide l’objet BLOB SDP pour les valeurs de structure et de champ.<br/>                                   |
| [**Obtient \_ MachineAddress**](itsdp-get-machineaddress.md)   | Obtient l’adresse de l’ordinateur hôte d’origine.<br/>                                        |
| [**Obtient \_ MediaCollection**](itsdp-get-mediacollection.md) | Obtient un pointeur vers l’interface [**ITMediaCollection**](itmediacollection.md) pour la Conférence.<br/> |
| [**nom d’accès \_**](itsdp-get-name.md)                       | Obtient le nom de la session.<br/>                                                                   |
| [**recevoir l' \_ expéditeur**](itsdp-get-originator.md)           | Obtient l’expéditeur de la Conférence.<br/>                                                              |
| [**Obtient \_ ProtocolVersion**](itsdp-get-protocolversion.md) | Obtient la version du protocole SDP.<br/>                                                           |
| [**recevoir \_ SessionID**](itsdp-get-sessionid.md)             | Obtient la valeur du protocole NTP (Network Time Protocol) 32 bits qui sert d’identificateur de session.<br/> |
| [**Obtient \_ SessionVersion**](itsdp-get-sessionversion.md)   | Obtient la valeur 32 bits (idéalement NTP) qui sert de version de session.<br/>                  |
| [**Obtient \_ TimeCollection**](itsdp-get-timecollection.md)   | Obtient un pointeur vers l’interface [**ITTimeCollection**](ittimecollection.md) pour la Conférence.<br/>   |
| [**accéder à l' \_ URL**](itsdp-get-url.md)                         | Obtient l'URL.<br/>                                                                            |
| [**GetEmailNames**](itsdp-getemailnames.md)              | Obtient le tableau des adresses et des noms de messagerie associés à l’objet blob de conférence.<br/>                |
| [**GetPhoneNumbers**](itsdp-getphonenumbers.md)          | Obtient les numéros de téléphone.<br/>                                                                  |
| [**Insérer une \_ Description**](itsdp-put-description.md)         | Définit la description de la session.<br/>                                                            |
| [**put \_ MachineAddress**](itsdp-put-machineaddress.md)   | Définit l’adresse de l’ordinateur hôte d’origine.<br/>                                        |
| [**nom de l’put \_**](itsdp-put-name.md)                       | Définit le nom de la session.<br/>                                                                   |
| [**Placer l' \_ expéditeur**](itsdp-put-originator.md)           | Obtient l’expéditeur de la Conférence.<br/>                                                              |
| [**put \_ SessionVersion**](itsdp-put-sessionversion.md)   | Définit la version de la session.<br/>                                                                    |
| [**\_URL put**](itsdp-put-url.md)                         | Définit l’URL.<br/>                                                                            |
| [**SetEmailNames**](itsdp-setemailnames.md)              | Définit le tableau des noms et adresses de messagerie associés à l’objet blob de conférence.<br/>                 |
| [**SetPhoneNumbers**](itsdp-setphonenumbers.md)          | Définit les numéros de téléphone.<br/>                                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

