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
ms.openlocfilehash: bed0ea39809d3dfe40ebcedf2fbf2105833af836c12b95ffdfe442d3956d52a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882179"
---
# <a name="systemmonitorlogfiles-property"></a>SystemMonitor. LogFiles, propriété

Collection d’un ou de plusieurs fichiers journaux à utiliser comme source des valeurs de compteur affichées dans le moniteur système.

## <a name="syntax"></a>Syntaxe


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Valeur de la propriété

Collection d’objets [**LogFileItem**](logfileitem.md) qui spécifient les fichiers journaux utilisés comme source de données pour le graphique.

## <a name="remarks"></a>Remarques

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

 

 





