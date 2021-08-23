---
description: La fonctionnalité de l’interface ITConnection est illustrée ci-dessous.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interface ITConnection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64758f6a5cf7bcd9106504412f4cf7f39e6fb7ca0b76e35b38e19dc3f815ccf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140342"
---
# <a name="itconnection-interface"></a>Interface ITConnection

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITConnection** fournit les fonctionnalités suivantes :

-   Permet d’accéder aux informations relatives à l’adresse et à la durée de vie (TTL) de la session.
-   Fournit l’accès aux informations de bande passante.
-   Active la manipulation de la clé de chiffrement.

L’interface **ITConnection** est créée en appelant **QueryInterface** sur [**ITConferenceBlob**](itconferenceblob.md).

## <a name="members"></a>Membres

L’interface **ITConnection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITConnection** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITConnection** possède ces méthodes.



| Méthode                                                               | Description                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ AddressType**](itconnection-get-addresstype.md)             | Obtient le type d’adresse.<br/>                                                                                                              |
| [**bénéficier de \_ la bande passante**](itconnection-get-bandwidth.md)                 | Obtient la valeur de bande passante.<br/>                                                                                                               |
| [**Obtient \_ BandwidthModifier**](itconnection-get-bandwidthmodifier.md) | Obtient le modificateur de bande passante.<br/>                                                                                                        |
| [**Obtient \_ NetworkType**](itconnection-get-networktype.md)             | Obtient le type de réseau.<br/>                                                                                                              |
| [**Obtient \_ NumAddresses**](itconnection-get-numaddresses.md)           | Obtient le nombre d’adresses à utiliser pour la session.<br/>                                                                            |
| [**Obtient \_ STARTADDRESS**](itconnection-get-startaddress.md)           | Obtient la première adresse à utiliser pour la session.<br/>                                                                                  |
| [**Obtient la \_ durée de vie**](itconnection-get-ttl.md)                             | Obtient l’étendue de la [*durée de*](t-tapgloss.md) vie (TTL) pour les transmissions sur les adresses.<br/> |
| [**GetEncryptionKey**](itconnection-getencryptionkey.md)            | Obtient la clé de chiffrement.<br/>                                                                                                            |
| [**put \_ AddressType**](itconnection-put-addresstype.md)             | Définit le type d’adresse.<br/>                                                                                                              |
| [**put \_ NetworkType**](itconnection-put-networktype.md)             | Définit le type de réseau.<br/>                                                                                                              |
| [**SetAddressInfo**](itconnection-setaddressinfo.md)                | Définit les informations d’adresse.<br/>                                                                                                           |
| [**SetBandwidthInfo**](itconnection-setbandwidthinfo.md)            | Définit la valeur de la bande passante.<br/>                                                                                                           |
| [**SetEncryptionKey**](itconnection-setencryptionkey.md)            | Définit la clé de chiffrement nécessaire pour déchiffrer la session ou une indication à un mécanisme pour obtenir une clé utilisable par un moyen externe.<br/>     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

