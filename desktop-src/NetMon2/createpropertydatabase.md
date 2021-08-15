---
description: La fonction CreatePropertyDatabase crée une base de données de propriétés qui stocke les propriétés d’un protocole.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: CreatePropertyDatabase, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7c07f6f3e4569c06f0b3890e3ef3a26bca10b3272849fc005dfb3be6cbc2836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367216"
---
# <a name="createpropertydatabase-function"></a>CreatePropertyDatabase fonction)

La fonction **CreatePropertyDatabase** crée une base de données de propriétés qui stocke les propriétés d’un protocole.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProtocol* \[ dans\]
</dt> <dd>

Handle du protocole associé à la base de données. Lorsque Moniteur réseau appelle la fonction [Register](register-parser.md) , moniteur réseau transmet le descripteur de protocole à la dll de l’analyseur.

</dd> <dt>

*nProperties* \[ dans\]
</dt> <dd>

Nombre de propriétés stockées dans la base de données. Définissez ce paramètre sur le nombre de propriétés prises en charge par le protocole.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est un code d’erreur.



| Code de retour                                                                                             | Description                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**\_erreur interne \_ NMERR**</dt> </dl>   | Une erreur interne s'est produite.<br/>                                     |
| <dl> <dt>**NMERR \_ non valide \_ HPOTOCOL**</dt> </dl> | Le descripteur du protocole spécifié dans *hProtocol* n’est pas valide.<br/>     |
| <dl> <dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt> </dl>   | Moniteur réseau ne dispose pas de suffisamment de mémoire pour créer la base de données.<br/> |



 

## <a name="remarks"></a>Remarques

La fonction **CreatePropertyDatabase** doit être appelée uniquement lors de l’implémentation de la fonction [Register](register-parser.md) . L’analyseur utilise **CreatePropertyDatabase** pour créer une base de données de propriétés qui décrit les propriétés d’un protocole. Moniteur réseau utilise la base de données pour interpréter les informations contenues dans le protocole.

La fonction **CreatePropertyDatabase** alloue les structures dont Moniteur réseau a besoin pour gérer une base de données de propriétés.

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

[S’inscrire](register-parser.md)
</dt> </dl>

 

 




