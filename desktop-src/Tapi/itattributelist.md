---
description: L’interface ITAttributeList fournit des méthodes pour obtenir et définir des attributs non interprétés.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interface ITAttributeList (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526659"
---
# <a name="itattributelist-interface"></a>Interface ITAttributeList

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

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



 

