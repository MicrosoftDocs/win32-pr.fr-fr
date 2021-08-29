---
description: 'L’interface IEnumMedia fournit des méthodes d’énumération COM standard pour l’interface ITMedia. La méthode ITMediaCollection :: obtenir \_ EnumerationIf retourne un pointeur vers IEnumMedia.'
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Interface IEnumMedia (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e180e861e452d841153127f6476ed5d8f5924480877eac78c4634e86437189f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660749"
---
# <a name="ienummedia-interface"></a>Interface IEnumMedia

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **IEnumMedia** fournit des méthodes d’énumération COM standard pour l’interface [**ITMedia**](itmedia.md) . La méthode [**ITMediaCollection :: obtenir \_ EnumerationIf**](itmediacollection-get-enumerationif.md) retourne un pointeur vers **IEnumMedia**.

## <a name="members"></a>Membres

L’interface **IEnumMedia** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumMedia** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumMedia** possède ces méthodes.



| Méthode                            | Description                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Répliqué**](ienummedia-clone.md) | Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.<br/> |
| [**Suivant**](ienummedia-next.md)   | Obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.<br/>                 |
| [**Initialisation**](ienummedia-reset.md) | Réinitialise au début de la séquence d’énumération.<br/>                                    |
| [**Saut**](ienummedia-skip.md)   | Ignore le nombre spécifié d’éléments dans la séquence d’énumération.<br/>           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

