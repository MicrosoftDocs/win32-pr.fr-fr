---
description: 'En savoir plus sur : fonction JetGetInstanceMiscInfo'
title: JetGetInstanceMiscInfo fonction)
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3fe6dbdc997b7c9f72094999aa852036c578dd99
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988501"
---
# <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo fonction)

La fonction **JetGetInstanceMiscInfo** récupère des informations sur l’instance, tandis que l’instance est en ligne.

**Windows vista : JetGetInstanceMiscInfo** est introduit dans Windows vista.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Identifie l’instance de base de données qui sera utilisée pour l’appel d’API.

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations. Le type de la mémoire tampon dépend de *InfoLevel*. L’appelant est chargé d’aligner la mémoire tampon de manière appropriée.

*cbMax*

Taille, en octets, de la mémoire tampon passée dans *pvResult*.

*InfoLevel*

Détermine le type d’informations qui sera récupéré pour l’instance spécifiée par l' *instance*. Le format des données stockées dans *pvResult* dépend de *InfoLevel*.

Les options suivantes peuvent être utilisées avec ce paramètre.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_InstanceMiscInfoLogSignature</p> | <p><em>pvResult</em> est interprété comme une structure <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> de la séquence du journal des transactions associée à cette instance.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>La mémoire tampon est insuffisante.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> non valide ou un <em>InfoLevel</em> non valide a été spécifié.</p> | 



#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
