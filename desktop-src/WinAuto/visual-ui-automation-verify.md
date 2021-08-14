---
title: Vérification de l’interface utilisateur Visual Automation
description: vérification de l’interface utilisateur de visual Automation (visual UIA verify) est un Windows \ 32 ; Pilote d’interface graphique utilisateur pour la bibliothèque de test UIA conçue pour le test manuel de l’Automation d’interface utilisateur.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c50fdd123d24c8a6ef4215ae2451cf49b854b60b26c5d741db1921c42f6f7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563653"
---
# <a name="visual-ui-automation-verify"></a>Vérification de l’interface utilisateur Visual Automation

vérification de l’interface utilisateur de visual automation (visual UIA verify) est un pilote d’interface graphique utilisateur Windows pour la bibliothèque de Test UIA conçue pour le test manuel de l’Automation d’interface utilisateur. Il fournit une interface à la fonctionnalité de bibliothèque de tests UIA qui élimine la surcharge de codage d’un outil en ligne de commande.

-   [Commandes de menu](#menu-commands)
-   [Volets fonctionnels](#functional-panes)
    -   [Volet de l’arborescence des éléments Automation](#automation-elements-tree-pane)
    -   [Volet tests](#tests-pane)
    -   [Volet Résultats des tests](#test-results-pane)
    -   [Volet Propriétés](#properties-pane)

Visual UIA Verify ne prend en charge que le journal XML de vérification UIA (WUIALoggerXml.dll) en mode natif. Les transformations XML sélectionnables par l’utilisateur sont incorporées dans Visual UIA Verify pour présenter diverses vues du rapport d’enregistreur XML dans le volet **résultats des tests** .

Par défaut, Visual UIA Verify charge le fournisseur UI Automation côté client fourni avec la version d’origine d’UI Automation. Vous pouvez choisir de ne pas charger ce fournisseur en ajoutant **/NOCLIENTSIDEPROVIDER** dans l’option de ligne de commande de VisualUIVerifyNative.exe.

La capture d’écran suivante montre les principales zones fonctionnelles de l’interface utilisateur vérification de Visual UIA.

![principales zones fonctionnelles de l’interface utilisateur vérification de Visual UIA](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Commandes de menu

Le tableau suivant décrit les commandes du menu vérification de Visual UIA.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Menu</th>
<th>Commande</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>File</strong></td>
<td><strong>Quitter</strong></td>
<td>Quittez la vérification de Visual UIA.</td>
</tr>
<tr class="even">
<td><strong>Visualiser</strong></td>
<td><strong>Mettre en surbrillance</strong></td>
<td>Mettez en surbrillance le rectangle englobant de l’élément sélectionné dans le volet de l' <strong>arborescence éléments Automation</strong> . Les options suivantes sont disponibles.
<ul>
<li><strong>Rectangle</strong>: ligne rouge pleine.</li>
<li><strong>Rectangle de fondu</strong>: ligne rouge pleine qui disparaît après quelques secondes.</li>
<li><strong>Rayons et rectangle</strong>: trait rouge plein avec des lignes de surbrillance bleue supplémentaires qui rayonnent à partir de chaque angle du rectangle englobant.</li>
<li><strong>None</strong>: aucune mise en surbrillance visible.</li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><strong>Arborescence des éléments d’automatisation</strong>$ {Remove} $<br />
</td>
<td><strong>Actualiser l’élément sélectionné</strong></td>
<td>Actualise les enfants de l’élément sélectionné dans le volet d' <strong>arborescence éléments Automation</strong> . La liste d’éléments est statique et n’est pas actualisée dynamiquement (automatiquement) si l’arborescence d’éléments change.</td>
</tr>
<tr class="even">
<td><strong>Navigation</strong></td>
<td>Naviguez dans la hiérarchie de l’arborescence d’éléments jusqu’à l’un des éléments suivants.
<ul>
<li><strong>Parent</strong>: accéder à l’élément parent.</li>
<li><strong>Premier enfant</strong>: accéder au premier élément enfant.</li>
<li><strong>Frère suivant</strong>: accédez au premier élément frère.</li>
<li><strong>Frère précédent</strong>: accède à l’élément frère précédent.</li>
<li><strong>Dernier enfant</strong>: accéder au dernier élément enfant.</li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><strong>Mode</strong>$ {Remove} $<br />
</td>
<td><strong>Always On haut</strong></td>
<td>La fenêtre de vérification du décodeur Visual UIA reste en haut de l’ordre de plan du bureau.</td>
</tr>
<tr class="even">
<td><strong>Mode sensitif (utilisez Ctrl)</strong></td>
<td>Quand la touche CTRL est enfoncée, l’élément sous le curseur de la souris est identifié comme étant l’élément concerné. Le volet d' <strong>arborescence éléments Automation</strong> est actualisé et l’élément correspondant dans la liste d’éléments est mis en surbrillance.</td>

</tr>
<tr class="odd">
<td><strong>Focus, suivi</strong></td>
<td>Au fur et à mesure que le focus change, l’élément ayant le focus est identifié comme l’élément d’intérêt. Le volet d' <strong>arborescence éléments Automation</strong> est actualisé et l’élément correspondant dans la liste d’éléments est mis en surbrillance.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Tests</strong>$ {Remove} $<br />
</td>
<td><strong>Aller à gauche</strong></td>
<td>Déplacer un nœud vers la gauche dans l’arborescence des <strong>tests</strong> .</td>
</tr>
<tr class="odd">
<td><strong>Monter</strong></td>
<td>Déplacer un nœud vers le haut dans l’arborescence des <strong>tests</strong> .</td>

</tr>
<tr class="even">
<td><strong>Descendre</strong></td>
<td>Déplacer un nœud vers le dessous dans l’arborescence des <strong>tests</strong> .</td>

</tr>
<tr class="odd">
<td><strong>Aller à droite</strong></td>
<td>Déplacer un nœud vers la droite dans l’arborescence <strong>tests</strong> .</td>

</tr>
<tr class="even">
<td><strong>Exécuter le ou les tests sélectionnés sur l’élément sélectionné</strong></td>
<td>Exécuter les tests sélectionnés à partir de l’arborescence <strong>tests</strong> sur l’élément sélectionné.</td>

</tr>
<tr class="odd">
<td><strong>Filtrer les problèmes connus</strong></td>
<td>Filtrez les bogues UI Automation connus des résultats des tests.</td>

</tr>
<tr class="even">
<td><strong>Aide</strong></td>
<td><strong>À propos de la vérification de l’interface utilisateur Visual Automation</strong></td>
<td>Affichez la version du logiciel et les informations de copyright pour Visual UIA Verify.</td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a>Volets fonctionnels

Cette section décrit les volets fonctionnels de l’interface utilisateur vérification de Visual UIA.

-   [Volet de l’arborescence des éléments Automation](#automation-elements-tree-pane)
-   [Volet tests](#tests-pane)
-   [Volet Résultats des tests](#test-results-pane)
-   [Volet Propriétés](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Volet de l’arborescence des éléments Automation

Le volet d' **arborescence éléments Automation** contient un instantané hiérarchique des objets d’élément Automation qui sont disponibles pour le test. L’élément supérieur dans l’arborescence représente le bureau.

Cette vue est une collection statique qui est compilée lors du démarrage de la vérification de Visual UIA. Pour actualiser la vue sur le nœud sélectionné, utilisez la commande de menu **Actualiser l’élément sélectionné** ou le bouton de barre d’outils.

La capture d’écran suivante montre le volet d' **arborescence éléments Automation** .

![volet de l’arborescence des éléments Automation de la vérification de Visual UIA](images/automation-elements-tree-pane.png)

Un nœud grisé (non disponible) dans l' **arborescence des éléments d’automatisation** indique que l’élément est membre de la vue brute UI Automation, mais ne remplit pas les conditions nécessaires pour être considéré comme un membre de l’affichage de contenu ou de l’affichage de contrôle. Toutefois, l’élément peut toujours être testé à partir de vérification de l’interface utilisateur de Visual Automation. Pour plus d’informations, consultez la [vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md).

Les commandes disponibles à partir de la barre d’outils de l' **arborescence des éléments Automation** sont les suivantes :

-   **Actualiser**: actualise le nœud sélectionné et ses enfants. Cette commande n’actualise pas l’intégralité de l’arborescence des éléments, sauf si le nœud racine est sélectionné.
-   **Parent (CTRL + MAJ + F6)**: accéder au parent du nœud actuel.
-   **Premier enfant (Ctrl + Maj + F7)**: accéder au premier enfant du nœud actuel.
-   **Frère suivant (Ctrl + Maj + F8)**: accéder à l’enfant frère suivant du nœud actuel.
-   **Frère précédent (Ctrl + Maj + F9)**: accéder au frère précédent du nœud actuel.
-   **Dernier enfant (CTRL + MAJ + F10)**: accéder au dernier enfant du nœud actuel.
-   **Focus Tracking**: active ou désactive la sélection de nœud en fonction du suivi du focus.

### <a name="tests-pane"></a>Volet tests

Le **volet tests** contient une liste de tests UI Automation organisés par type de test (**élément Automation**, **contrôle** et **modèle**) et priorité (**vérification de build**, **priorité 0**, **priorité 1**, **priorité 2** et **priorité 3**). Cette liste est générée en fonction du type de contrôle de l’élément sélectionné dans le volet d' **arborescence éléments Automation** . Pour plus d'informations, consultez [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

La capture d’écran suivante montre le volet **tests** .

![volet de test](images/test-pane.png)

Les commandes disponibles à partir de la barre d’outils **tests** sont les suivantes :

-   **Afficher**: spécifie les tests UI Automation à afficher. autrement dit, affichez tous les tests ou uniquement les tests adaptés au type de contrôle de l’élément sélectionné dans l' **arborescence des éléments Automation** (valeur par défaut).
-   **Type**: spécifie les types de test à afficher : **élément Automation**, **modèle** ou **contrôle**.
-   **Priorités**: spécifie les priorités de test à afficher : **vérification de build**, **priorité 0**, **priorité 1**, **priorité 2** ou **priorité 3**.
-   **Aller à gauche**: accéder au parent du nœud actuel.
-   **Monter**: accédez au frère précédent du nœud actuel.
-   **Descendre**: accédez au frère suivant du nœud actuel.
-   **Aller à droite**: accède au premier enfant du nœud actuel.
-   **Exécuter le (s) test (s) sélectionné (s)**: exécute les tests sur l’élément sélectionné dans l' **arborescence des éléments Automation**.

### <a name="test-results-pane"></a>Volet Résultats des tests

Le volet **résultats des tests** contient la fonctionnalité de vérification de la journalisation de vérification de visualable. La capture d’écran suivante montre le volet **résultats des tests** .

![volet résultats des tests](images/test-results-pane.png)

Les commandes disponibles dans la barre d’outils **résultats des tests** sont les suivantes :

-   **Précédent**: page précédente dans l’historique d’affichage du rapport.
-   **Transférer**: page suivante dans l’historique d’affichage du rapport.
-   **Global**: affiche un résumé des résultats des tests (**réussite**, **échec** et **erreur inattendue**). Le résultat du test est lié à l’affichage **tous les résultats** . La commande **globale** affiche un tableau comme celui qui suit.

    ![Tableau des résultats des tests globaux](images/overall-test-results.png)

-   **Tous les résultats**: affiche un journal détaillé pour chaque résultat de test, comme indiqué dans les tableaux suivants.

    ![exemple de journaliser les détails des résultats de l’affichage tous les résultats](images/all-results-log.png)

    Le nom du test dans le tableau **tous les résultats** est lié à une description de cas de test pour l’élément, comme dans le tableau suivant.

    ![Détails du cas de test](images/test-case-detail.png)

-   **Full log (journal complet**) : affiche une autre vue du journal détaillé pour chaque résultat de test, comme illustré dans la capture d’écran suivante.

    ![autre vue d’un cas de test, détails](images/alt-view-of-test-case-detail.png)

-   **XML**— affiche le code XML brut généré par l’enregistreur d’événements XML.
-   Recherche **rapide**: recherche en texte simple de la vue actuelle dans le volet **résultats des tests** .
-   **Ouvrir dans une nouvelle fenêtre**: ouvre la vue actuelle dans une nouvelle instance d’Internet Explorer.

### <a name="properties-pane"></a>Volet Propriétés

Le volet **Propriétés** contient une liste de propriétés UI Automation et de valeurs de propriété organisées par type de propriété : **accessibilité générale**, **identification**, **modèles** (modèles de contrôle), **État** et **visibilité**. Les valeurs de propriété sont renseignées dynamiquement en fonction du type de contrôle de l’objet sélectionné dans le volet d' **arborescence éléments Automation** . La capture d’écran suivante montre le volet **Propriétés** .

![volet Propriétés](images/properties-pane.png)

Si le contrôle sélectionné prend en charge un modèle de contrôle spécifique, Visual UIA Verify offre la possibilité d’appeler des méthodes prises en charge par ce modèle de contrôle. Par exemple, le [type de contrôle Window](uiauto-supportwindowcontroltype.md) prend en charge le [modèle de contrôle Window](uiauto-implementingwindow.md), qui a une méthode [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) qui peut être appelée à partir du volet **Propriétés** , comme indiqué dans la capture d’écran suivante. Pour plus d'informations, consultez [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

![méthode Close du modèle de contrôle Window appelée à partir du volet Propriétés](images/close-invoked-from-properties-pane.png)

Les commandes disponibles à partir de la barre d’outils **Propriétés** sont les suivantes :

-   **Actualiser**: actualise l’arborescence des **Propriétés** .
-   **Développer tout**: développe tous les nœuds dans l’arborescence des **Propriétés** .

 

 




