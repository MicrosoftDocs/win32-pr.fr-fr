---
title: SystemMonitor. LogFileName, propriété
description: Récupère ou définit le nom d’un fichier journal à utiliser comme source des valeurs de compteur affichées dans le moniteur système.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Propriété LogFileName SysMon
- Propriété LogFileName SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriété LogFileName
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384704"
---
# <a name="systemmonitorlogfilename-property"></a>SystemMonitor. LogFileName, propriété

Récupère ou définit le nom d’un fichier journal à utiliser comme source des valeurs de compteur affichées dans le moniteur système.

> [!Note]  
> Cette propriété a été rendue obsolète par la propriété [**LogFiles**](systemmonitor-logfiles.md) .

 

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property LogFileName As String
```



## <a name="property-value"></a>Valeur de la propriété

Chemin d’accès au fichier journal. Vous pouvez spécifier un chemin d’accès absolu, relatif ou UNC. L’extension de nom de fichier journal doit être. csv,. TSV ou. BLG.

## <a name="exceptions"></a>Exceptions



| Type d'exception                                  | Condition                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | Impossible de trouver le fichier spécifié. La valeur de Err. Number est 0xC0000BD1. |
| **System.ArgumentException**                    | Vous ne pouvez pas spécifier une chaîne vide.                                    |



 

## <a name="remarks"></a>Notes

Cette propriété retourne le nom du fichier journal à partir du premier membre de la collection [**LogFiles**](systemmonitor-logfiles.md) .

La définition de cette propriété échoue si la collection [**LogFiles**](systemmonitor-logfiles.md) contient un ou plusieurs membres.

Vous devez utiliser l’outil Logman.exe ou le composant logiciel enfichable MMC Perfmon. msc pour générer les fichiers journaux que vous ajoutez à ce regroupement. Pour Perfmon. msc, les journaux de compteur se trouvent sous **journaux et alertes de performance**. Pour plus d’informations sur l’utilisation de Logman.exe ou Perfmon. msc, recherchez logman ou à l’aide de performances, respectivement, dans le **Centre d’aide et de support**.

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
</dt> </dl>

 

 





