---
title: Message DRV_OPEN (mmsystem. h)
description: Indique au pilote d’ouvrir une nouvelle instance.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- message DRV_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239802"
---
# <a name="drv_open-message"></a>DRV \_ message ouvert

Indique au pilote d’ouvrir une nouvelle instance.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificateur du pilote installable.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle de l’instance du pilote installable.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Adresse d’une chaîne de caractères larges se terminant par un caractère null qui spécifie les informations de configuration utilisées pour ouvrir l’instance. Si aucune information de configuration n’est disponible, soit cette chaîne est vide, soit le paramètre a la **valeur null**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

données spécifiques au pilote 32 bits.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur différente de zéro en cas de réussite ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Si le pilote retourne une valeur différente de zéro, le système utilise cette valeur comme identificateur de pilote (le paramètre *dwDriverId* ) dans les messages qu’il envoie par la suite à l’instance du pilote. Le pilote peut retourner n’importe quel type de valeur comme identificateur. Par exemple, certains pilotes retournent des adresses mémoire qui pointent vers des informations spécifiques à l’instance. L’utilisation de cette méthode de spécification des identificateurs pour une instance de pilote permet aux pilotes d’accéder aux informations pendant qu’ils traitent des messages.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Pilotes installables](installable-drivers.md)
</dt> <dt>

[Messages de pilote installables](installable-driver-messages.md)
</dt> </dl>

 

 





