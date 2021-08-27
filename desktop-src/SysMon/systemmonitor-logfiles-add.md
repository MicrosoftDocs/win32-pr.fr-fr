---
title: LogFiles. Add, méthode
description: Ajoute un fichier journal à la collection.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Ajouter la méthode SysMon
- Add, méthode SysMon, classe LogFiles
- LogFiles, classe SysMon, méthode Add
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af01c5c7a1bbe16826457d7e1f8700df01876827c522a36db41f6c3843101d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882334"
---
# <a name="logfilesadd-method"></a>LogFiles. Add, méthode

Ajoute un fichier journal à la collection.

## <a name="syntax"></a>Syntaxe


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du chemin* \[ dans\]
</dt> <dd>

Chemin d’accès au fichier journal. Vous pouvez spécifier le chemin d’accès en tant que chemin d’accès absolu, relatif ou UNC. L’extension de nom de fichier journal doit être .csv,. TSV ou. BLG.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous devez utiliser l’outil Logman.exe ou le composant logiciel enfichable MMC Perfmon. msc pour générer les fichiers journaux que vous ajoutez à ce regroupement. Pour Perfmon. msc, les journaux de compteur se trouvent sous **journaux et alertes de performance**. Pour plus d’informations sur l’utilisation de Logman.exe ou Perfmon. msc, recherchez logman ou à l’aide de performances, respectivement, dans le **Centre d’aide et de support**.

**avant Windows Vista :** Vous ne pouvez pas ajouter de fichiers journaux à la [**collection de fichiers journaux**](systemmonitor-logfiles.md) si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Tout d’abord, définissez **systemmonitor. DataSourceType** sur **DataSourceTypeConstants.sysmonNullDataSource**, ajoutez vos fichiers journaux et compteurs, puis définissez **systemmonitor. DataSourceType** sur **DataSourceTypeConstants.sysmonLogFiles**.

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

 

 





