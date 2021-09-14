---
title: LogFiles, objet (Isysmon.h)
description: Utilisez cette classe pour gérer une collection d’un ou de plusieurs fichiers journaux qui contiennent des données de compteurs de performances. Pour récupérer cet objet, appelez SystemMonitor. LogFiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- LogFiles, objet SysMon
- LogFiles, objet SysMon, Description
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008857"
---
# <a name="logfiles-object"></a>LogFiles (objet)

Utilisez cette classe pour gérer une collection d’un ou de plusieurs fichiers journaux qui contiennent des données de compteurs de performances.

Pour récupérer cet objet, appelez [**systemmonitor. LogFiles**](systemmonitor-logfiles.md).

## <a name="members"></a>Membres

L’objet **LogFiles** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **LogFiles** possède ces méthodes.



| Méthode                                          | Description                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Complémentaires**](systemmonitor-logfiles-add.md)       | Ajoute une instance [**LogFileItem**](logfileitem.md) à la collection.<br/>      |
| [**Remove**](systemmonitor-logfiles-remove.md) | Supprime une instance [**LogFileItem**](logfileitem.md) de la collection.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **LogFiles** possède ces propriétés.



| Propriété                                                 | Description                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Saut**](systemmonitor-logfiles-count.md)<br/> | Récupère le nombre d’instances de [**LogFileItem**](logfileitem.md) dans la collection.<br/>  |
| [**Élément**](systemmonitor-logfiles-item.md)<br/>   | Récupère l’instance [**LogFileItem**](logfileitem.md) spécifiée de la collection.<br/> |



 

## <a name="remarks"></a>Notes

Pour que SYSMON affiche des compteurs de performances à partir d’un fichier journal, définissez [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) sur [**DataSourceTypeConstants. sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Après avoir ajouté les fichiers journaux à la collection, utilisez la collection de [**compteurs**](counters.md) pour spécifier les données de compteurs que vous souhaitez lire à partir des fichiers journaux. Notez que si **systemmonitor. DataSourceType** est défini sur **DataSourceTypeConstants. sysmonLogFiles**, SYSMON rééchantillonnera les fichiers journaux chaque fois que vous ajouterez un fichier journal ou un compteur à leurs collections respectives.

**avant Windows Vista :** Vous ne pouvez pas ajouter de fichiers journaux à la [**collection de fichiers journaux**](systemmonitor-logfiles.md) si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur [**DataSourceTypeConstants. sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Tout d’abord, définissez **systemmonitor. DataSourceType** sur **DataSourceTypeConstants. sysmonNullDataSource**, ajoutez vos fichiers journaux et compteurs, puis affectez à **systemmonitor.** DataSourceType la valeur **DataSourceTypeConstants. sysmonLogFiles**.

Les propriétés [**systemmonitor. LogViewStart**](systemmonitor-logviewstart.md) et [**systemmonitor. LogViewStop**](systemmonitor-logviewstop.md) spécifient la plage de valeurs échantillonnées dans les fichiers journaux du graphique. SYSMON Graph n’affiche qu’une seule vue des données du fichier journal (la vue du graphique ne fait pas défiler l’activité en cours sur l’ordinateur). Si les données échantillonnées dépassent ce qui peut être affiché sur une seule vue de graphique, SYSMON compresse les données échantillonnées (chaque point représenté par un graphique représente la moyenne de plusieurs valeurs échantillonnées) pour s’adapter à toutes les données échantillonnées des fichiers journaux sur le graphique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





