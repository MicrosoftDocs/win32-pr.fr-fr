---
description: La fonction GetProtocolFromTable retourne un handle à un protocole&\# 8212 ; en fonction d’une table de remise et d’une valeur données.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: GetProtocolFromTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950957"
---
# <a name="getprotocolfromtable-function"></a>GetProtocolFromTable fonction)

La fonction **GetProtocolFromTable** retourne un handle à un protocole basé sur une table de remise et une valeur données.

## <a name="syntax"></a>Syntaxe


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*htable* \[ dans\]
</dt> <dd>

Handle vers une table de remise.

</dd> <dt>

*ItemToFind* \[ dans\]
</dt> <dd>

Valeur utilisée pour localiser le protocole dans une table de remise. La valeur doit être disponible dans les données de protocole.

</dd> <dt>

*lpInstData* \[ à\]
</dt> <dd>

S’il est disponible dans la table de remise, données d’instance pour le protocole suivant. La longueur des données d’instance ne peut pas être supérieure à celle \_ d’un PTR DWORD.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un handle de protocole.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Lors de l’implémentation de la fonction d’exportation [RecognizeFrame](recognizeframe.md) , la fonction **GetProtocolFromTable** est utilisée pour obtenir un handle pour le protocole suivant. La fonction **GetProtocolFromTable** est appelée pour récupérer un handle à partir du protocole suivant si le protocole identifie le protocole qui suit.

**Données d’instance**

Les données d’instance peuvent être des données qui sont inférieures ou égales à un \_ ptr DWORD en longueur, ou un pointeur vers des données, telles que des données de trame brutes, qui n’a pas besoin d’être alloué ou libéré par l’analyseur.

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

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




