---
description: Les \_ constantes d’indicateur de bit LINECALLHUBTRACKING décrivent le type de suivi de hub d’appel fourni.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Constantes LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525469"
---
# <a name="linecallhubtracking_-constants"></a>\_Constantes LINECALLHUBTRACKING

Les constantes d’indicateur de bit **LINECALLHUBTRACKING \_** décrivent le type de suivi de hub d’appel fourni.

<dl> <dt>

<span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING \_ ALLCALLS**
</dt> <dd> <dl> <dt>



Le suivi des concentrateurs d’appels est fourni au niveau de l’appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ aucun**
</dt> <dd> <dl> <dt>



Aucun suivi d’appel du Hub n’est fourni.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING \_ PROVIDERLEVEL**
</dt> <dd> <dl> <dt>



Les hubs d’appel sont suivis au niveau du fournisseur de services. Les appels par modification des appels ne sont pas signalés.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Lorsque des modifications se produisent dans cette structure de données, un message [**\_ CALLINFO de ligne**](line-callinfo.md) est envoyé à l’application. Les paramètres de ce message sont un descripteur de l’appel et une indication de l’élément d’information qui a changé. La structure de données [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) indique le type de suivi fourni.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CALLINFO de ligne \_**](line-callinfo.md)
</dt> <dt>

[**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




