---
description: 'En savoir plus sur : fonction JetGetErrorInfoW'
title: JetGetErrorInfoW fonction)
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 867d96561459d009be8464f431307bfa373e8782
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983422"
---
# <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW fonction)

BAS_ fonction **JetGetErrorInfoW** du moteur de base de données.

remarque : cette documentation est basée sur une version préliminaire du moteur de Stockage Extensible. Ces informations sont susceptibles d’être modifiées.

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>Paramètres

*pvContext*

Contexte ou valeur d’erreur pour lequel les informations d’erreur étendues sont nécessaires. La valeur passée dépend de la valeur du paramètre *InfoLevel* .

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations. Le type de la mémoire tampon dépend de la valeur du paramètre *InfoLevel* . L’appelant doit être configuré pour aligner la mémoire tampon de manière appropriée.

*cbMax*

Taille maximale de la structure *pvResult* qui est passée.

*InfoLevel*

Le type d’informations qui sera récupéré pour les informations d’erreur/contexte est spécifié par le paramètre *pvContext* . Le format des données stockées dans *pvResult* dépend de *InfoLevel*.

Le tableau suivant répertorie les valeurs possibles pour ce paramètre.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_ErrorInfoSpecificErr</p> | <p><em>pvContext</em> est interprété comme un <a href="gg269297(v=exchg.10).md">JET_ERR</a>code/Error, <em>pvResult</em> est interprété comme un <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>et les champs de la structure <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> sont remplis de manière appropriée.</p> | 



*grbit*

Réservé.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./extensible-storage-engine-error-codes.md) avec l’un des codes de retour énumérés dans le tableau suivant. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contient une valeur inattendue ou contient une valeur qui n’a pas de sens lorsqu’elle est associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetGetErrorInfo</strong> dans les cas suivants :</p><ul><li><p>La valeur du paramètre <em>InfoLevel</em> spécifiée n’est pas valide.</p></li><li><p>La valeur <em>Grbit</em> spécifiée n’est pas valide.</p></li><li><p>La valeur <em>cbMax</em> de la mémoire tampon du paramètre <em>pvResult</em> spécifiée est inférieure à la taille requise pour la sortie de ce paramètre <em>InfoLevel</em> .</p></li><li><p>Pour <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, la valeur <a href="gg294092(v=exchg.10).md">JET_ERR</a> passée est inconnue pour le moteur.</p></li></ul> | 
| <p>JET_errDisabledFunctionality</p> | <p>Si cette référence de Windows ne prend pas en charge cette fonction, cette erreur est retournée.</p> | 



En cas de réussite, la mémoire tampon de sortie qui est appropriée pour le contexte/la valeur de l’erreur demandée sera définie sur les informations d’erreur étendues demandées.

En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.

### <a name="remarks"></a>Remarques

La fonction [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) et [JET_ERRCAT](./jet-errcat.md) groupe de constantes contiennent la documentation sur les informations d’erreur étendues retournées pour *InfoLevel* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Requiert Windows 8.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows 8 Server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Remarque : seul le <strong>JetGetErrorInfoW</strong> (Unicode) est implémenté. Cette API n’a pas de version (ANSI).</p> | 

