---
description: 'L’interface IEnumParticipant fournit des méthodes d’énumération COM standard pour l’interface ITParticipant. La méthode ITParticipantControl :: EnumerateParticipants retourne un pointeur vers IEnumParticipant.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interface IEnumParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ba6deb232b03a7923c8ea47e9e200f3d3ea9beb5bddcd0572e3cac4c2b6269
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003577"
---
# <a name="ienumparticipant-interface"></a>Interface IEnumParticipant

\[**IEnumParticipant** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **IEnumParticipant** fournit des méthodes d’énumération COM standard pour l’interface [**ITParticipant**](itparticipant.md) . La méthode [**ITParticipantControl :: EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) retourne un pointeur vers **IEnumParticipant**.

l’interface **IEnumParticipant** est masquée dans les langages de script et de Visual Basic.

## <a name="members"></a>Membres

L’interface **IEnumParticipant** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumParticipant** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumParticipant** possède ces méthodes.



| Méthode                                  | Description                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Répliqué**](ienumparticipant-clone.md) | Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.<br/> |
| [**Suivant**](ienumparticipant-next.md)   | Obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.<br/>                 |
| [**Initialisation**](ienumparticipant-reset.md) | Réinitialise au début de la séquence d’énumération.<br/>                                    |
| [**Saut**](ienumparticipant-skip.md)   | Ignore le nombre spécifié d’éléments dans la séquence d’énumération.<br/>           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

