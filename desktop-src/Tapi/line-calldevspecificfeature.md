---
description: Le message CALLDEVSPECIFICFEATURE de la ligne TSPI \_ est envoyé à la fonction de rappel LINEEVENT pour notifier à l’interface TAPI les événements spécifiques à l’appareil qui se produisent sur une ligne ou une adresse.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: Message LINE_CALLDEVSPECIFICFEATURE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2891f019035f53be4dbc0a40de429e5c0d9dc567
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540655"
---
# <a name="line_calldevspecificfeature-message"></a>\_Message CALLDEVSPECIFICFEATURE de ligne

Le message **\_ CALLDEVSPECIFICFEATURE** de la ligne TSPI est envoyé à la fonction de rappel [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) pour notifier à l’interface TAPI les événements spécifiques à l’appareil qui se produisent sur une ligne ou une adresse. La signification du message et l’interprétation du *dwParam1* via les paramètres *dwParam3* sont spécifiques à l’appareil.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*htLine* 
</dt> <dd>

Handle de l’objet opaque TAPI sur le périphérique de ligne.

</dd> <dt>

*htCall* 
</dt> <dd>

Handle de l’objet opaque TAPI vers l’appareil d’appel.

</dd> <dt>

*dwMsg* 
</dt> <dd>

La ligne de valeur \_ CALLDEVSPECIFICFEATURE.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Spécifique à l’appareil.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spécifique à l’appareil.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Spécifique à l’appareil.

</dd> </dl>

## <a name="remarks"></a>Notes

Le message de **ligne \_ CALLDEVSPECIFICFEATURE** est utilisé par un fournisseur de services conjointement avec la fonction [**\_ lineDevSpecificFeature TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) . Sa signification est spécifique à l’appareil.

L’interface TAPI envoie le message [**\_ DEVSPECIFICFEATURE de ligne**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) aux applications en réponse à la réception de ce message d’un fournisseur de services. Les paramètres *htLine* et *htCall* sont traduits dans le *hCall* approprié en tant que paramètre *hDevice* au niveau de l’interface TAPI. Les paramètres *dwParam1*, *dwParam2* et *dwParam3* sont transmis sans modification.

Il n’y a aucun message directement correspondant au niveau de l’interface TAPI, bien que ce message soit très similaire à la ligne \_ DEVSPECIFICFEATURE. Au niveau de TSPI, les messages de fonctionnalités spécifiques à l’appareil sont répartis entre les événements de rapport sur les lignes et les adresses, et ces événements de rapport sur les appels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DEVSPECIFICFEATURE de ligne \_**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))
</dt> <dt>

[**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

