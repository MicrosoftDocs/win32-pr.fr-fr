---
description: 'En savoir plus sur : structure JET_DBINFOMISC3'
title: Structure JET_DBINFOMISC3
TOCTitle: JET_DBINFOMISC3 Structure
ms:assetid: ffb23ac1-21ad-4dc6-98f8-aa4e6ef395ac
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294148(v=EXCHG.10)
ms:contentKeyID: 32765762
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b3f0d56702da29b4ddd0557c7d8f1f18e8addd8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987287"
---
# <a name="jet_dbinfomisc3-structure"></a>Structure JET_DBINFOMISC3


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_dbinfomisc3-structure"></a>Structure JET_DBINFOMISC3

La structure **JET_DBINFOMISC3** contient diverses informations sur une base de données. Il s’agit des informations contenues dans l’en-tête de base de données.

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
    } JET_DBINFOMISC3;
```

### <a name="members"></a>Membres

**ulVersion**

Version native du moteur de base de données qui a créé la base de données. Consultez [JetGetVersion](./jetgetversion-function.md) pour récupérer la version native du moteur de base de données actuel.

**ulUpdate**

Effectue le suivi des mises à jour incrémentielles du format de base de données qui sont à compatibilité descendante.


| <p>ulVersion, ulUpdate =</p> | <p>Signification</p> | 
|------------------------------|----------------|
| <p>0x620, 0</p> | <p>Format bêta du système d’exploitation d’origine (4/22/97).</p> | 
| <p>0x620, 1</p> | <p>Ajoutez des colonnes dans le catalogue pour l’indexation conditionnelle et l’ancienne (5/29/97).</p> | 
| <p>0x620, 2</p> | <p>Ajoutez l’indicateur fLocalizedText dans IDB (6/5/97).</p> | 
| <p>0x620, 3</p> | <p>Ajoutez des SPLIT_BUFFER à des pages racine de l’arborescence d’espace (10/30/97).</p> | 
| <p>0x620, 2</p> | <p>Rétablissez la révision pour que ESE97 reste compatible avec les versions ultérieures (1/28/98).</p> | 
| <p>0x620, 3</p> | <p>Ajoutez de nouvelles colonnes avec balises au catalogue (« CallbackData » et « CallbackDependencies »).</p> | 
| <p>0x620, 4</p> | <p>Prise en charge de SLV : signSLV, fSLVExists dans l’en-tête de base de connaissances (5/5/98).</p> | 
| <p>0x620, 5</p> | <p>Nouvelle arborescence d’espace SLV (5/29/98).</p> | 
| <p>0x620, 6</p> | <p>Table d’espace SLV (10/12/98).</p> | 
| <p>0x620, 7</p> | <p>IDXSEG de 4 octets (12/10/98).</p> | 
| <p>0x620, 8</p> | <p>Nouveau format de colonne de modèle (1/25/99).</p> | 
| <p>0x620, 9</p> | <p>Colonnes de modèle triées (6/24/99).</p> | 
| <p>0x620, A</p> | <p>Base de code fusionné (3/26/2003).</p> | 
| <p>0x620, B</p> | <p>Nouveau format de somme de contrôle (1/08/2004).</p> | 
| <p>0x620, C</p> | <p>Augmentation de la longueur maximale de la clé à 1000/2000 octets pour les pages de 4/8 Ko (1/15/2004).</p> | 
| <p>0x620, D</p> | <p>Indicateurs d’espace de catalogue, space_header. v2 (7/15/2007).</p> | 
| <p>0x620, E</p> | <p>Ajoutez un nouveau format de nœud/extension au gestionnaire d’espace, utilisez-le pour les pools d’espace réservés (8/9/2007).</p> | 
| <p>0x620, F</p> | <p>Compression pour les valeurs longues intrinsèques (10/30/2007).</p> | 
| <p>0x620, 10</p> | <p>Compression pour les valeurs Long séparées (12/05/2007).</p> | 
| <p>0x620, 11</p> | <p>Nouvelle taille de segment VL pour les pages de grande taille (12/29/2007).</p> | 



**signDb**

Signature de la base de données (y compris l’heure de création). Cette structure est de 28 octets.

**dbstate**

Il s’agit de l’état de la base de données.

Les options suivantes sont disponibles pour ce membre.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_dbstateJustCreated<br />1</p> | <p>La base de données vient d’être créée.</p> | 
| <p>JET_dbstateDirtyShutdown<br />2</p> | <p>La base de données nécessite une récupération matérielle ou logicielle pour être utilisable ou déplaçable. L’un ne doit pas essayer de déplacer des bases de données dans cet État.</p> | 
| <p>JET_dbstateCleanShutdown<br />3</p> | <p>La base de données est dans un état propre. La base de données peut être jointe sans aucun fichier journal.</p> | 
| <p>JET_dbstateBeingConverted<br />4</p> | <p>La base de données est en cours de mise à niveau.</p> | 
| <p>JET_dbstateForceDetach<br />5</p> | <p>Internes.</p> | 



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

Représente la génération de journal minimale requise pour relire les journaux. Il s’agit généralement du même que la génération du point de contrôle.

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

Génération de journal actuelle. Cette valeur peut être inférieure à genMaxRequired si JET_paramWaypointLatency est différent de zéro.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
