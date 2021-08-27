---
description: 'En savoir plus sur : fonction JetIdle'
title: JetIdle fonction)
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: babe3077c01b6b2a9c1f2f55b48921582d6343bd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984542"
---
# <a name="jetidle-function"></a>JetIdle fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetidle-function"></a>JetIdle fonction)

La fonction **JetIdle** est défunte et ne doit être utilisée qu’à des fins de test. **JetIdle** peut être utilisé pour effectuer des tâches de nettoyage inactives ou vérifier l’état de la Banque des versions dans le moteur ESE.

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session qui sera utilisée pour cet appel.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro, un ou plusieurs des bits suivants :


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitIdleCompact</p> | <p>Déclenche le nettoyage de la Banque des versions.</p> | 
| <p>JET_bitIdleFlushBuffers</p> | <p>Réservé pour un usage futur. Si cet indicateur est spécifié, l’API retourne JET_errInvalidgrbit.</p> | 
| <p>JET_bitIdleStatus</p> | <p>Retourne JET_wrnIdleFull si la Banque des versions est supérieure à la moitié complète.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un paramètre <em>Grbit</em> fourni à l’API n’est pas valide.</p> | 



Si cette fonction a la valeur, l’opération appropriée est déclenchée, ou un code d’erreur indiquant la totalité de la Banque des versions dépend du *Grbit* fourni.

Si cette fonction échoue, l’opération demandée ne s’est pas terminée correctement.

#### <a name="remarks"></a>Remarques

La Banque des versions gère le mécanisme d’isolation d’instantané de ESE. Si la Banque des versions est plus de moitié complète, le programme peut fermer des transactions de longue durée. Si une transaction de longue durée épuise la Banque des versions, il cesse d’autoriser les opérations d’écriture dans la base de données.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
