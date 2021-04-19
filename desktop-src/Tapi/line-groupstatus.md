---
description: Le \_ message de ligne GROUPSTATUS est envoyé lorsque l’état d’un groupe ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: Message LINE_GROUPSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533040"
---
# <a name="line_groupstatus-message"></a>\_Message GROUPSTATUS de ligne

Le message de **ligne \_ GROUPSTATUS** est envoyé lorsque l’état d’un groupe ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle de l’application sur le périphérique de ligne. Cela est relatif au gestionnaire de l’agent.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spécifie l’état du groupe qui a changé. L’application peut appeler [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) pour déterminer les modifications apportées aux groupes disponibles. Le paramètre *dwParam2* est une ou plusieurs des [**\_ constantes LINEGROUPSTATUS**](linegroupstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




