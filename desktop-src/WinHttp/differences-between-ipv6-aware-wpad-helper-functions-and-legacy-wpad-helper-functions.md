---
title: IPv6-Aware et fonctions d’assistance WPAD existantes
description: Différences entre les fonctions d’assistance WPAD IPv6-Aware et les fonctions d’assistance WPAD héritées
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6423b9bcb6a609cf21b8399ca03d7da1e0b19450994eb78a66f4c7aaad7d31d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860999"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a>IPv6-Aware et fonctions d’assistance WPAD existantes

Les tableaux suivants expliquent les différences entre les nouvelles fonctions d’assistance WPAD et les fonctions d’assistance WPAD héritées. Les nouvelles fonctions sont marquées d’un astérisque.



<table>
<thead>
<tr class="header">
<th>Fonctions</th>
<th>Entrée</th>
<th>Output</th>
<th>Motif de modification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>dnsResolve</td>
<td>Host</td>
<td>Adresse IPv4</td>
<td rowspan="2">La fonction ex renverra une liste de IPv6/IPv4. Nécessaire, car les adresses IPv6 ou IPv4 peuvent avoir plusieurs adresses monodiffusion pour une seule interface. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>dnsResolveEx*</td>
<td>Host</td>
<td>Liste des adresses IPv6/IPv4</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Fonctions</th>
<th>Entrée</th>
<th>Output</th>
<th>Motif de modification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isResolveable</td>
<td>Hôte IPv4</td>
<td>TRUE/FALSE</td>
<td rowspan="2">La fonction ex retourne la valeur TRUE si un hôte peut résoudre une adresse IPv6 ou IPv4. La fonction héritée retourne la valeur TRUE uniquement si l’hôte est résolu en une adresse IPv4. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>isResolveableEx*</td>
<td>Hôte IPv6/IPv4</td>
<td>TRUE/FALSE</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Fonctions</th>
<th>Entrée</th>
<th>Output</th>
<th>Motif de modification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>myIPAddress</td>
<td>aucun</td>
<td>Adresse IPv4</td>
<td rowspan="2">La fonction ex renverra une liste de IPv6/IPv4. Nécessaire, car les adresses IPv6 ou IPv4 peuvent avoir plusieurs adresses monodiffusion pour une seule interface $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>myIPAddressEx*</td>
<td>aucun</td>
<td>Liste des adresses IPv6/IPv4</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Fonctions</th>
<th>Entrée</th>
<th>Output</th>
<th>Motif de modification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isInNet</td>
<td>Hôte, modèle d’adresse IP séparée par des points, masque d’adresse IP</td>
<td>TRUE/FALSE</td>
<td rowspan="2">Indiquez une version IP agnostique pour déterminer si une adresse IP se trouve dans un sous-réseau donné. En outre, la notation de masque dans IPv4 est dépréciée. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>isInNetEx*</td>
<td>Préfixe IP de l’adresse IP</td>
<td>TRUE/FALSE</td>

</tr>
</tbody>
</table>



 



| Fonctions           | Entrée                       | Output                             | Motif de modification                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| sortIPAddressList\* | Liste des adresses IPv6/IPv4 | Liste triée des adresses IPv6/IPv4 | Il n’existe pas de fonction héritée équivalente, car les fonctions héritées ne retournaient qu’une seule adresse IPv4. par conséquent, il n’était pas nécessaire de trier. |



 



| Fonctions          | Entrée | Output                     | Motif de modification                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| getClientVersion\* | aucun  | Numéro de version du moteur WPAD | Actuellement, cette fonction retourne la version 1,0. Nous avons ajouté cette fonction pour permettre aux administrateurs informatiques de mettre à jour leur WPAD pour qu’ils fonctionnent avec différentes versions du moteur WPAD sans causer de ruptures à leur déploiement existant. |



 

> [!Note]  
> cette fonctionnalité nécessite Windows Internet Explorer 7 ou version ultérieure.

 

 

 



