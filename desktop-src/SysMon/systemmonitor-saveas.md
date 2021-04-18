---
title: SystemMonitor. SaveAs, méthode
description: Enregistre les valeurs de compteur de la vue du graphique dans un fichier journal.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- SaveAs, méthode SysMon
- SaveAs, méthode SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527157"
---
# <a name="systemmonitorsaveas-method"></a>SystemMonitor. SaveAs, méthode

Enregistre les valeurs de compteur de la vue du graphique dans un fichier journal.

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du fichier* \[ dans\]
</dt> <dd>

Chemin d’accès du fichier journal. Vous pouvez spécifier le chemin d’accès en tant que chemin d’accès absolu, relatif ou UNC. L’extension de nom de fichier journal doit être. TSV ou. htm. Si un dossier du chemin d’accès n’existe pas, SYSMON le crée. Si le fichier existe, le fichier est remplacé. SYSMON applique les listes de contrôle d’accès par défaut à partir du répertoire parent.

</dd> <dt>

*filetype* \[ dans\]
</dt> <dd>

Format des données de compteur enregistrées dans le fichier journal. Vous pouvez spécifier [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) ou **SysmonFileType.sysmonFileTsv**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Seules les données de compteur visibles dans la vue du graphique sont enregistrées (pour le nombre réel de points de données enregistrés, consultez [**systemmonitor. DataPointCount**](systemmonitor-datapointcount.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. relog**](systemmonitor-relog.md)
</dt> </dl>

 

 





