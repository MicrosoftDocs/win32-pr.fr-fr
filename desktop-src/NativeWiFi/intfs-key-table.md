---
description: Contient la table d’informations clés de toutes les interfaces de réseau local sans fil gérées par le service de configuration sans fil.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: Structure INTFS_KEY_TABLE (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011596"
---
# <a name="intfs_key_table-structure"></a>Structure de table de \_ clés INTFS \_

\[**INTFS \_ la \_ TABLE de clés** n’est plus prise en charge à partir de Windows Vista et Windows Server 2008. Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires. Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]

La structure de **\_ \_ table de clés INTFS** contient la table d’informations de clé pour toutes les interfaces de réseau local sans fil gérées par le service de configuration sans fil.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwNumIntfs**
</dt> <dd>

Nombre total d’interfaces.

</dd> <dt>

**pIntfs**
</dt> <dd>

Pointeur vers la structure d' [**\_ \_ entrée de clé INTF**](intf-key-entry.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> le fichier d’en-tête *Wzcsapi. h* n’est pas disponible dans le SDK Windows.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| Fin de la prise en charge des clients<br/>    | Windows XP avec SP3<br/>                                                       |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




