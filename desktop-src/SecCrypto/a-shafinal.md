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
ms.openlocfilehash: 42a22cfca32409fdfa02586bb90c76f8e8f2489b22cfe2769b50d928d2564af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960288"
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

## <a name="remarks"></a>Remarques

Cette fonction est très similaire à SHAFinal, mais elle est appelée directement à partir de la bibliothèque, plutôt que d’être routée via l’infrastructure de chiffrement. pour plus d’informations, consultez [Windows les fournisseurs NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Bibliothèque<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
