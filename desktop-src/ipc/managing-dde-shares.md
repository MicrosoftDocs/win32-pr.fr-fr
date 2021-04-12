---
description: L’échange de données réseau fournit des fonctions qui vous permettent de supprimer un partage, d’obtenir ou de définir des informations de partage ou d’énumérer des partages.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Gestion des partages DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321357"
---
# <a name="managing-dde-shares"></a>Gestion des partages DDE

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

L’échange de données réseau fournit des fonctions qui vous permettent de supprimer un partage, d’obtenir ou de définir des informations de partage ou d’énumérer des partages.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tâche</th>
<th>Procédure</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Supprimer un partage DDE</td>
<td>Utilisez la fonction <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> .</td>
</tr>
<tr class="even">
<td>Recevoir des informations sur le partage DDE</td>
<td>Utilisez la fonction <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> .</td>
</tr>
<tr class="odd">
<td>Définir les informations de partage DDE</td>
<td>Utilisez la fonction <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> .</td>
</tr>
<tr class="even">
<td>Énumérer les partages DDE</td>
<td>Utilisez la fonction <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> . Vous pouvez également énumérer les partages DDE approuvés à l’aide de la fonction <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>Énumérer les utilisateurs connectés</td>
<td>Utilisez la fonction <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> .</td>
</tr>
<tr class="even">
<td>Modifier le nom de partage DDE</td>
<td>Supprimez l’ancien partage et créez un nouveau partage.
<ol>
<li>Récupérez les informations de partage à l’aide de <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li>
<li>Supprimez le partage à l’aide de <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</li>
<li>Modifiez le membre <strong>lpszShareName</strong> de la structure <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> retournée par <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li>
<li>Transmettez la structure <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modifiée à <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

