---
description: L’interface ITMedia est une représentation de média dans un protocole SDP (session Description Protocol), consultez RFC 2327.
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interface ITMedia (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526327"
---
# <a name="itmedia-interface"></a>Interface ITMedia

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITMedia** est une représentation de média dans un protocole SDP (session Description Protocol), consultez RFC 2327. Cette interface exporte des méthodes pour récupérer et définir des propriétés de média de base, telles que le type. Les méthodes [**ITMediaCollection :: obten \_ Item**](itmediacollection-get-item.md) et [**ITMediaCollection :: Create**](itmediacollection-create.md) créent l’interface **ITMedia** .

## <a name="members"></a>Membres

L’interface **ITMedia** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITMedia** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITMedia** possède ces méthodes.



| Méthode                                                          | Description                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Obtient \_ FormatCodes**](itmedia-get-formatcodes.md)             | Obtient la liste des codes de format de charge utile du média.<br/>                                          |
| [**recevoir \_ MEDIANAME**](itmedia-get-medianame.md)                 | Obtient le nom du support.<br/>                                                                  |
| [**Obtient \_ MediaTitle**](itmedia-get-mediatitle.md)               | Obtient le titre du support.<br/>                                                                 |
| [**Obtient \_ NumPorts**](itmedia-get-numports.md)                   | Obtient le nombre de ports nécessaires pour la session.<br/>                                      |
| [**Obtient \_ StartPort**](itmedia-get-startport.md)                 | Obtient la valeur de port 16 bits pour le premier port.<br/>                                        |
| [**Obtient \_ TransportProtocol**](itmedia-get-transportprotocol.md) | Obtient le protocole de transport.<br/>                                                          |
| [**put \_ FormatCodes**](itmedia-put-formatcodes.md)             | Définit la liste des codes de format de charge utile du média.<br/>                                          |
| [**put \_ MEDIANAME**](itmedia-put-medianame.md)                 | Définit le nom du support.<br/>                                                                  |
| [**put \_ MediaTitle**](itmedia-put-mediatitle.md)               | Définit le titre du support.<br/>                                                                 |
| [**put \_ TransportProtocol**](itmedia-put-transportprotocol.md) | Définit le protocole de transport.<br/>                                                          |
| [**SetPortInfo**](itmedia-setportinfo.md)                      | Définit la valeur du port 16 bits pour le premier port et le nombre de ports nécessaires pour la session.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**ITSDP**](itsdp.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

