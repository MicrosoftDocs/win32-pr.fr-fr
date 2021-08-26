---
description: 'En savoir plus sur : fonction JetSetCursorFilter'
title: JetSetCursorFilter fonction)
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5958d288e8b101795d1c8e4b4db789ade4b98418
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477515"
---
# <a name="jetsetcursorfilter-function"></a>JetSetCursorFilter fonction)


_**S’applique à :** Windows | Windows Serveurs_

La fonction **JetSetCursorFilter** définit un tableau de filtres simples pour la fonction [JetMove](./jetmove-function.md) .

la fonction **JetSetCursorFilter** a été introduite dans le système d’exploitation Windows 8.

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Curseur à positionner.

*rgFilters*

Filtres d’enregistrements simples.

*cFilters*

Nombre de filtres.

*grbit*

Groupe de bits qui spécifie zéro, une ou plusieurs des options de déplacement énumérées dans le tableau suivant.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>Aucun</p> | <p>Option par défaut.</p> | 



### <a name="return-value"></a>Valeur de retour

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. pour plus d’informations sur les erreurs ESE (extensible Stockage engine) possibles, consultez [erreurs du moteur de Stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 



#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>Requiert Windows 8.</p> | | <p><strong>Serveur</strong></p> | <p>Requiert Windows Server 2012.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JetMove](./jetmove-function.md)  
[JET_ERR](./jet-err.md)
