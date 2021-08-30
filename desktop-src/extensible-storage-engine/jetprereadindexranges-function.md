---
description: 'En savoir plus sur : fonction JetPrereadIndexRanges'
title: JetPrereadIndexRanges fonction)
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fba09bc0bfb806a8785ea1c009f2bfbb7eb5105c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478995"
---
# <a name="jetprereadindexranges-function"></a>JetPrereadIndexRanges fonction)


_**S’applique à :** Windows | Windows Serveurs_

La fonction **JetPrereadIndexRanges** prélit les index pour améliorer les performances.

la fonction **JetPrereadIndexRanges** a été introduite dans le système d’exploitation Windows 8.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table avec laquelle émettre les prélectures.

*rgIndexRanges*

Plages de clés à prélire.

*cIndexRanges*

Nombre de plages de clés à prélire, déterminé par le nombre d’éléments dans *rgIndexRanges*.

*pcRangesPreread*

Nombre de plages de clés réellement prélues.

*rgcolumnidPreread*

Liste des ID de colonne pour les colonnes de valeur longue à prélire. Par défaut, seul l’enregistrement sur la page est prélecture. Si les colonnes de valeur longue page non paginée doivent être prélues, leurs ID de colonne doivent être transmis via ce paramètre.

*ccolumnidPreread*

Nombre d’ID de colonne pour les colonnes de valeurs longues à prélire, déterminé par le nombre d’éléments dans *rgcolumnidPreread*.

*grbit*

Groupe de bits qui spécifie zéro, une ou plusieurs des valeurs de direction de prélecture énumérées dans le tableau suivant.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>Transférer</p> | <p>Lecture anticipée.</p> | 
| <p>Vers l'arrière</p> | <p>Prélire en arrière.</p> | 
| <p>FirstPageOnly</p> | <p>Prélire uniquement la première page d’une colonne longue.</p> | 
| <p>NormalizedKey</p> | <p>Clé/signet normalisé fourni à la place de la valeur de colonne.</p> | 



### <a name="return-value"></a>Valeur de retour

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. pour plus d’informations sur les erreurs ESE (extensible Stockage engine) possibles, consultez [erreurs du moteur de Stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 



#### <a name="remarks"></a>Remarques

Si les enregistrements avec les plages de clés spécifiées ne se trouvent pas dans le cache des tampons, vous devez démarrer des lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>Requiert Windows 8.</p> | | <p><strong>Serveur</strong></p> | <p>Requiert Windows Server 2012.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)
