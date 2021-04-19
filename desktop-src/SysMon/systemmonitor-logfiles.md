---
title: SystemMonitor. LogFiles, propriété
description: Collection d’un ou de plusieurs fichiers journaux à utiliser comme source des valeurs de compteur affichées dans le moniteur système.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Propriété LogFiles SysMon
- Propriété LogFiles SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, propriété LogFiles
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513779"
---
# <a name="systemmonitorlogfiles-property"></a>SystemMonitor. LogFiles, propriété

Collection d’un ou de plusieurs fichiers journaux à utiliser comme source des valeurs de compteur affichées dans le moniteur système.

## <a name="syntax"></a>Syntaxe


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Valeur de la propriété

Collection d’objets [**LogFileItem**](logfileitem.md) qui spécifient les fichiers journaux utilisés comme source de données pour le graphique.

## <a name="remarks"></a>Notes

Pour ajouter ou supprimer un fichier journal de la collection de fichiers journaux, la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) ne doit pas être définie sur sysmonLogFiles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





