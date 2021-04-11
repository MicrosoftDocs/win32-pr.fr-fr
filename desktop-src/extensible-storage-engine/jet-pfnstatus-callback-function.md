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
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203895"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS fonction de rappel


_**S’applique à :** Windows | Serveur Windows_

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

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md). Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

En cas de réussite, l’opération qui a émis le rappel peut se poursuivre normalement. Dans certains cas, le rappel peut retourner un avertissement qui influence cette opération.

En cas d’échec, l’opération qui a émis le rappel peut se poursuivre normalement ou échouer.

### <a name="remarks"></a>Notes

Cette fonction de rappel sera utilisée dans une notification de progression dans laquelle la structure indiquera l’état actuel de la progression. Notez que la fonction de rappel peut être appelée plusieurs fois pour la progression de l’opération.

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[Codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md)  
[Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
