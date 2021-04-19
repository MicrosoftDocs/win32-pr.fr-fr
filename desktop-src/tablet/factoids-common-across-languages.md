---
description: Un certain nombre de Factoids décrivent les entrées communes à tous les moduleurs de langage et n’ont pas besoin d’avoir des formats différents pour des langues différentes. Le tableau suivant répertorie les Factoids qui sont communs à tous les langages.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids commun dans plusieurs langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530837"
---
# <a name="factoids-common-across-languages"></a>Factoids commun dans plusieurs langues

Un certain nombre de Factoids décrivent les entrées communes à tous les moduleurs de langage et n’ont pas besoin d’avoir des formats différents pour des langues différentes. Le tableau suivant répertorie les Factoids qui sont communs à tous les langages.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Factoid</th>
<th>Définition</th>
<th>Exemples</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Caractères</strong></td>
<td>Définit le décalage pour un chiffre unique. Le module de reconnaissance est biaisé pour retourner uniquement des chiffres quand ce Factoid est défini.<br/></td>
<td>0-9<br/></td>
</tr>
<tr class="even">
<td><strong>E-mail</strong></td>
<td>Définit le décalage pour une adresse de messagerie.<br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><strong>Web</strong></td>
<td>Définit le décalage pour différents formats d’URL.<br/>
<blockquote>
[!Note]<br />
Les paramètres par défaut pour le module de reconnaissance incluent le Factoid <strong>Web</strong> . Pour cette raison, vous ne pouvez pas remarquer une différence importante entre le Factoid <strong>Web</strong> et le paramètre par défaut. Toutefois, le Factoid <strong>Web</strong> permet d’éliminer les espaces entre les mots d’une URL.
</blockquote>
<br/></td>
<td>http : \\ Microsoft.net<br/> https://microsoft.us/<br/> https : \\ www.Microsoft.au \<br/> https://microsoft.com<br/> www.microsoft_world. com<br/> www.microsoft.us \<br/> http : \\www.microsoft.com\myfile.htm<br/> http : \\www.microsoft.com\myfile.html<br/> http : \\ www. Microsoft. com\myfile.asp<br/> http : \\ www.Microsoft.uk<br/> http : \\ www.Microsoft.info<br/> www.microsoft.biz<br/></td>
</tr>
<tr class="even">
<td><strong>Par défaut</strong></td>
<td>Retourne le module de reconnaissance à ses paramètres par défaut.<br/></td>
<td>Le paramètre par défaut pour Factoids pour les langues occidentales comprend le dictionnaire système, le dictionnaire de l’utilisateur, les différents signes de ponctuation et le <strong>Web</strong> et le <strong>numéro</strong> Factoids.<br/> Le paramètre par défaut pour Factoids pour les langues d’Extrême-Orient comprend tous les caractères pris en charge par le module de reconnaissance.<br/></td>
</tr>
<tr class="odd">
<td><strong>Aucun</strong></td>
<td>Désactive tous les Factoids, les dictionnaires et le modèle de langue.<br/></td>
<td>Ce Factoid doit être utilisé uniquement lorsque vous ne voulez pas que le module de reconnaissance utilise des règles grammaticales ou des dictionnaires, y compris le dictionnaire système. Ce Factoid est utile pour l’entrée de chaînes aléatoires, telles que les codes de produit. N’utilisez pas l’indicateur de forçage avec ce Factoid.<br/></td>
</tr>
</tbody>
</table>



 

 

 




