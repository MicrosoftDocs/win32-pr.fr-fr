---
description: l’outil de configuration de trace Microsoft Windows HTTP Services (WinHTTP), WinHttpTraceCfg.exe, est utilisé pour configurer les fonctionnalités de trace à des fins de débogage et de détection de paquets.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, outil de configuration de trace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7747e0b2fe023ab3c2c86d19a722059482aed19062cf2a450b8d0f237a8b3a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562411"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, outil de configuration de trace

l’outil de configuration de trace [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) , WinHttpTraceCfg.exe, est utilisé pour configurer les fonctionnalités de trace à des fins de débogage et de détection de paquets. Il est important de pouvoir surveiller les fonctions WinHTTP et le trafic réseau correspondant. Le débogage des applications qui utilisent des protocoles de transmission chiffrés, tels que les SSL (Secure Sockets Layer) (SSL), empêche la détection de paquets au niveau de la couche de transport réseau et nécessite la possibilité d’intercepter le trafic entre le client et le serveur après qu’il a été déchiffré. Microsoft Windows HTTP Services (WinHTTP) fournit une fonctionnalité de trace qui offre un éventail de fonctionnalités pour intercepter le flux de trafic entre le client et le serveur.

Cette fonctionnalité de trace peut être un outil précieux pour le débogage. Il peut être utilisé, par exemple, pour afficher les paramètres passés à différents appels de fonction, ainsi que pour afficher les données réelles envoyées et reçues par une application WinHTTP.

-   [Utilisation de la fonction de trace](#using-the-trace-facility)
-   [Interprétation des données de trace](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Utilisation de la fonction de trace

WinHTTP obtient des paramètres de contrôle de traçage à partir du Registre. Ces paramètres de contrôle affectent la manière dont WinHTTP produit la sortie de trace et comment cette sortie est mise en forme. Toutes les applications qui utilisent WinHTTP partagent les mêmes paramètres.

un outil de configuration de trace, WinHttpTraceCfg.exe, est disponible en téléchargement sur le site web des [outils du Kit de ressources Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) . L’outil de configuration définit ou récupère les paramètres du registre de la fonctionnalité de trace en fonction des paramètres de ligne de commande spécifiés.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

Le tableau suivant répertorie les paramètres possibles pour l’outil de configuration de.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Paramètre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Affiche les données de syntaxe.<br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Spécifie si la fonctionnalité de trace est activée ou désactivée. <br/> 
<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Paramètre par défaut. Désactive le suivi.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Active le suivi.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-l</td>
<td><p>Spécifie un préfixe pour le fichier journal. Le préfixe peut inclure un chemin d’accès. Le fichier journal est écrit dans le répertoire actif ou dans le répertoire spécifié dans le préfixe et a le format suivant.</p>
<p><<em>préfixe</em> > -< <em>nom de l’application</em> > . <<em>Time</em> > . log</p>
<p>Si aucun préfixe n’est spécifié, une chaîne vide est utilisée. Spécifiez &quot; * &quot; pour supprimer un préfixe existant.</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>Spécifie si la sortie de trace est affichée dans un débogueur ou écrite dans un fichier.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Paramètre par défaut. Écrit dans le fichier journal.</td>
</tr>
<tr class="even">
<td>1</td>
<td>S’affiche dans un débogueur.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-S</td>
<td><p>Spécifie comment le trafic réseau (requêtes et réponses) est affiché.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Affiche uniquement les en-têtes HTTP.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Paramètre par défaut. Affiche le trafic réseau au format American National Standards Institute (ANSI).</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Affiche le trafic réseau au format hexadécimal.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>-T</td>
<td><p>Spécifie si les appels de fonction de niveau supérieur sont enregistrés dans la trace.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Paramètre par défaut. Les appels de fonction ne sont pas enregistrés.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Les appels de fonction de niveau supérieur sont enregistrés.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-M</td>
<td><p>Spécifie la taille maximale, en octets, d’un fichier journal généré par la fonction de suivi. Si cette option est spécifiée sans taille, la valeur minimale est de 65 535 octets. Si un fichier journal atteint la taille maximale, le contenu du fichier est effacé. Les données de trace continuent à être écrites dans le fichier journal.</p></td>
</tr>
</tbody>
</table>



 

L’exécution de l’outil de configuration de trace et la spécification d’aucun paramètre permet de récupérer et d’afficher les paramètres de registre actuels.

> [!Note]  
> Les fichiers journaux augmentent rapidement et dégradent les performances de l’application. Assurez-vous que l’espace disque requis est disponible avant d’activer la fonction de trace.

 

## <a name="interpreting-trace-data"></a>Interprétation des données de trace

Le flux de données de la fonction de trace reflète les fonctions WinHTTP appelées dans l’application et toutes les données HTTP envoyées ou reçues. Dans certains cas, les fonctions appelées en interne par WinHTTP sont également affichées.

L’illustration suivante montre une partie d’un fichier journal généré par la fonction de trace. Plusieurs éléments sont mis en surbrillance et étiquetés.

![exemple de suivi](images/ss-tracer-wco.png)

Chaque ligne de la sortie de trace contient des informations dans trois colonnes. La première colonne affiche la date et l’heure d’enregistrement de l’entrée. La deuxième colonne affiche un identificateur de demande (ID) qui peut être utilisé pour différencier plusieurs demandes. Si l’entrée de journal ne correspond pas à une demande spécifique, « \* session \* » s’affiche dans cette colonne. Il peut être utile de trier le fichier journal en fonction de cet ID pour afficher uniquement les événements qui se produisent pour une requête unique. L’exemple suivant montre une commande que vous pouvez utiliser pour trier le fichier journal.

**findstr 00000001 LogFile. log**

La troisième colonne affiche un appel de fonction, le trafic HTTP ou un message d’État inclus pour aider à interpréter la trace.

Lorsqu’une entrée de journal correspond à un appel de fonction, les paramètres de la fonction sont également enregistrés. Les adresses mémoire sont affichées au format hexadécimal, tandis que toutes les autres valeurs sont affichées sous forme de chaîne ASCII. La fonction de trace enregistre également l’heure et la valeur de retour pour chaque fonction.

Le format des données HTTP dépend des paramètres du Registre spécifiés avec l’outil de configuration de trace. Lorsque les données HTTP sont chiffrées, les données déchiffrées sont également affichées dans la sortie de trace.

 

 




