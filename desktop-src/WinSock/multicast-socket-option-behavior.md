---
description: Cette page décrit le comportement des options de socket de multidiffusion en fonction des différents États des paramètres d’option de Socket.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportement des options de socket de multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460b13fb710e86ef81fb64b48b697f7e73ccf392
ms.sourcegitcommit: 9942a888f172981e276def0c6b84fb0266fcb02d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2021
ms.locfileid: "123399765"
---
# <a name="multicast-socket-option-behavior"></a>Comportement des options de socket de multidiffusion

Cette page décrit le comportement des options de socket de multidiffusion en fonction des différents États des paramètres d’option de Socket.

Par exemple, cette page décrit le comportement lorsque l' \_ option de \_ Socket d’appartenance source d’ajout d’adresses IP \_ est définie sur un socket pour lequel l’option d’appartenance à une source d’ajout d’adresses IP \_ \_ \_ a déjà été définie avec la paire groupe/source spécifiée sur la même interface réseau. Il est autorisé à appeler IP \_ Add \_ source \_ membership sur le même groupe sur une autre interface réseau.

cette page vous aide à concevoir et à dépanner correctement les applications de multidiffusion Windows sockets. 

<table>
<thead>
<tr class="header">
<th>Option de socket initiale</th>
<th>Option de socket suivante en conflit</th>
<th>Erreur retournée</th>
<th>Remarques</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">IP_ADD_MEMBERSHIP<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>N’appelez pas IP_ADD_MEMBERSHIP avec le même groupe plusieurs fois sur la même interface réseau.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>N’appelez pas IP_ADD_SOURCE_MEMBERSHIP avec le même groupe précédemment appelé avec IP_ADD_MEMBERSHIP sur la même interface réseau.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Utilisez à la place IP_BLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Retourne une erreur lors de la tentative de déblocage d’une paire groupe/source qui n’a pas été bloquée précédemment sur la même interface réseau.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Tout appel ultérieur sur la même paire groupe/groupe/source</td>
<td>WSAEINVAL</td>
<td>La création d’appels d’option de socket sur une paire groupe ou groupe/source qui n’est pas actuellement dans la liste d’inclusion (en raison de la suppression de l’appartenance, ou autre) entraîne une erreur.</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>N’appelez pas IP_ADD_MEMBERSHIP avec le même groupe précédemment appelé avec IP_ADD_SOURCE_MEMBERSHIP sur la même interface réseau.</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>N’appelez pas IP_ADD_SOURCE_MEMBERSHIP avec la même paire groupe/source précédemment appelée avec IP_ADD_SOURCE_MEMBERSHIP sur la même interface réseau.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Retourne une erreur lors de la tentative de déblocage d’une paire groupe/source qui n’a pas été bloquée précédemment sur la même interface réseau.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Retourne une erreur lors de la tentative de déblocage d’une paire groupe/source qui n’a pas été bloquée précédemment sur la même interface réseau.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Retourne une erreur lors de la tentative de suppression d’une paire groupe/source qui ne figure pas dans la liste d’inclusion sur la même interface réseau.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Retourne une erreur lors de la tentative de blocage d’une paire groupe/source déjà bloquée sur la même interface réseau.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Utilisez à la place IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Utilisez à la place IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Retourne une erreur lors de la tentative de déblocage d’une paire groupe/source qui n’est pas dans la liste bloquée sur la même interface réseau.</td>
</tr>
</tbody>
</table>



 

 

 



