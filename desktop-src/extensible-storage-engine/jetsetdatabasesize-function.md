---
description: 'En savoir plus sur : fonction JetSetDatabaseSize'
title: JetSetDatabaseSize fonction)
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112035"
---
# <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize fonction)

La fonction **JetSetDatabaseSize** définit la taille d’un fichier de base de données non ouvert.

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Identifie le contexte de session de base de données à utiliser pour l’appel d’API.

*szDatabaseName*

Identifie le nom du fichier de base de données dont la taille doit être modifiée.

*CPG*

Spécifie la taille souhaitée de la base de données, en pages.

*pcpgReal*

Pointeur vers un nombre qui reçoit la taille de la base de données, en pages, après l’appel d’API. Si l’appel d’API a échoué, le contenu de *pcpgReal* n’est pas défini.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Code de retour</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>JET_errDatabaseInconsistent et JET_errDatabaseDirtyShutdown sont la même valeur numérique. La base de données dont la taille doit être ajustée doit être dans un état d’arrêt normal, appelée état cohérent. Une base de données incohérente n’est pas endommagée, mais elle nécessite la relecture des fichiers journaux.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p><em>szDatabaseName</em> ne doit pas être une chaîne vide et non null.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>L’espace libre est insuffisant sur le volume pour effectuer l’opération d’augmentation. <strong>JetSetDatabaseSize</strong> peut également renvoyer de nombreuses erreurs liées aux fichiers, notamment, mais sans s’y limiter :</p>
<ul>
<li><p>JET_errDiskIO</p></li>
<li><p>JET_errFileNotFound</p></li>
<li><p>JET_errInvalidPath</p></li>
<li><p>JET_errFileAccessDenied</p></li>
<li><p>JET_errOutOfFileHandles</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’une des raisons pour lesquelles cette erreur peut être retournée est si <em>CPG</em> ne respecte pas la taille de base de données minimale. La taille de base de données minimale actuelle est de 256 pages.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Les ressources mémoire du système sont insuffisantes.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

Si **JetSetDatabaseSize** est appelé avant d’insérer de grandes quantités de données, le fichier de base de données sera augmenté en une seule opération. Cela permet de réduire la probabilité que le fichier de base de données soit fragmenté au niveau du système de fichiers et de réduire également le nombre de fois où le fichier de base de données doit être augmenté. La croissance du fichier de base de données peut être plus rapide que la croissance à plusieurs reprises.

Seule la croissance du fichier est actuellement prise en charge. Pour réduire un fichier, utilisez la fonctionnalité de défragmentation du programme utilitaire esentutl.exe.

Si la valeur de *CPG* est inférieure à la taille actuelle de la base de données, l’opération sera ignorée. Si la valeur de *CPG* est inférieure à la taille minimale de la base de données (actuellement 256 pages), elle retournera JET_errInvalidParameter.

Pour définir la taille d’une base de données ouverte, consultez [JetGrowDatabase](./jetgrowdatabase-function.md).

La taille du fichier peut ne pas correspondre au nombre de pages retournées dans *pcpgReal*. Il existe deux pages réservées supplémentaires qui peuvent ne pas être comptées dans *pcpgReal*.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetSetDatabaseSizeW</strong> (Unicode) et <strong>JetSetDatabaseSizeA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetGrowDatabase](./jetgrowdatabase-function.md)
