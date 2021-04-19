---
description: 'En savoir plus sur : JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516207"
---
# <a name="jet_snp"></a>JET_SNP


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_snp"></a>JET_SNP

Le **JET_SNP** groupe de constantes décrit le type de l’opération pour laquelle des informations de progression doivent être obtenues. Ces constantes sont utilisées comme paramètre *SNP* de la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_snpRepair<br />
2</p></td>
<td><p>Le rappel est destiné à une opération de réparation.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpCompact<br />
4</p></td>
<td><p>Le rappel est destiné à la défragmentation de la base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpRestore<br />
8</p></td>
<td><p>Le rappel est destiné à une opération de restauration.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpBackup<br />
9</p></td>
<td><p>Le rappel est destiné à une opération de sauvegarde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgrade<br />
10</p></td>
<td><p>Non pris en charge.</p>
<p><strong>Windows 2000 :</strong>  Le rappel est destiné à l’opération de mise à niveau du format de base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpScrub<br />
11</p></td>
<td><p>Le rappel est destiné à une opération de mise à zéro de base de données (c’est-à-dire de nettoyage).</p>
<p><strong>Serveur Windows server 2003 et windows 2000 :</strong>  Non pris en charge.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgradeRecordFormat<br />
12</p></td>
<td><p>Le rappel est destiné au processus de mise à niveau du format d’enregistrement de toutes les pages de la base de données.</p>
<p><strong>Serveur Windows server 2003 et windows 2000 :</strong>  Non pris en charge.</p></td>
</tr>
</tbody>
</table>


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

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
