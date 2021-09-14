---
description: Ajoute des données à un objet de hachage spécifié.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: A_SHAUpdate, fonction (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123294"
---
# <a name="a_shaupdate-function"></a>Une \_ fonction SHAUpdate

Ajoute des données à un objet de hachage spécifié.

## <a name="syntax"></a>Syntaxe


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Contexte* \[ in, out\]
</dt> <dd>

Contexte SHA.

</dd> <dt>

*Mémoire tampon* \[ à\]
</dt> <dd>

Table de hachage.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Taille de la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction peut être appelée plusieurs fois pour calculer le hachage sur des flux de données longs ou des flux de données discontinus. La [**fonction \_ SHAFinal**](a-shafinal.md) doit être appelée avant la récupération de la valeur de hachage.

Cette fonction est très similaire à SHAUpdate, mais elle est appelée directement à partir de la bibliothèque, plutôt que d’être routée via l’infrastructure de chiffrement. pour plus d’informations, consultez [Windows les fournisseurs NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Bibliothèque<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
