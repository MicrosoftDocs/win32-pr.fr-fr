---
description: L’interface ITTime est une interface propre au fournisseur pour un objet blob de conférence SDP (session Descriptor Protocol).
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Interface ITTime (sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542301"
---
# <a name="ittime-interface"></a>Interface ITTime

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITTime** est une interface propre au fournisseur pour un objet blob de conférence SDP (session Descriptor Protocol). Il permet d’accéder à un ensemble de temps d’activation pour la session. Les méthodes [**IEnumTime :: Next**](ienumtime-next.md) et [**ITTimeCollection :: Create**](ittimecollection-create.md) créent l’interface **ITTime** .

## <a name="members"></a>Membres

L’interface **ITTime** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITTime** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITTime** possède ces méthodes.



| Méthode                                         | Description                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [**Obtient \_ StartTime**](ittime-get-starttime.md) | Obtient la valeur d’heure de début NTP (Network Time Protocol) 32 bits.<br/> |
| [**Obtient \_ StopTime**](ittime-get-stoptime.md)   | Obtient la valeur de l’heure de fin NTP.<br/>                                  |
| [**put \_ StartTime**](ittime-put-starttime.md) | Définit la valeur d’heure de début NTP 32 bits.<br/>                         |
| [**put \_ StopTime**](ittime-put-stoptime.md)   | Définit la valeur de l’heure de fin NTP.<br/>                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

