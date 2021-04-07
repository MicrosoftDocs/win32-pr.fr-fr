---
title: Appel de WDS à partir de la ligne de commande
description: Vous pouvez lancer l’interface utilisateur de Microsoft Windows Desktop Search (WDS) avec un filtre, une banque et une requête spécifiques à partir d’une autre application ou d’une page Web qui utilise l’objet d’assistance du navigateur (BHO) à l’aide de la syntaxe de ligne de commande windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724018"
---
# <a name="calling-wds-from-the-command-line"></a>Appel de WDS à partir de la ligne de commande

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

Vous pouvez lancer l’interface utilisateur de Microsoft Windows Desktop Search (WDS) avec un filtre, une banque et une requête spécifiques à partir d’une autre application ou d’une page Web qui utilise l’objet d’assistance du navigateur (BHO) à l’aide de la syntaxe de ligne de commande windowssearch.exe. Lors de l’appel de WDS à partir de la ligne de commande, aucune information sur les actions ou la sélection de l’utilisateur dans la fenêtre WDS n’est retournée à l’application ou à la page Web appelante.

Le chemin d’installation de WDS est spécifié dans le paramètre de Registre InstallDir sous HKEY_LOCAL_MACHINE \\ Software \\ Microsoft \\ Windows Desktop Search. Le chemin d’accès par défaut dans lequel windowssearch.exe est installé est Program Files \\ Windows Desktop Search.

## <a name="command-line-syntax"></a>Syntaxe de la ligne de commande

La syntaxe suivante s’applique à l’interface de ligne de commande de Windows Desktop Search 2. x.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Options</th>
<th>Paramètre</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/startup</td>

<td>Initialise Windows Desktop Search</td>
</tr>
<tr class="even">
<td>/indexnow</td>

<td>Désactive l’indexation et analyse à nouveau tous les emplacements d’index</td>
</tr>
<tr class="odd">
<td>/showstatus</td>

<td>Affiche la fenêtre État de l’indexation</td>
</tr>
<tr class="even">
<td>/launchsearchwindow ou/URL</td>

<td>Ouvre une fenêtre WDS avec une requête vide</td>
</tr>
<tr class="odd">
<td>/url</td>
<td>recherche : [Store | Show | requête] chaîne de requête</td>
<td>Ouvre une fenêtre WDS avec une requête et un filtre en fonction des paramètres suivants :
<ul>
<li><p>Store : spécifie la source de données à interroger : Files, Outlook, OutlookExpress. S’il n’est pas spécifié, la recherche est effectuée dans tous les magasins. <br/></p>
<blockquote>
[!Note]<br />
Bien que la syntaxe de requête avancée prenne en charge le référencement de Microsoft Outlook comme « OE », le paramètre Store sur la ligne de commande doit être « OutlookExpress ».
</blockquote>
<p><br/></p></li>
<li><p>Show : spécifie le type de résultats perçus à retourner. Pour obtenir la liste complète des types, consultez <a href="-search-2x-wds-perceivedtype.md">types perçus</a> . S’il n’est pas spécifié, tous les types sont retournés. <br/></p>
<blockquote>
[!Note]<br />
Il existe trois différences entre les valeurs de type perçues et les valeurs pour Show. Pour <code>show</code> , utilisez’documents’au lieu de’doc', 'images’au lieu de’pics’et’textdocuments’au lieu de’text'.
</blockquote>
<p><br/></p></li>
<li>requête : spécifie les critères de recherche. Cette valeur prend en charge les paramètres de <a href="-search-2x-wds-aqsreference.md">syntaxe de requête avancée</a> pour affiner les résultats. Le paramètre de requête doit être le dernier paramètre de l’URL.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>Exemple

Par exemple, pour rechercher dans tous les fichiers les images correspondant au critère « papier peint », utilisez la commande suivante :

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Syntaxe de requête avancée](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Types perçus](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Appel de WDS à partir de pages Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





