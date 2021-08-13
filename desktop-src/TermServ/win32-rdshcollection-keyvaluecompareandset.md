---
title: Méthode KeyValueCompareAndSet de la classe Win32_RDSHCollection
description: Compare la clé spécifiée dans la collection avec un comparand ; Si elles correspondent, la nouvelle valeur est affectée à la clé. Si la clé n’existe pas, la méthode insère la clé dans la collection.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode KeyValueCompareAndSet
- Services Bureau à distance de la méthode KeyValueCompareAndSet, classe Win32_RDSHCollection
- Win32_RDSHCollection de la classe Services Bureau à distance, méthode KeyValueCompareAndSet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e1aaaf90313c8c1434a65c4ffd1045933ad503245f0dacbf78c2b7e1ca054a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422709"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Méthode KeyValueCompareAndSet de la \_ classe Win32 RDSHCollection

Compare la clé spécifiée dans la collection avec un comparand ; Si elles correspondent, la nouvelle valeur est affectée à la clé. Si la clé n’existe pas, la méthode insère la clé dans la collection.

## <a name="syntax"></a>Syntaxe


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Clé à comparer.

</dd> <dt>

*NewValue* \[ dans\]
</dt> <dd>

Nouvelle valeur.

</dd> <dt>

*Comparand* \[ dans\]
</dt> <dd>

Chaîne à laquelle comparer la clé.

</dd> <dt>

*InitialValue* \[ à\]
</dt> <dd>

En cas de réussite ou d’échec, contient la valeur initiale de la clé.

</dd> </dl>

## <a name="remarks"></a>Remarques

Notez que cette méthode peut récupérer la valeur de la clé et, par conséquent, encapsule les fonctionnalités de [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





