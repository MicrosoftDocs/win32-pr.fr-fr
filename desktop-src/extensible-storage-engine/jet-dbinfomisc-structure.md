---
description: 'En savoir plus sur : structure JET_DBINFOMISC'
title: Structure JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c7684fe69cff252d75ea2cceb0872044e8a011b39e88375d6eb576cb1b5360e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486332"
---
# <a name="jet_dbinfomisc-structure"></a>Structure JET_DBINFOMISC


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_dbinfomisc-structure"></a>Structure JET_DBINFOMISC

La structure **JET_DBINFOMISC** contient diverses informations sur une base de données. Il s’agit des informations contenues dans l’en-tête de base de données.

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
    } JET_DBINFOMISC;
```

### <a name="members"></a>Membres

**ulVersion**

Version native du moteur de base de données qui a créé la base de données. Consultez [JetGetVersion](./jetgetversion-function.md) pour récupérer la version native du moteur de base de données actuel.

**ulUpdate**

Effectue le suivi des mises à jour incrémentielles du format de base de données qui sont à compatibilité descendante.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ulVersion, ulUpdate =</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x620, 0</p></td>
<td><p>Format bêta du système d’exploitation d’origine (4/22/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 1</p></td>
<td><p>Ajoutez des colonnes dans le catalogue pour l’indexation conditionnelle et l’ancienne (5/29/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Ajoutez l’indicateur fLocalizedText dans IDB (6/5/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Ajoutez des SPLIT_BUFFER à des pages racine de l’arborescence d’espace (10/30/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Rétablissez la révision pour que ESE97 reste compatible avec les versions ultérieures (1/28/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Ajoutez de nouvelles colonnes avec balises au catalogue ( &quot; CallbackData &quot; et &quot; CallbackDependencies &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 4</p></td>
<td><p>Prise en charge de SLV : signSLV, fSLVExists dans l’en-tête de base de connaissances (5/5/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 5</p></td>
<td><p>Nouvelle arborescence d’espace SLV (5/29/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 6</p></td>
<td><p>Table d’espace SLV (10/12/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 7</p></td>
<td><p>IDXSEG de 4 octets (12/10/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 8</p></td>
<td><p>Nouveau format de colonne de modèle (1/25/99).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 9</p></td>
<td><p>Colonnes de modèle triées (6/24/99).</p></td>
</tr>
<tr class="odd">
<td><p>0x623, 0</p></td>
<td><p>Nouveau gestionnaire d’espace (5/15/99).</p></td>
</tr>
</tbody>
</table>


**signDb**

Signature de la base de données (y compris l’heure de création). Cette structure est de 28 octets.

**dbstate**

Il s’agit de l’état de la base de données.

Les options suivantes sont disponibles pour ce membre.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_dbstateJustCreated<br />
1</p></td>
<td><p>La base de données vient d’être créée.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateDirtyShutdown<br />
2</p></td>
<td><p>La base de données nécessite une récupération matérielle ou logicielle pour être utilisable ou déplaçable. L’un ne doit pas essayer de déplacer des bases de données dans cet État.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateCleanShutdown<br />
3</p></td>
<td><p>La base de données est dans un état propre. La base de données peut être jointe sans aucun fichier journal.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateBeingConverted<br />
4</p></td>
<td><p>La base de données est en cours de mise à niveau.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateForceDetach<br />
5</p></td>
<td><p>Internes.</p></td>
</tr>
</tbody>
</table>


**lgposConsistent**

NULL si la base de données est dans un état modifié. Il s’agit de la position du journal qui a été utilisée lors du dernier enregistrement de la base de données dans un état d’arrêt normal.

**logtimeConsistent**

NULL si la base de données est dans un état modifié. Il s’agit de l’heure à laquelle la base de données a été ramenée dans un état d’arrêt normal.

**logtimeAttach**

Heure à laquelle la base de données a été attachée pour la dernière fois à [JetAttachDatabase](./jetattachdatabase-function.md).

**lgposAttach**

Position du journal qui a été utilisée lors de la dernière connexion de la base de données à [JetAttachDatabase](./jetattachdatabase-function.md).

**logtimeDetach**

Heure à laquelle la base de données a été détachée pour la dernière fois avec [JetDetachDatabase](./jetdetachdatabase-function.md).

**lgposDetach**

Position du journal qui a été utilisée lors du dernier détachement de la base de données avec [JetDetachDatabase](./jetdetachdatabase-function.md).

**signLog**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.

**bkinfoFullPrev**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.

**bkinfoIncPrev**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.

**bkinfoFullCur**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.

**fShadowingDisabled**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.

**fUpgradeDb**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé dans votre code.

**dwMajorVersion**

Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour. Utilisé pour la mise à jour des index.

**dwMinorVersion**

Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour. Utilisé pour la mise à jour des index.

**dwBuildNumber**

Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour. Utilisé pour la mise à jour des index.

**lSPNumber**

Représente les numéros de version de Windows NT lorsque les index de base de données ont été mis à jour. Utilisé pour la mise à jour des index.

**cbPageSize**

Taille de la page de base de données. 0 signifie que la taille de la page est de 4 Ko.

Cette valeur est récupérée uniquement si JET_DbInfoMisc a été passé à [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) ou [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
