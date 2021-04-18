---
description: Les \_ constantes PHONEINITIALIZEEXOPTION spécifient le mécanisme de notification d’événement à utiliser lors de l’initialisation d’une session.
ms.assetid: 7d8b122d-bebe-4904-abc8-d680b0899e25
title: Constantes PHONEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023f6801f65910bedf7d2637079694b4c6b6d85e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540721"
---
# <a name="phoneinitializeexoption_-constants"></a>\_Constantes PHONEINITIALIZEEXOPTION

Les constantes **PHONEINITIALIZEEXOPTION \_** spécifient le mécanisme de notification d’événement à utiliser lors de l’initialisation d’une session.

<dl> <dt>

<span id="PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="phoneinitializeexoption_usecompletionport"></span>**PHONEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**
</dt> <dd> <dl> <dt>



L’application souhaite utiliser le mécanisme de notification d’événement du port d’achèvement.


</dt> </dl> </dd> <dt>

<span id="PHONEINITIALIZEEXOPTION_USEEVENT"></span><span id="phoneinitializeexoption_useevent"></span>**PHONEINITIALIZEEXOPTION \_ USEEVENT**
</dt> <dd> <dl> <dt>



L’application souhaite utiliser le mécanisme de notification d’événement de handle d’événement.


</dt> </dl> </dd> <dt>

<span id="PHONEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="phoneinitializeexoption_usehiddenwindow"></span>**PHONEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**
</dt> <dd> <dl> <dt>



L’application souhaite utiliser le mécanisme de notification d’événements de fenêtre masquée.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Pour plus d’informations sur le fonctionnement de ces options, consultez [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




