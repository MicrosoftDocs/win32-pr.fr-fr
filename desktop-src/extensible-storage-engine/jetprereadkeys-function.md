---
description: 'En savoir plus sur : fonction JetPrereadKeys'
title: JetPrereadKeys fonction)
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24547a7970270943546e5fcfbc026ff24be144b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126850707"
---
# <a name="jetprereadkeys-function"></a>JetPrereadKeys fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetprereadkeys-function"></a>JetPrereadKeys fonction)

La fonction **JetPrereadKeys** lit les valeurs clés pour améliorer les performances du nettoyage de la Banque des versions.

**Windows 7 :** la fonction PrereadKeys est introduite dans Windows 7.

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Curseur à utiliser pour cet appel.

*rgpvKeys*

Tableau de pointeurs vers les clés. Les clés peuvent être créées avec [JetMakeKey](./jetmakekey-function.md) ou récupérées avec [JetGetBookmark](./jetgetbookmark-function.md). Les clés doivent être triées dans l’ordre croissant ou décroissant, selon le Grbit passé. Les clés peuvent être triées avec memcmp.

*rgcbKeys*

Tableau de longueurs de clé. rgpvKeys \[ n \] doit pointer vers une clé de longueur rgcbKeys \[ n\]

*ckeys*

Nombre de clés. rgpvKeys et rgcbKeys doivent tous pointer vers un tableau avec au moins éléments ckeys.

*pckeysPreread*

Retourne le nombre de clés pour lesquelles des prélectures ont été émises. Ce paramètre peut être NULL.

*grbit*

Il doit s’agir d’JET_bitPrereadForward ou JET_bitPrereadBackward. Si Grbit est JET_bitPrereadForward, les clés doivent être triées dans l’ordre croissant. Si Grbit est JET_bitPrereadBackward, les clés doivent être triées dans l’ordre décroissant.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

Diverses erreurs d’e/s peuvent être retournées avec les erreurs d’utilisation de l’API suivantes :


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errInvalidGrbit</p> | <p>Grbit n’était ni JET_bitPrereadForward ni JET_bitPrereadBackward.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Une taille de clé incorrecte a été passée. Les clés ne peuvent pas être égales à 0 ni supérieure à la longueur de clé maximale pour la table.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un paramètre non valide a été passé. Cela peut être dû à une valeur null pour un paramètre obligatoire ou peut indiquer que le tableau de clés n’est pas correctement trié.</p> | 



**JetPrereadKeys** parcourt les pages internes de l’arbre b (b-Tree) pour déterminer quelles pages de feuille contiennent les clés spécifiées par RgpvKeys/rgcbKeys. La liste des pages feuille est triée, puis les prélectures sont émises pour les plages de pages. Le nombre de pages pouvant être prélues est limité. il est donc possible que toutes les clés ne soient pas prélues. Dans ce cas, le nombre de clés réellement prélues est retourné dans pckeysPreread.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows 7.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008 R2.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 

