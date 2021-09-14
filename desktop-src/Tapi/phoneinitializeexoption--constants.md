---
description: Les \_ constantes PHONEINITIALIZEEXOPTION spécifient le mécanisme de notification d’événement à utiliser lors de l’initialisation d’une session.
ms.assetid: 7d8b122d-bebe-4904-abc8-d680b0899e25
title: Constantes PHONEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023f6801f65910bedf7d2637079694b4c6b6d85e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008731"
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

## <a name="remarks"></a>Remarques

Pour plus d’informations sur le fonctionnement de ces options, consultez [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




