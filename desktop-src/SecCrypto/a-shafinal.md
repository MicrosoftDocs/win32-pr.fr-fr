---
description: Calcule le hachage final des données entrées par la fonction MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: A_SHAFinal, fonction (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543782"
---
# <a name="a_shafinal-function"></a>Une \_ fonction SHAFinal

Calcule le hachage final des données entrées par la fonction MD5Update.

## <a name="syntax"></a>Syntaxe


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Contexte* \[ in, out\]
</dt> <dd>

Contexte SHA.

</dd> <dt>

*Résultat* \[ à\]
</dt> <dd>

Table de hachage résultante.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction est très similaire à SHAFinal, mais elle est appelée directement à partir de la bibliothèque, plutôt que d’être routée via l’infrastructure de chiffrement. Pour plus d’informations, consultez [fournisseurs NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Bibliothèque<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
