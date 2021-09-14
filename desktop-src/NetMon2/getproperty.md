---
description: La fonction GetProperty retourne un handle vers une propriété donnée.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: GetProperty, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121401"
---
# <a name="getproperty-function"></a>GetProperty, fonction

La fonction **GetProperty** retourne un handle vers une propriété donnée.

## <a name="syntax"></a>Syntaxe


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProtocol* \[ dans\]
</dt> <dd>

Handle du protocole.

</dd> <dt>

*PropertyName* \[ dans\]
</dt> <dd>

Nom de la propriété (par exemple, **checksum**).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est le handle de la propriété.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

La fonction **GetProperty** peut être utilisée pour obtenir le handle de propriété nécessaire pour localiser les instances de la propriété. Les fonctions utilisées pour localiser les instances de propriété sont [FindPropertyInstance](findpropertyinstance.md) (qui localise la première instance) et [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (qui localise l’instance suivante).

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetProperty** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




