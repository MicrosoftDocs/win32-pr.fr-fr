---
description: La fonction RKeyCloseKeyService n’est pas prise en charge.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: RKeyCloseKeyService, fonction (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862622"
---
# <a name="rkeyclosekeyservice-function"></a>RKeyCloseKeyService fonction)

La fonction **RKeyCloseKeyService** n’est pas prise en charge.

**Windows Server 2003 :** La fonction **RKeyCloseKeyService** ferme un handle de service de clé ouvert par un appel précédent à la fonction [**RKeyOpenKeyService**](rkeyopenkeyservice.md) . Notez que ce comportement a changé avec Windows Server 2003 avec Service Pack 1 (SP1).

## <a name="syntax"></a>Syntaxe


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hKeySvcCli* \[ dans\]
</dt> <dd>

Handle [**de \_ handle KEYSVCC**](keysvcc-handle.md) précédemment ouvert par [**RKeyOpenKeyService**](rkeyopenkeyservice.md). Cette valeur ne peut pas être **null**.

</dd> <dt>

*conservé* \[ in, out\]
</dt> <dd>

Réservé. Définissez cette valeur sur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est S \_ OK.

Si la fonction échoue, la valeur de retour est un **ULong** qui indique l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




