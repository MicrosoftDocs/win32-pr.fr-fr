---
description: Les \_ constantes d’indicateur de bit LINECALLHUBTRACKING décrivent le type de suivi de hub d’appel fourni.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Constantes LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98d24b9641e7662871aef64f1358eeddfb58f5c9400b45aee405b8c6d8f134a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405189"
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

## <a name="remarks"></a>Remarques

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

 

 




