---
description: Le message QOSINFO de la ligne TSPI \_ force l’interface TAPI à déclencher un événement QoS. Pour plus d’informations, consultez ITQOSEvent.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Message LINE_QOSINFO (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e6273eb31447f0e0c9543dfa191a25869fa08f05be8a5c639ceb101deff47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873319"
---
# <a name="line_qosinfo-message"></a>\_Message QOSINFO de ligne

Le message **\_ QOSINFO** de la ligne TSPI force l’interface TAPI à déclencher un événement QoS. Pour plus d’informations, consultez [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) .


```C++
        
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*htLine* 
</dt> <dd>

Handle TAPI pour la ligne.

</dd> <dt>

*htCall* 
</dt> <dd>

Handle TAPI pour l’appel.

</dd> <dt>

*dwMsg* 
</dt> <dd>

La ligne de valeur \_ QOSINFO.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Membre de l’énumérateur [**d' \_ événements QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) qui identifie le type d’événement.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Constante de [type de média](./tapiprotocol--constants.md) qui identifie le média de l’appel associé à cet événement.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_événement QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

