---
description: 'En savoir plus sur : méthode API. RetrieveColumn'
title: API. RetrieveColumn, méthode
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 3bcb5effcfc59e155007fbd9e1733d95db058970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758979"
---
# <a name="apiretrievecolumn-method"></a>API. RetrieveColumn, méthode

Inclure les membres protégés  
Inclure les membres hérités  

## <a name="overload-list"></a>Liste de surcharge

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur. Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur. Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif. En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
