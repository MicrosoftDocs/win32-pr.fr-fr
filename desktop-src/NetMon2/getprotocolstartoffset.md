---
description: Retourne l’offset d’un protocole spécifié dans le frame.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: GetProtocolStartOffset, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121378"
---
# <a name="getprotocolstartoffset-function"></a>GetProtocolStartOffset fonction)

La fonction **GetProtocolStartOffset** retourne le décalage d’un protocole spécifié dans le frame.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* 
</dt> <dd>

Handle du frame.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Nom de protocole, tel que TCP.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est un décalage **DWORD** au début du protocole dans lequel la recherche d’une valeur de retour égale à zéro indique que le protocole est le premier protocole dans le frame.

Si la fonction échoue, le protocole n’est pas dans le frame, la valeur de retour est-1.

## <a name="remarks"></a>Notes

Quand le handle d’un frame est donné, cette fonction retourne l’offset à un protocole spécifié dans le frame. Par exemple, pour déterminer si le cadre est un frame DNS, l’analyseur DNS requiert l’adresse du port du protocole TCP. L’analyseur DNS appelle cette fonction avec TCP comme valeur *ProtocolName* . Si le frame est reconnu par le protocole TCP, le **mot** offset à partir du début du frame jusqu’au début de la trame TCP est retourné. S’il n’existe aucun protocole TCP, la valeur de retour est zéro.

Cette fonction recherche le début d’un protocole dans un frame.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




