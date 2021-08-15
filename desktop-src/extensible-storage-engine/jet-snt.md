---
description: 'En savoir plus sur : JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: ad04730c52bce38e462c2521dc7c34872bfcb69c3337ac6af18d09d865b9cfd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252513"
---
# <a name="jet_snt"></a>JET_SNT


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_snt"></a>JET_SNT

Le [JET_SNT]() groupe de constantes décrit les points de la progression d’une opération sur laquelle les informations sont demandées dans un appel à la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .

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
<td><p>JET_sntBegin<br />
5</p></td>
<td><p>Début d’une opération</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRequirements<br />
7</p></td>
<td><p>Non pris en charge.</p>
<p><strong>Windows serveur 2000 :</strong>  L’opération est démarrée. Dans ce cas, le dernier paramètre de la fonction de rappel doit être un pointeur valide vers une structure de <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> qui indique le nombre total d’unités à exécuter.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntProgress<br />
0</p></td>
<td><p>Nombre d’unités terminées et nombre d’unités encore à effectuer. Ces informations sont retournées dans les membres d’une structure <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_sntComplete<br />
6</p></td>
<td><p>Achèvement d’une opération.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntFail<br />
3</p></td>
<td><p>L’échec d’une opération.</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRecoveryStep<br />
8</p></td>
<td><p>Contrôle de récupération d’une opération.</p>
<div class="alert">

> [!NOTE]
> <P>cette valeur ne s’applique pas aux versions du système d’exploitation Windows à partir de Windows 8.</P>


</div></td>
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
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
