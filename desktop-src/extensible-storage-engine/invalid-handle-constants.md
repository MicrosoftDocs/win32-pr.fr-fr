---
description: 'En savoir plus sur : constantes de handle non valides'
title: Constantes de handle non valides
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035140"
---
# <a name="invalid-handle-constants"></a>Constantes de handle non valides


_**S’applique à :** Windows | Serveur Windows_

## <a name="invalid-handle-constants"></a>Constantes de handle non valides

Les constantes suivantes indiquent des handles non valides pour différents aspects de ESE.

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
<td><p>JET_instanceNil<br />
(~ (JET_INSTANCE) 0)</p></td>
<td><p>Handle non valide pour une instance de base de données.<br />
<strong>Windows XP :</strong> Introduite dans Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_sesidNil<br />
(~ (JET_SESID) 0)</p></td>
<td><p>Handle non valide pour un ID de session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_tableidNil<br />
(~ (JET_TABLEID) 0)</p></td>
<td><p>Handle non valide pour un ID de table.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNil<br />
((JET_GRBIT) 0)</p></td>
<td><p>Handle non valide pour un groupe de bits.</p></td>
</tr>
<tr class="odd">
<td><p>JET_LSNil<br />
(~ (JET_LS) 0)</p></td>
<td><p>Handle non valide pour le stockage local.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbidNil<br />
((JET_DBID) 0xFFFFFFFF)</p></td>
<td><p>Handle non valide pour l’ID de base de données.</p></td>
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

