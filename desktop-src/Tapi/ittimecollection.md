---
description: L’interface ITTimeCollection est une interface propre au fournisseur pour l’objet blob de conférence du protocole SDP (session descripteur).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interface ITTimeCollection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525424"
---
# <a name="ittimecollection-interface"></a>Interface ITTimeCollection

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITTimeCollection** est une interface propre au fournisseur pour l’objet blob de conférence du protocole SDP (session descripteur). Cette interface permet l’accès aux interfaces [**ITTime**](ittime.md) par index, ainsi que la création et la suppression de composants de temps. La méthode [**ITSdp :: obten \_ TimeCollection**](itsdp-get-timecollection.md) crée l’interface **ITTimeCollection** .

## <a name="members"></a>Membres

L’interface **ITTimeCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITTimeCollection** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITTimeCollection** possède ces méthodes.



| Méthode                                                           | Description                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Créés**](ittimecollection-create.md)                        | Crée un composant [**ITTime**](ittime.md) .<br/>                                                             |
| [**Supprimer**](ittimecollection-delete.md)                        | Supprime un composant [**ITTime**](ittime.md) .<br/>                                                             |
| [**Obtient la \_ \_ NewEnum**](ittimecollection-get--newenum.md)          | Retourne un énumérateur pour cette collection.<br/>                                                                  |
| [**nombre d’extractions \_**](ittimecollection-get-count.md)                 | Obtient le nombre d’éléments dans la collection.<br/>                                                                        |
| [**Obtient \_ EnumerationIf**](ittimecollection-get-enumerationif.md) | Retourne l’interface d’énumération [**IEnumTime**](ienumtime.md) qui énumère [**ITTime**](ittime.md).<br/> |
| [**recevoir un \_ élément**](ittimecollection-get-item.md)                   | Pour un index donné, retourne un élément dans la collection.<br/>                                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

