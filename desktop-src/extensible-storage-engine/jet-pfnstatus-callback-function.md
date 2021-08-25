---
description: 'En savoir plus sur : fonction de rappel JET_PFNSTATUS'
title: JET_PFNSTATUS fonction de rappel
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
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
ms.openlocfilehash: d10de8491379a3e19217bcdb4a28f3546ebc009f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482915"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS fonction de rappel


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS fonction de rappel

La fonction de rappel **JET_PFNSTATUS** reçoit des informations sur la progression des opérations de longue durée, telles que les opérations de défragmentation, de sauvegarde ou de restauration. Pendant ces opérations, le moteur de base de données appelle cette fonction de rappel pour fournir une mise à jour de la progression de l’opération.

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session de type [JET_SESID](./jet-sesid.md) avec laquelle la fonction d’exécution longue a été appelée.

*SNP*

Type d’opération tel que spécifié dans [JET_SNP](./jet-snp.md). Les types d’opérations incluent la réparation, le compactage, la restauration, la sauvegarde, la mise à jour, le nettoyage et la mise à jour du format d’enregistrement.

*SNT*

État d’une opération. Les types d’État incluent début, en cours, achèvement ou échec. L’État est spécifié avec le troisième paramètre de type [JET_SNT](./jet-snt.md).

*va*

Pointeur facultatif vers une structure de type [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Valeur renvoyée

cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des [codes d’erreur du moteur d’Stockage Extensible](./extensible-storage-engine-error-codes.md). pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

En cas de réussite, l’opération qui a émis le rappel peut se poursuivre normalement. Dans certains cas, le rappel peut retourner un avertissement qui influence cette opération.

En cas d’échec, l’opération qui a émis le rappel peut se poursuivre normalement ou échouer.

### <a name="remarks"></a>Remarques

Cette fonction de rappel sera utilisée dans une notification de progression dans laquelle la structure indiquera l’état actuel de la progression. Notez que la fonction de rappel peut être appelée plusieurs fois pour la progression de l’opération.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[codes d’erreur du moteur de Stockage Extensible](./extensible-storage-engine-error-codes.md)  
[erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
