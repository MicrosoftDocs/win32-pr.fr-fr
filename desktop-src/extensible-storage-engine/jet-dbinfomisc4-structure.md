---
description: 'En savoir plus sur : structure JET_DBINFOMISC4'
title: Structure JET_DBINFOMISC4
TOCTitle: JET_DBINFOMISC4 Structure
ms:assetid: 63f446bc-98b7-4a60-9575-d6b4757fb0fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269269(v=EXCHG.10)
ms:contentKeyID: 32765571
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
ms.openlocfilehash: d52697bfc67b6eafa69c3d284be087527ca73275a03f5d9b98e6b88cb2de6bd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017193"
---
# <a name="jet_dbinfomisc4-structure"></a>Structure JET_DBINFOMISC4


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_dbinfomisc4-structure"></a>Structure JET_DBINFOMISC4

La structure **JET_DBINFOMISC4** contient diverses informations sur une base de données. Il s’agit des informations contenues dans l’en-tête de base de données.

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
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
      JET_BKINFO bkinfoCopyPrev;
      JET_BKINFO bkinfoDiffPrev;
    } JET_DBINFOMISC4;
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
<td><p>0x620, A</p></td>
<td><p>Base de code fusionné (3/26/2003).</p></td>
</tr>
<tr class="even">
<td><p>0x620, B</p></td>
<td><p>Nouveau format de somme de contrôle (1/08/2004).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, C</p></td>
<td><p>Augmentation de la longueur maximale de la clé à 1000/2000 octets pour les pages de 4/8 Ko (1/15/2004).</p></td>
</tr>
<tr class="even">
<td><p>0x620, D</p></td>
<td><p>Indicateurs d’espace de catalogue, space_header. v2 (7/15/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, E</p></td>
<td><p>Ajoutez un nouveau format de nœud/extension au gestionnaire d’espace, utilisez-le pour les pools d’espace réservés (8/9/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, F</p></td>
<td><p>Compression pour les valeurs longues intrinsèques (10/30/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 10</p></td>
<td><p>Compression pour les valeurs Long séparées (12/05/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 11</p></td>
<td><p>Nouvelle taille de segment VL pour les pages de grande taille (12/29/2007).</p></td>
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

**genMinRequired**

Représente la génération de journal minimale requise pour relire les journaux. Elle est généralement utilisée comme génération de point de contrôle.

**genMaxRequired**

Représente la génération de journal maximale requise pour relire les journaux.

**logtimeGenMaxCreate**

Représente la date et l’heure de création du fichier journal genMax.

**ulRepairCount**

Nombre de fois où une réparation a été appelée sur cette base de données.

**logtimeRepair**

Représente la date et l’heure de la dernière réparation effectuée.

**ulRepairCountOld**

Nombre de fois où la réparation a été exécutée sur cette base de données avant la dernière défragmentation.

**ulECCFixSuccess**

Nombre de fois qu’une erreur d’un bit a été résolue et a généré une bonne page.

**logtimeECCFixSuccess**

Représente la date et l’heure auxquelles la dernière erreur de bit a été résolue et a donné lieu à une bonne page.

**ulECCFixSuccessOld**

Représente le nombre de fois qu’une erreur de bit a été résolue et a donné lieu à une bonne page avant la dernière réparation.

**ulECCFixFail**

Nombre de fois qu’une erreur de bit a été résolue et a entraîné une mauvaise page.

**logtimeECCFixFail**

Représente la date et l’heure auxquelles la dernière erreur de bit a été résolue et a entraîné une page incorrecte.

**ulECCFixFailOld**

Nombre de fois qu’une erreur de bit a été résolue et a entraîné une mauvaise page avant la dernière réparation.

**ulBadChecksum**

Nombre de fois qu’une erreur ECC/checksum non corrigeable a été détectée.

**logtimeBadChecksum**

Représente la date et l’heure de la dernière erreur ECC/checksum non corrigeable.

**ulBadChecksumOld**

Nombre de fois qu’une erreur ECC/checksum non réparable a été détectée avant la dernière réparation.

**genCommitted**

Nombre maximal de générations de journaux validées dans la base de données. En général, génération de journal en cours.

**bkinfoCopyPrev**

Dernière sauvegarde de copie réussie.

**bkinfoDiffPrev**

Dernière sauvegarde différentielle réussie. Cette valeur est réinitialisée lorsque bkinfoFullPrev est défini.

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
