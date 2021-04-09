---
description: 'En savoir plus sur : fonction JetInit2'
title: Fonction JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103954036"
---
# <a name="jetinit2-function"></a>Fonction JetInit2


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetinit2-function"></a>Fonction JetInit2

La fonction **JetInit2** met le moteur de base de données dans un État où il peut prendre en charge l’utilisation des fichiers de base de données par l’application. Le moteur doit déjà être correctement configuré pour l’initialisation à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md). La récupération après incident de la base de données s’effectue automatiquement dans le cadre du processus d’initialisation.

**Windows XP :**  **JetInit2** est introduit dans Windows XP.

Cette fonction est obsolète. Utilisez [JetInit3](./jetinit3-function.md) à la place.

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Paramètres

*pinstance*

Instance à utiliser pour cet appel.

Pour Windows 2000, ce paramètre est ignoré et doit toujours avoir la valeur NULL.

Pour Windows XP et versions ultérieures, l’utilisation de ce paramètre dépend du mode de fonctionnement du moteur. Si le moteur fonctionne en mode hérité (mode de compatibilité de Windows 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la valeur NULL ou il peut être défini sur une mémoire tampon de sortie valide contenant la valeur NULL ou JET_instanceNil qui retourne le handle d’instance global créé comme un effet secondaire de l’initialisation. Ce descripteur d’instance peut ensuite être passé à toute autre API qui prend une instance. Si le moteur fonctionne en mode multi-instance, ce paramètre doit être défini sur une mémoire tampon d’entrée valide qui contient le handle d’instance retourné par le [JetCreateInstance](./jetcreateinstance-function.md) en cours d’initialisation.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.

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
<td><p>JET_bitReplayReplicatedLogFiles</p></td>
<td><p>Réservé pour un usage futur.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Réservé pour un usage futur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Cette option permet à l’utilisateur d’exécuter la récupération sur un ensemble de fichiers journaux, sans que toutes les bases de données présentes, soient attachées à un point du jeu de journaux.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Effectuer la récupération, mais s’arrêter à la phase de restauration. Cela permet la copie et l’application des journaux de transactions supplémentaires.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>En cas de récupération logicielle réussie, tronquez les fichiers journaux.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>L’entrée de mappage de base de données est manquante par défaut au même emplacement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Ignorer les journaux perdus à la fin du flux de journal.</p>
<p><strong>Windows 7 : JET_bitReplayIgnoreLostLogs</strong> est introduite dans Windows 7.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


#### <a name="remarks"></a>Notes

Une instance doit être initialisée avec un appel à **JetInit2** avant de pouvoir être utilisée par une autre chose que [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de [JetInit](./jetinit-function.md). Une instance est l’unité de récupérabilité pour le moteur de base de données. Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données. Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions.

Si la récupération s’exécute sur un ensemble de journaux, pour lesquels toutes les bases de données ne sont pas présentes (ce qui renvoie l’erreur JET_errAttachedDatabaseMismatch dans des conditions normales), et que le client souhaite que la récupération se poursuive malgré les bases de données manquantes, le JET_ bitReplayIgnoreMissingDB est utilisé pour poursuivre la récupération des bases de données disponibles.

Pour plus d’informations, consultez la section Notes dans [JetInit](./jetinit-function.md) .

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[Fichiers ESE (Extensible Storage Engine)](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres de ressource](./resource-parameters.md)
