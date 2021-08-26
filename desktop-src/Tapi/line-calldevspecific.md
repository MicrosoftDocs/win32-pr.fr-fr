---
description: Le \_ message CALLDEVSPECIFIC de la ligne TSPI est envoyé à la fonction de rappel LINEEVENT pour notifier à l’interface TAPI les événements spécifiques à l’appareil qui se produisent lors d’un appel.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: Message LINE_CALLDEVSPECIFIC (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9930da3c30d51781b10b28ed7a712cb681950eaea1a387212a5e0894658a9125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012599"
---
# <a name="line_calldevspecific-message"></a>\_Message CALLDEVSPECIFIC de ligne

Le message **\_ CALLDEVSPECIFIC** de la ligne TSPI est envoyé à la fonction de rappel [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) pour notifier à l’interface TAPI les événements spécifiques à l’appareil qui se produisent lors d’un appel. La signification du message et l’interprétation du *dwParam1* via les paramètres *dwParam3* sont spécifiques à l’appareil.


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

La ligne de valeur \_ CALLDEVSPECIFIC.

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

## <a name="remarks"></a>Remarques

Le message de **ligne \_ CALLDEVSPECIFIC** est utilisé par un fournisseur de services conjointement avec la fonction [**\_ lineDevSpecific TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) . Sa signification est spécifique à l’appareil.

L’interface TAPI envoie le message [**\_ DEVSPECIFIC de ligne**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) aux applications en réponse à la réception de ce message d’un fournisseur de services. Les paramètres *htLine* et *htCall* sont traduits dans le *hCall* approprié en tant que paramètre *hDevice* au niveau de l’interface TAPI. Les paramètres *dwParam1*, *dwParam2* et *dwParam3* sont transmis sans modification.

Il n’y a aucun message directement correspondant au niveau de l’interface TAPI, bien que ce message soit très similaire à la [**ligne \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)). Au niveau de TSPI, les messages spécifiques à l’appareil sont répartis entre les événements de rapport sur les lignes et les adresses, et ces événements de rapport sur les appels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DEVSPECIFIC de ligne \_**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

