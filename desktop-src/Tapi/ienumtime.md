---
description: 'L’interface IEnumTime fournit des méthodes d’énumération COM standard pour l’interface ITTime. La méthode ITTimeCollection :: obtenir \_ EnumerationIf retourne un pointeur vers IEnumTime.'
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interface IEnumTime (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008758"
---
# <a name="ienumtime-interface"></a>Interface IEnumTime

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **IEnumTime** fournit des méthodes d’énumération COM standard pour l’interface [**ITTime**](ittime.md) . La méthode [**ITTimeCollection :: obtenir \_ EnumerationIf**](ittimecollection-get-enumerationif.md) retourne un pointeur vers **IEnumTime**.

## <a name="members"></a>Membres

L’interface **IEnumTime** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumTime** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumTime** possède ces méthodes.



| Méthode                           | Description                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumtime-clone.md) | Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.<br/> |
| [**Suivant**](ienumtime-next.md)   | Obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.<br/>                 |
| [**Réinitialiser**](ienumtime-reset.md) | Réinitialise au début de la séquence d’énumération.<br/>                                    |
| [**Ignorer**](ienumtime-skip.md)   | Ignore le nombre spécifié d’éléments dans la séquence d’énumération.<br/>           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

