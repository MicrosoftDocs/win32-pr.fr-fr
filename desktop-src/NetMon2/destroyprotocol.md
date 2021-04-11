---
description: La fonction DestroyProtocol détruit le protocole créé par la fonction CreateProtocol.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: DestroyProtocol, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202726"
---
# <a name="destroyprotocol-function"></a>DestroyProtocol fonction)

La fonction **DestroyProtocol** détruit le protocole créé par la fonction **CreateProtocol** .

## <a name="syntax"></a>Syntaxe


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProtocol* \[ dans\]
</dt> <dd>

Handle du protocole à détruire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Aucun.

## <a name="remarks"></a>Notes

La DLL de l’analyseur appelle la fonction **DestroyProtocol** lors de son implémentation de [DllMain](dllmain-parser.md). **DestroyProtocol** est appelé quand le système d’exploitation va décharger la dll.



| Pour plus d’informations sur                                        | Consultez                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau. | [Analyseurs](parsers.md)                                  |
| L’implémentation de **DllMain** comprend un exemple.         | [Implémentation de DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DllMain](dllmain-parser.md)
</dt> </dl>

 

 




