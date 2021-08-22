---
title: SystemMonitor. Relog, méthode
description: Rejournalise les données de compteur dans un nouveau fichier. Vous pouvez également utiliser cette méthode pour spécifier un nouveau type de fichier et réduire le nombre d’échantillons contenus dans le fichier journal.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Relog, méthode SysMon
- Relog, méthode SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode relog
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73025a352ba3ec2e9ed113c59a7e04f98084495da834f83bf052c697833dd13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881726"
---
# <a name="systemmonitorrelog-method"></a>SystemMonitor. Relog, méthode

Rejournalise les données de compteur dans un nouveau fichier. Vous pouvez également utiliser cette méthode pour spécifier un nouveau type de fichier et réduire le nombre d’échantillons contenus dans le fichier journal.

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du fichier* \[ dans\]
</dt> <dd>

Chemin d’accès du fichier journal. Vous pouvez spécifier le chemin d’accès en tant que chemin d’accès absolu, relatif ou UNC. L’extension de nom de fichier journal doit être. BLG,. TSV ou .csv. Si un dossier du chemin d’accès n’existe pas, SYSMON le crée. Si le fichier existe, le fichier est remplacé. SYSMON applique les listes de contrôle d’accès par défaut à partir du répertoire parent.

</dd> <dt>

*filetype* \[ dans\]
</dt> <dd>

Format des données de compteur enregistrées dans le fichier journal. Vous pouvez spécifier [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysMonFileCsv** ou **SysmonFileType.sysmonFileTsv**.

</dd> <dt>

*filtre* \[ dans\]
</dt> <dd>

Nombre d’échantillons des anciens fichiers journaux à enregistrer dans le nouveau fichier journal. Spécifiez 1 pour enregistrer chaque échantillon des anciens fichiers dans les nouveaux fichiers. Spécifiez 2 pour enregistrer un des deux échantillons de l’ancien fichier. Spécifiez 3 pour enregistrer un des trois échantillons de l’ancien fichier. Et ainsi de suite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode utilise les fichiers journaux contenus dans la collection [**systemmonitor. LogFiles**](systemmonitor-logfiles.md) pour reconsigner les données de compteur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. SaveAs**](systemmonitor-saveas.md)
</dt> </dl>

 

 





