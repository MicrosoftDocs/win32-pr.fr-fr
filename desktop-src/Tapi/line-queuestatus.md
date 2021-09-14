---
description: Le \_ message de ligne QUEUESTATUS est envoyé lorsque l’état d’une file d’attente ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Message LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217620"
---
# <a name="line_queuestatus-message"></a>\_Message QUEUESTATUS de ligne

Le message de **ligne \_ QUEUESTATUS** est envoyé lorsque l’état d’une file d’attente ACD change sur un gestionnaire d’agent pour lequel l’application a actuellement une ligne ouverte. Ce message est généré à l’aide de la fonction [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


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

Identificateur de la file d’attente dont l’État a changé.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Spécifie l’état de la file d’attente qui a changé. Il peut s’agir d’une ou plusieurs des [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




