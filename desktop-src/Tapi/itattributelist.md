---
description: L’interface ITAttributeList fournit des méthodes pour obtenir et définir des attributs non interprétés.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interface ITAttributeList (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8dd0ac143791a09eedbd3fe575dcecb894a1fb6dbb218c8ecfdcadf60ebd60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762425"
---
# <a name="itattributelist-interface"></a>Interface ITAttributeList

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITAttributeList** fournit des méthodes pour obtenir et définir des attributs non interprétés. En ce qui concerne la position des chaînes d’attributs dans un protocole SDP (session descripteur), consultez le paquet RFC 2327), les méthodes supposent que toutes les chaînes d’attribut existent juste avant que les attributs de média soient spécifiés et après tous les attributs communs. L’interface **ITAttributeList** est créée en appelant **QueryInterface** sur [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Membres

L’interface **ITAttributeList** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITAttributeList** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITAttributeList** possède ces méthodes.



| Méthode                                                          | Description                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**Complémentaires**](itattributelist-add.md)                              | Ajoute l’attribut à l’index spécifié.<br/>   |
| [**Supprimer**](itattributelist-delete.md)                        | Supprime l’attribut à l’index spécifié.<br/> |
| [**Obtient \_ AttributeList**](itattributelist-get-attributelist.md) | Obtient la liste des attributs.<br/>                 |
| [**nombre d’extractions \_**](itattributelist-get-count.md)                 | Obtient le nombre d'attributs.<br/>               |
| [**recevoir un \_ élément**](itattributelist-get-item.md)                   | Obtient l’attribut spécifié par l’index.<br/>   |
| [**put \_ AttributeList**](itattributelist-put-attributelist.md) | Définit la liste des attributs.<br/>                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

