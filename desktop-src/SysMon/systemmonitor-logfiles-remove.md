---
title: LogFiles. Remove, méthode
description: Supprime l’instance LogFileItem spécifiée de la collection.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Supprimer la méthode SysMon
- Remove, méthode SysMon, classe LogFiles
- LogFiles, classe SysMon, Remove, méthode
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742933"
---
# <a name="logfilesremove-method"></a>LogFiles. Remove, méthode

Supprime l’instance [**LogFileItem**](logfileitem.md) spécifiée de la collection.

## <a name="syntax"></a>Syntaxe


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

Index entier du fichier journal à supprimer de la collection. L’index est de base un.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

**Avant Windows Vista :** Vous ne pouvez pas supprimer les fichiers journaux de la [**collection de fichiers journaux**](systemmonitor-logfiles.md) si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur sysmonLogFiles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





