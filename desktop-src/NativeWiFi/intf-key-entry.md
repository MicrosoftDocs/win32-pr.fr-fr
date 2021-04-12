---
description: Stocke les informations clés relatives à une interface de réseau local sans fil gérée par le service de configuration sans fil.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: Structure INTF_KEY_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318534"
---
# <a name="intf_key_entry-structure"></a>Structure d’entrée de \_ clé INTF \_

\[**INTF \_ L' \_ entrée de clé** n’est plus prise en charge à partir de Windows Vista et windows Server 2008. Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires. Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]

La structure d' **\_ \_ entrée de clé INTF** stocke les informations clés sur une interface de réseau local sans fil gérée par le service de configuration sans fil.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**wszGuid**
</dt> <dd>

Pointeur vers le GUID d’interface représenté sous la forme d’une chaîne Unicode au format suivant : "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête *wzcsapi. h* n’est pas disponible dans le SDK Windows.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| Fin de la prise en charge des clients<br/>    | Windows XP avec SP3<br/>                                                       |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_table de clé INTFS \_**](intfs-key-table.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> </dl>

 

 




