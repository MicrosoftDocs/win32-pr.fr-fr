---
description: Manipule une description de conférence textuelle.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interface ITConferenceBlob (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa130e4456f206b27e41d03ead47138c777f9dad9e41d5d834bb018b29fc5447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119379089"
---
# <a name="itconferenceblob-interface"></a>Interface ITConferenceBlob

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITConferenceBlob** manipule une description de conférence textuelle. L’interface est destinée à être indépendante du format et de la syntaxe de la description de la Conférence. Pour manipuler des aspects spécifiques de la description de la Conférence, l’application doit interroger une autre interface. Actuellement, seules les descriptions de conférence SDP sont prises en charge ; l’application doit utiliser **QueryInterface** pour [**ITSdp**](itsdp.md) pour accéder aux différents champs de la description de la Conférence SDP. L’interface **ITConferenceBlob** est créée en appelant **QueryInterface** sur [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Membres

L’interface **ITConferenceBlob** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITConferenceBlob** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITConferenceBlob** possède ces méthodes.



| Méthode                                                             | Description                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ CharacterSet**](itconferenceblob-get-characterset.md)     | Obtient l’indicateur de [**\_ \_ jeu de caractères BLOB**](blob-character-set.md) indiquant si les caractères BLOB sont au format ASCII, Unicode, etc.<br/> |
| [**Obtient \_ ConferenceBlob**](itconferenceblob-get-conferenceblob.md) | Obtient un pointeur vers l’objet blob de conférence.<br/>                                                                                             |
| [**Rein**](itconferenceblob-init.md)                              | Initialise l’objet blob de conférence.<br/>                                                                                                   |
| [**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)    | Valide les modifications apportées à l’objet blob de conférence.<br/>                                                                                            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

