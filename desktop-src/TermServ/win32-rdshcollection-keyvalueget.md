---
title: Méthode KeyValueGet de la classe Win32_RDSHCollection
description: Récupère la valeur associée à la clé spécifiée dans la collection.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode KeyValueGet
- Services Bureau à distance de la méthode KeyValueGet, classe Win32_RDSHCollection
- Win32_RDSHCollection de la classe Services Bureau à distance, méthode KeyValueGet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 943db8db044758e7f78e7d79b4ae5280c6ce51281b5858237a24e5f83add33a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422679"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a>Méthode KeyValueGet de la \_ classe Win32 RDSHCollection

Récupère la valeur associée à la clé spécifiée dans la collection.

## <a name="syntax"></a>Syntaxe


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Clé qui identifie la valeur que vous souhaitez récupérer.

</dd> <dt>

*Valeur* \[ à\]
</dt> <dd>

En cas de réussite, retourne la valeur associée à la clé spécifiée.

</dd> </dl>

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

 

 





