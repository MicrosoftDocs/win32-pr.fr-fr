---
description: Les \_ constantes LINEINITIALIZEEXOPTION spécifient le mécanisme de notification d’événement à utiliser lors de l’initialisation d’une session.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Constantes LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008741"
---
# <a name="lineinitializeexoption_-constants"></a>\_Constantes LINEINITIALIZEEXOPTION

Les constantes **LINEINITIALIZEEXOPTION \_** spécifient le mécanisme de notification d’événement à utiliser lors de l’initialisation d’une session.

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



L’application souhaite utiliser le mécanisme de notification d’événement de suivi de hub d’appel. Cette constante est exposée uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**
</dt> <dd> <dl> <dt>



L’application souhaite utiliser le mécanisme de notification d’événement du port d’achèvement. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**
</dt> <dd> <dl> <dt>



L’application souhaite utiliser le mécanisme de notification d’événement de handle d’événement. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**
</dt> <dd> <dl> <dt>



L’application souhaite utiliser le mécanisme de notification d’événements de fenêtre masquée. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Pour plus d’informations sur le fonctionnement de ces options, consultez [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




