---
description: Avant de commencer à développer une application de services HTTP Microsoft Windows (WinHTTP), vous devez d’abord déterminer s’il faut utiliser l’API C/C++ ou l’interface COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Choix d’une interface WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544902"
---
# <a name="choosing-a-winhttp-interface"></a>Choix d’une interface WinHTTP

Avant de commencer à développer une application de services HTTP Microsoft Windows (WinHTTP), vous devez d’abord déterminer s’il faut utiliser l’API C/C++ ou l’interface COM. Le tableau suivant récapitule les avantages et les inconvénients associés à chacune de ces approches.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>API C/C++</th>
<th>Interface COM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Avantages</td>
<td><ul>
<li>Les réponses peuvent être traitées par segments, ce qui est plus efficace.</li>
<li>Les opérations de publication peuvent également être traitées par segments, accélérant ainsi le temps de traitement.</li>
<li>Prise en charge d’AutoProxy.</li>
<li>Accès à l’ensemble complet des fonctionnalités de WinHTTP.</li>
<li>Les données binaires peuvent être facilement gérées.</li>
</ul></td>
<td><ul>
<li>La création d’une application est simple et requiert moins de lignes de code que l’API C/C++.</li>
<li>L’interface peut être utilisée par les langages de script.</li>
</ul></td>
</tr>
<tr class="even">
<td>Inconvénients</td>
<td><ul>
<li>Le traitement est plus complexe.</li>
<li>L’API C/C++ requiert davantage d’étapes que l’interface COM pour effectuer les mêmes actions.</li>
<li>La configuration d’une demande nécessite davantage de code.</li>
</ul></td>
<td><ul>
<li>L’interface COM ne permet pas d’accéder à l’ensemble complet des fonctionnalités de WinHTTP.</li>
<li>Il est difficile de gérer les types de données binaires dans certains langages de script, tels que VBScript et JScript.</li>
<li>L’interface COM ne prend pas en charge le proxy AutoProxy.</li>
<li>Les applications doivent utiliser le modèle de APARTMENT_THREADED COM.</li>
<li>Avant qu’une réponse puisse commencer à être traitée, toute la réponse doit d’abord être reçue et mise en mémoire tampon.</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



