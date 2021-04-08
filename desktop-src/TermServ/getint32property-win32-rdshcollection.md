---
title: Méthode GetInt32Property de la classe Win32_RDSHCollection (Microsoft. Diagnostics. appanalysis. h)
description: Récupère une valeur de propriété entière d’un \_ objet Win32 RDSHCollection.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetInt32Property
- Services Bureau à distance de la méthode GetInt32Property, classe Win32_RDSHCollection
- Win32_RDSHCollection de la classe Services Bureau à distance, méthode GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5cc29234fe3bb1b92e68e728423931da965391f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740405"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a>Méthode GetInt32Property de la \_ classe Win32 RDSHCollection

Récupère une valeur de propriété entière d’un objet [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Clé qui identifie la propriété à récupérer.

</dd> <dt>

*Valeur* \[ à\]
</dt> <dd>

Reçoit la valeur de la propriété récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                                 |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                                   |
| En-tête<br/>                   | <dl> <dt>Microsoft. Diagnostics. appanalysis. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





