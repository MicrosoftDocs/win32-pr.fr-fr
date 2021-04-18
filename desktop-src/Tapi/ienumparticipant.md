---
description: 'L’interface IEnumParticipant fournit des méthodes d’énumération COM standard pour l’interface ITParticipant. La méthode ITParticipantControl :: EnumerateParticipants retourne un pointeur vers IEnumParticipant.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interface IEnumParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533394"
---
# <a name="ienumparticipant-interface"></a>Interface IEnumParticipant

\[**IEnumParticipant** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **IEnumParticipant** fournit des méthodes d’énumération COM standard pour l’interface [**ITParticipant**](itparticipant.md) . La méthode [**ITParticipantControl :: EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) retourne un pointeur vers **IEnumParticipant**.

L’interface **IEnumParticipant** est masquée dans les langages de script et de Visual Basic.

## <a name="members"></a>Membres

L’interface **IEnumParticipant** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumParticipant** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumParticipant** possède ces méthodes.



| Méthode                                  | Description                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Répliqué**](ienumparticipant-clone.md) | Crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.<br/> |
| [**Suivant**](ienumparticipant-next.md)   | Obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.<br/>                 |
| [**Réinitialiser**](ienumparticipant-reset.md) | Réinitialise au début de la séquence d’énumération.<br/>                                    |
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

 

