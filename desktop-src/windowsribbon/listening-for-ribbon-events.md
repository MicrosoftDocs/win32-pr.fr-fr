---
title: Écoute des événements de ruban
description: l’infrastructure de ruban Windows utilise l’infrastructure Suivi d’v nements pour Windows (ETW) pour permettre aux développeurs d’apprendre comment les utilisateurs interagissent avec le ruban de leur application.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows Ruban, événements
- Ruban, événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9519553a40cd613085949d4650c2689e817f387e47e9ab4380b629464e90d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202969"
---
# <a name="listening-for-ribbon-events"></a>Écoute des événements de ruban

l’infrastructure de ruban Windows utilise l’infrastructure [Suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour permettre aux développeurs d’apprendre comment les utilisateurs interagissent avec le ruban de leur application.

## <a name="introduction"></a>Introduction

Le mécanisme d’événement d’infrastructure de ruban est conçu de telle sorte que l’infrastructure signale les événements de l’interface utilisateur du ruban à l’application afin que vous puissiez surveiller l’activité des utilisateurs, apprendre leurs modèles d’interaction et évaluer les tendances d’utilisation. Ces informations peuvent être utilisées pour affiner l’expérience utilisateur des itérations ultérieures de votre application de ruban.

L’utilisation des événements de l’infrastructure du ruban implique les opérations suivantes :

1.  l’application ruban doit inscrire un écouteur de [Suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour recevoir des notifications d’événements de ruban à partir de l’infrastructure du ruban.
2.  l’infrastructure du ruban déclenche des rappels d’événements de l’interface utilisateur du ruban au moment de l’exécution, si l’application a inscrit un écouteur [de Suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) .

## <a name="supported-events"></a>Événements pris en charge

Les événements exposés aux applications du ruban sont décrits dans le tableau suivant. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Événement</th>
<th>Rapport d’événements</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Onglet activé</td>
<td>ID de commande<br/> Nom de commande<br/> Verbe d’événement<br/></td>
</tr>
<tr class="even">
<td>Onglet contextuel activé</td>
<td>ID de commande<br/> Nom de commande<br/> Verbe d’événement<br/></td>
</tr>
<tr class="odd">
<td>Menu de l’application ouvert</td>
<td>Verbe d’événement<br/></td>
</tr>
<tr class="even">
<td>Menu de l’application fermé</td>
<td>Verbe d’événement<br/></td>
</tr>
<tr class="odd">
<td>Menu (normal ou Galerie ouvert)</td>
<td>ID de commande<br/> Nom de commande<br/> Verbe d’événement<br/>
<blockquote>
[!Note]<br />
Les événements de menu QAT ne sont pas exposés.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Menu (normal ou Galerie fermé)</td>
<td>ID de commande<br/> Nom de commande<br/> Verbe d’événement<br/>
<blockquote>
[!Note]<br />
Les événements de menu QAT ne sont pas exposés.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Commande</td>
<td>ID de commande<br/> Nom de commande<br/> Verbe d’événement<br/> L’un des emplacements d’événements suivants :
<ul>
<li>DERNIER</li>
<li>QUICKACCESSTOOLBAR</li>
<li>APPLICATIONMENU</li>
<li>CONTEXTPOPUP</li>
</ul>
<br/> ID de commande parent<br/> Nom de la commande parente<br/> L’une des méthodes d’appel suivantes :
<ul>
<li>Cliquez sur</li>
<li>KEYTIP</li>
<li>CLAVIER</li>
<li>INTERFACE</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
Les galeries d’éléments et les zones de liste déroulante incluent l’index d’élément sélectionné, mais n’incluent pas les valeurs de chaîne et d’entier. Les jointures n’incluent pas la valeur entière.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Ruban réduit</td>
<td>Verbe d’événement<br/></td>
</tr>
<tr class="odd">
<td>Ruban développé (bouton de développement cliqué ou appui sur épinglé)</td>
<td>Verbe d’événement<br/></td>
</tr>
<tr class="even">
<td>Mode d’application basculé</td>
<td>Verbe d’événement<br/> ID de mode (valeur définie par <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)<br/>
<blockquote>
[!Note]<br />
L’application est chargée de décompresser cet entier pour déterminer les modes qui ont été définis.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Info-bulle affichée</td>
<td>Verbe d’événement<br/> ID de commande parent<br/> Nom de la commande parente<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Guides du développeur de Framework de ruban](windowsribbon-guides-entry.md)
</dt> <dt>

[Déclaration des commandes et des contrôles avec le balisage du ruban](./windowsribbon-schema.md)
</dt> <dt>

[Instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processus de conception du ruban](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

