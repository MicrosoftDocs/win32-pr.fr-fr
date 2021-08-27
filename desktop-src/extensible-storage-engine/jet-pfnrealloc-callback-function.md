---
description: 'En savoir plus sur : fonction de rappel JET_PFNREALLOC'
title: JET_PFNREALLOC fonction de rappel
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: f7427a28752384f6c30e050458e5844dcaedd1a7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989142"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC fonction de rappel


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC fonction de rappel

La fonction JET_PFNREALLOC est un rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) utilisé par [JetEnumerateColumns](./jetenumeratecolumns-function.md) pour allouer de la mémoire pour ses mémoires tampons de sortie.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Paramètres

*pvContext*

Pointeur de contexte donné à [JetEnumerateColumns](./jetenumeratecolumns-function.md). Ce pointeur de contexte peut être utilisé pour communiquer l’état de l’appelant de [JetEnumerateColumns](./jetenumeratecolumns-function.md) à l’implémentation de ce rappel.

*va*

Si la valeur est non NULL, spécifie un pointeur vers un bloc de mémoire précédemment alloué par ce rappel. Si la valeur est NULL, un nouveau bloc de mémoire de la taille demandée sera alloué.

*libéré*

Nouvelle taille du bloc de mémoire en octets. Si ce paramètre a la valeur 0 (zéro) et qu’un bloc de mémoire est spécifié, ce bloc de mémoire est libéré.

### <a name="return-value"></a>Valeur renvoyée

Le système peut générer des codes de réussite ou d’échec à la suite d’un appel à cette fonction. pour plus d’informations sur la façon de retourner ces codes en tant que HRESULTs, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>Succès</p> | <p>Si un bloc de mémoire précédemment alloué a été spécifié et qu’une nouvelle taille de zéro a été spécifiée, ce bloc est libéré et la valeur NULL est retournée. Si un bloc de mémoire précédemment alloué a été spécifié et qu’une nouvelle taille différente de zéro a été spécifiée, le bloc de mémoire réalloué est retourné. Si aucun bloc de mémoire n’a été spécifié, un bloc de mémoire nouvellement alloué de la taille spécifiée est retourné.</p> | 
| <p>Échec</p> | <p>La valeur NULL est retournée. Si un bloc de mémoire précédemment alloué a été fourni, ce bloc restera alloué.</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetEnumerateColumns](./jetenumeratecolumns-function.md)
