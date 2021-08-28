---
title: Interface utilisateur graphique AccChecker
description: Cette rubrique décrit les éléments qui composent l’interface graphique utilisateur AccChecker.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf645a3afd35bdd906d1ab26453d16672311cb4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473385"
---
# <a name="the-accchecker-graphical-user-interface"></a>Interface utilisateur graphique AccChecker

Cette rubrique décrit les éléments qui composent l’interface graphique utilisateur AccChecker.

-   [Onglet vérifications](#verifications-tab)
-   [Onglet résultats](#results-tab)
-   [Onglets lecteur d’écran MSAA et UIA](#msaa-and-uia-screen-reader-tabs)
-   [Onglets d’arborescence MSAA et UIA](#msaa-and-uia-tree-tabs)
-   [Menu fichier](#file-menu)
-   [Rubriques connexes](#related-topics)

## <a name="verifications-tab"></a>Onglet vérifications

AccChecker démarre avec la vue par défaut de l’onglet **vérifications** :

![Capture d’écran montrant l’onglet « vérifications » dans l’outil de vérification de l’accessibilité U I.](images/accchecker-verifications-tab.png)

L’onglet **vérifications** contient les composants suivants.

-   **Sélecteur de cible de vérification** Offre les options suivantes pour sélectionner une application ou un contrôle cible.
    -   Choisissez une cible dans la liste déroulante préremplie. Cette liste contient tous les HWND de niveau supérieur identifiés au démarrage.
    -   Choisissez un HWND en fonction de l’emplacement du curseur de la souris (les contrôles sélectionnables sont mis en surbrillance avec un rectangle rouge). Cette option vous permet de sélectionner n’importe quel objet visible ayant un HWND.
    -   Entrez un HWND particulier.
-   Liste de vérification des **routines de vérification** Permet de sélectionner la routine de vérification souhaitée à exécuter sur une application ou un contrôle. Pour plus d’informations, consultez routines de vérification.
-   **Sélecteur de fichier de suppression d’erreur et d’avertissement** Les fichiers de suppression sont générés à partir de l’onglet **résultats** de la vérification. En cliquant avec le bouton droit sur un message d’erreur ou d’avertissement et en sélectionnant **supprimer** dans le menu contextuel, un indicateur est défini pour ce message. Si la case à cocher **suppressions** est activée, les entrées supprimées apparaissent dans la liste. Une entrée supprimée peut être supprimée en utilisant le même menu contextuel que celui utilisé pour la supprimer.

    Un fichier de suppression est enregistré au format XML en sélectionnant **enregistrer la suppression** dans le menu **fichier** . Ce fichier est consommé lors des exécutions de vérification suivantes où les messages sont masqués. Pour supprimer le fichier de suppression, cliquez sur **Effacer**. Pour plus d’informations sur des messages spécifiques, consultez messages du journal de vérification. Utilisez l’option **enregistrer le journal** du menu **fichier** pour enregistrer la liste entière sous forme de fichier journal au format XML ou sous forme de fichier texte mis en forme.

    ![accchecker onglet résultats avec l’élément de contexte de suppression mis en surbrillance](images/accchecker-results-tab-with-suppress.png)

    l’exemple suivant montre le contenu d’un fichier de suppression généré en exécutant les vérifications des **propriétés** sur le Windows application du panneau de configuration du pare-feu. L’erreur avec l’ID « ElementHasNoName » a été choisie pour la suppression dans cet exemple.

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   **Afficher les résultats classés par ordre de priorité** Offre les options suivantes pour filtrer les résultats de la vérification par priorité.
    -   **Tout** Inclure tous les résultats, quelle que soit la priorité.
    -   **P1 uniquement** Inclure uniquement les résultats de priorité 0 et de priorité 1.
    -   **P1 P2 uniquement** Incluez les résultats de priorité 0 à priorité 2.
-   **Exécuter les vérifications sélectionnées** Fournit le bouton **exécuter des vérifications** pour démarrer le processus de vérification. Lorsque les vérifications sont en cours d’exécution, le bouton prend la valeur **annuler les vérifications** et peut être utilisé pour arrêter les vérifications une fois l’exécution du en cours terminée.

## <a name="results-tab"></a>Onglet Résultats

L’onglet **résultats** est rempli une fois les tâches de vérification sélectionnées terminées. Il comprend les composants suivants.

-   La liste des messages, qui affiche les messages d’erreur, d’avertissement et d’information générés par les tâches de vérification sélectionnées. Les messages affichés peuvent être filtrés par type à l’aide des cases à cocher au-dessus de la liste des messages.
-   Détails du message et capture d’écran de la cible de vérification. La sélection d’un message dans la liste des messages affiche plus de détails et met en surbrillance l’élément correspondant dans le volet de capture d’écran. Le bouton **visualiser** , bascule AccChecker vers l’onglet de l' **arborescence MSAA** . Si une erreur est mise en surbrillance sous l’onglet **résultats** , l’élément correspondant est mis en surbrillance sous l’onglet de l' **arborescence MSAA** .

Cliquer avec le bouton droit sur un message expose un menu contextuel avec les éléments suivants.

-   **Supprimer** Ajoute le message à la liste de suppression.
-   **Copier dans le presse-papiers** Copie les détails du message dans le presse-papiers.
-   **Visualiser** Bascule AccChecker vers l’onglet d' **arborescence MSAA** . L’élément qui correspond à l’erreur sélectionnée est mis en surbrillance.
-   **Aide** Affiche des informations supplémentaires sur le message.

## <a name="msaa-and-uia-screen-reader-tabs"></a>Onglets lecteur d’écran MSAA et UIA

Les onglets lecteur d’écran MSAA et lecteur d’écran UIA sont similaires. Les deux affichent une transcription des éléments rencontrés dans un parcours simulé de la cible de vérification par un lecteur d’écran, à l’exception de l’implémentation MSAA, tandis que l’autre montre l’implémentation de UIA.

Les éléments sont consultés et journalisés comme un lecteur d’écran. Les informations présentées dans cet onglet sont essentielles pour confirmer que seules les informations utiles et pertinentes sont annoncées. Par exemple, un nom de contrôle de son mode normal, tel que « Edit MenuItem » ou « PushButton Close », est acceptable ; Toutefois, un nom de contrôle qui n’a pas de sens, tel que « CPNavPanel22 » ou « DefaultValue1 », n’est pas acceptable. Le bouton **visualiser** , force AccChecker à basculer vers l' **arborescence MSAA** ou l’onglet d' **arborescence UIA** . Si un élément est mis en surbrillance sous l’onglet **lecteur d’écran** , l’élément correspondant est mis en surbrillance dans l' **arborescence MSAA** ou l’onglet d' **arborescence UIA** .

La routine de vérification **Screenreader** sous **consistance** doit être sélectionnée dans l’onglet **vérifications** de l' **onglet lecteur d’écran MSAA** à afficher. De même, la routine de vérification **UiaScreenReader** doit être sélectionnée pour que l’onglet **lecteur d’écran UIA** s’affiche.

la capture d’écran suivante montre l’onglet lecteur de l’écran UIA avec un exemple de vérification de Bloc-notes.

![accchecker onglet lecteur d’écran affichant les exemples de résultats de la vérification](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a>Onglets d’arborescence MSAA et UIA

Si vous exécutez une routine de vérification, AccChecker compile tous les éléments visibles dans la cible de vérification et les affiche hiérarchiquement sous l’onglet de l' **arborescence MSAA** et l’onglet d' **arborescence UIA** . la capture d’écran suivante montre l’onglet d’arborescence MSAA avec la hiérarchie d’éléments pour Bloc-notes.

![onglet d’arborescence accchecker MSAA](images/accchecker-tree-tab.png)

## <a name="file-menu"></a>Menu Fichier




| Menu | Commande | Description | 
|------|---------|-------------|
| <strong>Fichier</strong>$ {Remove} $<br /> | <strong>Ouvrir</strong> | Fournit les options suivantes.<br /><ul><li><strong>Dll de vérification</strong> Ouvre une DLL de vérification. Les vérifications AccChecker natives sont encapsulées dans une DLL autonome (VerificationRoutines.dll). Cette conception permet aux équipes de test de créer leur propre ensemble de vérifications en fonction de la plateforme d’interface utilisateur en cours de test.</li><li><strong>Fichier journal</strong> Vous permet de choisir un fichier journal de vérification à ouvrir.</li></ul> | 
| <strong>Charger automatiquement les vérifications disponibles</strong> | Charge automatiquement toutes les vérifications AccChecker disponibles. | 
| <strong>Enregistrer le journal</strong> | Enregistrez le journal de vérification au format XML ou sous forme de texte brut. Le texte brut est plus lisible. | 
| <strong>Enregistrement de la suppression</strong> | Enregistrez le journal des suppressions au format XML. Ce fichier spécifie les messages de vérification à ignorer dans les tests de régression. | 
| <strong>Quitter</strong> | Ferme l’outil AccChecker. | 
| <strong>Vérifications</strong>$ {Remove} $<br /> | <strong>Exécuter maintenant</strong> | Exécutez les routines de vérification comme spécifié pour la cible de vérification choisie. | 
| <strong>Activer tout</strong> | Activez toutes les cases à cocher de la routine de vérification. | 
| <strong>Désactiver tout</strong> | Désactivez toutes les cases à cocher de la routine de vérification. | 
| <strong>Options</strong> | <strong>Always On haut</strong> | Faites de AccChecker la fenêtre de niveau supérieur dans l’ordre de plan. | 
| <strong>Aide</strong>$ {Remove} $<br /> | <strong>Aide</strong> | Affichez les informations d’aide. | 
| <strong>À propos de</strong> | Affichez la version de AccChecker et une adresse de messagerie pour contacter Microsoft sur AccChecker. | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
</dt> </dl>

 

 





