---
description: Le \_ message ADDRESSSTATE de ligne TAPI est envoyé lorsque l’état d’une adresse est modifié sur une ligne actuellement ouverte par l’application. L’application peut appeler lineGetAddressStatus pour déterminer l’état actuel de l’adresse.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Message LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfc158bd41b635142252546fbc289ed868851a3ac79d80bddba2df6118715bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959879"
---
# <a name="line_addressstate-message"></a>\_Message ADDRESSSTATE de ligne

Le message **\_ ADDRESSSTATE de ligne** TAPI est envoyé lorsque l’état d’une adresse est modifié sur une ligne actuellement ouverte par l’application. L’application peut appeler [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) pour déterminer l’état actuel de l’adresse.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de l’appareil de ligne.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificateur d’adresse de l’adresse qui a modifié l’État.

</dd> <dt>

*dwParam2* 
</dt> <dd>

État de l’adresse qui a changé. Il peut s’agir d’une ou plusieurs des [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

La **ligne \_ ADDRESSSTATE** message est envoyée à toute application qui a ouvert le périphérique de ligne et qui a activé ce message. L’envoi de ce message pour les différents éléments d’État peut être contrôlé et interrogé à l’aide de [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) et [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Par défaut, le rapport d’état de l’adresse est désactivé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




