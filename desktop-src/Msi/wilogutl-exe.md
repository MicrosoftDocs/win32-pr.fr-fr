---
description: Wilogutl.exe aide à analyser les fichiers journaux à partir d’une installation Windows Installer et affiche les solutions suggérées aux erreurs qui se trouvent dans un fichier journal.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542062"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe aide à analyser les fichiers journaux à partir d’une installation Windows Installer et affiche les solutions suggérées aux erreurs qui se trouvent dans un fichier journal.

Les erreurs non critiques ne sont pas affichées. Wilogutl.exe peut être exécuté en mode silencieux ou à l’aide d’une interface utilisateur. L’outil génère des rapports en tant que fichiers texte dans l’interface utilisateur et en mode silencieux. Il fonctionne mieux avec les fichiers journaux de Windows Installer détaillés, mais il fonctionne également avec les journaux non détaillés. Pour plus d’informations, consultez [Journalisation](logging.md).

Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Syntaxe

**wilogutl.exe***\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*

Vous pouvez utiliser les lignes de commande suivantes pour exécuter en mode silencieux.

**Wilogutl/q/l** *c : \\ mymsilog. log* **/o** *c \\ OutputDir \\*

**Wilogutl/q/l** *c : \\ mymsilog. log*

## <a name="command-line-options"></a>Options de ligne de commande

Wilogutl.exe utilise les options de ligne de commande qui ne respectent pas la casse. Un séparateur de tirets peut être utilisé à la place d’une barre oblique.



| Option | Description                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| aucun   | S’exécute en mode interface utilisateur, sans options de ligne de commande.                                                                                                                                                   |
| /q     | Spécifie le mode silencieux. Wilogutl.exe génère des fichiers de rapport et n’affiche pas d’interface utilisateur.                                                                                            |
| /l     | Spécifie le nom du fichier journal à analyser. Cette option est requise lors de l’utilisation du mode silencieux.                                                                                           |
| /o     | Spécifie le répertoire de sortie pour les fichiers de rapport. Ce chemin de sortie est utilisé uniquement lors de l’exécution en mode silencieux. Si l’option n’est pas présente, les rapports sont placés dans le répertoire C : \\ WiLogResults. |



 

