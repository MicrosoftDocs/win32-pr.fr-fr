---
description: L’interface ITMediaCollection fournit l’accès à l’ensemble d’informations de média dans une description de conférence SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interface ITMediaCollection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540973"
---
# <a name="itmediacollection-interface"></a>Interface ITMediaCollection

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITMediaCollection** fournit l’accès à l’ensemble d’informations de média dans une description de conférence SDP (RFC 2327). Chaque description de support dans le SDP est décrite par une interface [**ITMedia**](itmedia.md) . **ITMediaCollection** permet de manipuler le jeu d’informations de **ITMEDIA** pour le SDP, y compris :

-   Autorise l’accès aux médias par index.
-   Permet la création et la suppression de médias.

La méthode [**ITSdp :: obten \_ MediaCollection**](itsdp-get-mediacollection.md) crée l’interface **ITMediaCollection** .

## <a name="members"></a>Membres

L’interface **ITMediaCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITMediaCollection** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITMediaCollection** possède ces méthodes.



| Méthode                                                            | Description                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Créés**](itmediacollection-create.md)                        | Crée un nouveau média avec les propriétés par défaut et le retourne.<br/> |
| [**Supprimer**](itmediacollection-delete.md)                        | Supprime le support correspondant à l’index spécifié.<br/>     |
| [**Obtient la \_ \_ NewEnum**](itmediacollection-get--newenum.md)          | Retourne un énumérateur pour cette collection.<br/>                   |
| [**nombre d’extractions \_**](itmediacollection-get-count.md)                 | Obtient le nombre de médias dans la session.<br/>                    |
| [**Obtient \_ EnumerationIf**](itmediacollection-get-enumerationif.md) | Obtient un pointeur vers l’interface d’énumération.<br/>                      |
| [**recevoir un \_ élément**](itmediacollection-get-item.md)                   | Retourne le média correspondant à l’index spécifié.<br/>     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