Quand elle est exécutée en mode interface utilisateur, Wilogutl.exe affiche les boîtes de dialogue suivantes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Analyseur de journal détaillé Windows Installer</td>
<td>La boîte de dialogue Windows Installerer l’analyseur de journal détaillé permet aux utilisateurs de sélectionner un fichier journal à analyser :
<ul>
<li>Le bouton <strong>ouvrir</strong> ouvre le fichier dans le bloc-notes. La zone d’aperçu peut être utilisée pour vérifier que le fichier journal correct a été sélectionné.</li>
<li>Le bouton <strong>analyser</strong> démarre l’analyse des fichiers journaux et affiche la boîte de dialogue vue détaillée du fichier journal.</li>
</ul></td>
</tr>
<tr class="even">
<td>Affichage détaillé du fichier journal</td>
<td>La boîte de dialogue Affichage détaillé du fichier journal affiche les informations d’erreur journalisées. Utilisez les boutons <strong>précédent</strong> et <strong>suivant</strong> pour parcourir plusieurs erreurs. Pour afficher les erreurs non critiques, activez la case à cocher <strong>afficher les erreurs de débogage ignorées</strong> . La version du programme d’installation sur l’ordinateur utilisé pour exécuter l’installation journalisée s’affiche. Si l’installation journalisée a été exécutée avec des autorisations élevées, la case à cocher <strong>installation élevée</strong> est activée et les informations sont fournies dans les zones de texte <strong>Détails des privilèges côté client</strong> et <strong>Détails des privilèges côté serveur</strong> . La boîte de dialogue vue détaillée du fichier journal contient les boutons suivants :<br/>
<ul>
<li><strong>États</strong> - Affiche la boîte de dialogue États des fonctionnalités et des composants.</li>
<li><strong>Propriétés</strong> - de Affiche la boîte de dialogue Propriétés.</li>
<li><strong>Stratégies</strong> - Affiche la boîte de dialogue stratégies.</li>
<li><strong>Journal</strong> - annoté html Afficher le journal comme fichier HTML annoté.</li>
<li><strong>Enregistrer les résultats</strong> - Enregistrer les fichiers de rapport dans le répertoire spécifié.</li>
<li><strong>Aide sur les messages d’erreur</strong> - Afficher l’aide du message d’erreur du programme d’installation.</li>
<li><strong>Aide</strong> - Afficher l’aide de Windows Installer analyseur de journal d’installation.</li>
<li><strong>Comment lire un fichier journal</strong> - Affichez le document d’aide du fichier journal.</li>
</ul></td>
</tr>
<tr class="odd">
<td>États des fonctionnalités et des composants</td>
<td>La boîte de dialogue États des fonctionnalités <strong>et</strong> des composants affiche les États des fonctionnalités et des composants :
<ul>
<li>La colonne <strong>fonctionnalité</strong> affiche le nom de la fonctionnalité dans le package d’installation.</li>
<li>La colonne <strong>composant</strong> indique le nom du composant dans le package d’installation.</li>
<li>La colonne <strong>installé</strong> indique l’état de la fonctionnalité ou du composant à la fin de l’installation.</li>
<li>La colonne <strong>requête</strong> affiche la sélection de l’utilisateur au cours de l’installation pour l’état de la fonctionnalité ou du composant.</li>
<li>La colonne <strong>action</strong> affiche l’action entreprise par le programme d’installation de la fonctionnalité ou du composant.</li>
</ul>
Pour plus d’informations, consultez <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> et <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.<br/></td>
</tr>
<tr class="even">
<td>Propriétés</td>
<td>La boîte de dialogue Propriétés affiche Windows Installer <a href="properties.md">Propriétés</a> et leurs valeurs à la fin de l’installation. Vous pouvez trier les propriétés par nom ou par valeur :
<ul>
<li>L’onglet <strong>client</strong> affiche les propriétés et les valeurs de la partie côté client de l’installation.</li>
<li>L’onglet <strong>serveur</strong> affiche les propriétés et les valeurs de la partie serveur de l’installation.</li>
<li>L’onglet <strong>imbriqué</strong> affiche les propriétés et les valeurs de toutes les <a href="concurrent-installations.md">installations simultanées</a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Stratégies</td>
<td>La boîte de dialogue stratégies affiche la <a href="system-policy.md">stratégie système</a> définie après l’installation :
<ul>
<li>Une valeur 0 (zéro) définie pour la stratégie signifie que la stratégie n’est pas activée.</li>
<li>La valeur 1 (un) signifie que la stratégie est activée.</li>
<li>La valeur ? (point d’interrogation) signifie que la valeur de stratégie n’est pas enregistrée dans le journal.</li>
</ul>
Si vous avez besoin d’une valeur de stratégie qui n’est pas dans le journal, essayez d’utiliser Regedit.exe pour vérifier les clés de Registre sur l’ordinateur qui n’a pas pu être installé.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a>Fichiers de rapport

Lorsque vous effectuez une analyse en mode silencieux ou que vous cliquez sur le bouton **enregistrer les résultats** dans la boîte de dialogue **vue détaillée du fichier journal** , l’outil analyseur d’installation de Windows Installer génère trois fichiers texte et un fichier journal annoté html.

Le tableau suivant identifie les noms et le contenu des fichiers de rapport.



| Nom                      | Description                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_summary.txt LogFileName  | Résume le fichier journal. Répertorie les informations affichées dans la boîte de dialogue Affichage détaillé du fichier journal et la première erreur.         |
| \_errors.txt LogFileName   | Identifie le nombre d’erreurs, les erreurs et les solutions recommandées. Ce fichier répertorie les erreurs critiques et non critiques. |
| \_policies.txt LogFileName | Identifie les noms et valeurs de stratégie définis à la fin de l’installation comme dans la boîte de dialogue stratégies.                       |
| Détails \_logfilename.htm  | Journal annoté HTML avec une légende pour le codage en couleurs.                                                                      |



 

## <a name="return-values"></a>Valeurs de retour

Si des arguments de ligne de commande non valides sont passés pour les opérations en mode silencieux, Wilogutl.exe ne fait rien, et le processus retourne l’une des valeurs du tableau suivant.



| Valeur | Signification                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | Le répertoire de sortie incorrect est spécifié.                                      |
| 2     | Un nom de fichier journal incorrect est spécifié.                                         |
| 3     | A réussi, mais il manque le commutateur obligatoire/l pour le nom du fichier journal. |
| 4     | Réussite de/l, mais absence du commutateur requis/q pour le mode silencieux.        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Outils de développement Windows Installer](windows-installer-development-tools.md)
</dt> </dl>

 

 




