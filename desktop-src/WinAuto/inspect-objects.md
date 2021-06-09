---
title: Outils d’accessibilité-inspecter
description: Inspect (Inspect.exe) est un outil Windows qui vous permet de sélectionner n’importe quel élément d’interface utilisateur et d’afficher les données d’accessibilité de l’élément.
ms.assetid: 38edacbc-cf24-4818-b029-561b21e3704c
keywords:
- Inspecter l’outil
- Accessibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcef8efa9efc0241d0f813da01623a1c02e6d226
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827635"
---
# <a name="accessibility-tools---inspect"></a>Outils d’accessibilité-inspecter

> [!Important]
> **Inspect** est un outil hérité. Nous vous recommandons d’utiliser à la place [Accessibility Insights](https://accessibilityinsights.io/) .

**Inspect** (Inspect.exe) est un outil Windows qui vous permet de sélectionner n’importe quel élément d’interface utilisateur et d’afficher les données d’accessibilité de l’élément. Vous pouvez afficher les propriétés et les modèles de contrôles de Microsoft UI Automation, ainsi que les propriétés de Microsoft Active Accessibility. **Inspect** vous permet également de tester la structure de navigation des éléments Automation dans l’arborescence UI Automation et les objets accessibles dans la hiérarchie Microsoft Active Accessibility.

## <a name="requirements"></a>Spécifications

Pour examiner l’Automation d’interface utilisateur, UI Automation doit être présent sur le système. Pour plus d’informations, consultez la section « Configuration requise » d' [UI Automation](entry-uiauto-win32.md).

L' **inspection** est installée dans le cadre de l’ensemble d’outils du kit de développement logiciel (SDK) Windows, mais elle n’est pas distribuée sous forme de téléchargement distinct. Le SDK Windows comprend tous les outils liés à l’accessibilité documentés dans cette section.

[Téléchargez le SDK Windows](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk/).

> [!NOTE]
> Pour les versions antérieures du SDK Windows, consultez l' [Archive des SDK Windows et des émulateurs](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive/).

**Inspect.exe** se trouve dans le \\ dossier bin \\ < *version* > \\ < *Platform*> du chemin d’installation du kit de développement logiciel (SDK) (vous n’êtes généralement pas obligé d’exécuter en tant qu’administrateur).

## <a name="the-inspect-window"></a>Fenêtre Inspect

La fenêtre **Inspect** comporte plusieurs parties principales :

- Barre de titre. Affiche le handle de fenêtre d' **inspection** (HWND).
- Barre de menus. Fournit l’accès pour **inspecter** les fonctionnalités.
- Barre d'outils. Fournit l’accès pour **inspecter** les fonctionnalités.
- Arborescence. Présente la structure hiérarchique des éléments d’interface utilisateur sous la forme d’un contrôle d’arborescence que vous pouvez utiliser pour naviguer parmi les éléments.
- Vue de données. Affiche toutes les propriétés d’accessibilité exposées pour l’élément d’interface utilisateur sélectionné.

Les commandes disponibles dans la barre de menus sont également disponibles dans la barre d’outils. L’image suivante illustre l’outil **Inspect** qui interroge les propriétés UI Automation de l’élément de menu **Modifier** dans le Bloc-notes.

![capture d’écran montrant l’interface utilisateur de l’outil d’inspection](images/inspect.png)

## <a name="using-inspect"></a>Utilisation de l’inspection

Lorsque vous lancez l' **inspection**, l' **arborescence** affiche l’emplacement de l’élément d’interface utilisateur actuellement sélectionné dans la hiérarchie d’éléments, et la vue de **données** affiche les informations de propriété pour l’élément d’interface utilisateur sélectionné. Vous pouvez naviguer dans l’interface utilisateur pour afficher des informations d’accessibilité sur chaque élément de l’interface utilisateur. Par défaut, **Inspect** effectue le suivi du focus du clavier ou de la souris. Lorsque le focus est modifié, la vue de **données** est mise à jour avec les informations de propriété de l’élément ayant le focus.

Pour naviguer parmi les éléments d’interface utilisateur, vous pouvez utiliser l’une des options suivantes :

- Souris
- Le clavier
- Contrôle Tree-View dans l' **arborescence**
- Options de navigation dans le menu de **navigation**
- Options de navigation dans la barre d’outils

Les trois dernières options vous permettent de naviguer dans la hiérarchie d’arborescence de l’interface utilisateur. La structure de cette arborescence peut différer légèrement entre l’automatisation d’UI et les modes de Active Accessibility de Microsoft.

## <a name="verifying-accessibility-property-information"></a>Vérification des informations de propriété d’accessibilité

La vue **données** affiche les informations de propriété de l’élément d’interface utilisateur qui est actuellement sélectionné. Vous pouvez configurer **Inspect** pour afficher des informations sur toutes les propriétés d’accessibilité ou sur un sous-ensemble de ces propriétés. Vous pouvez également spécifier d’autres options d’affichage, par exemple si l' **inspection** doit rester au-dessus d’autres interfaces utilisateur, ou si l' **inspection** doit mettre en surbrillance un rectangle englobant autour de l’élément sélectionné. Une fois que vous avez configuré l' **inspection** pour qu’elle fonctionne comme vous le souhaitez, vous pouvez commencer à naviguer entre les éléments d’interface utilisateur et à afficher les informations de propriété. **Inspect** enregistre vos paramètres de configuration lorsqu’il se ferme et les utilise pour initialiser la session d' **inspection** suivante.

### <a name="configure-property-settings"></a>Configurer les paramètres de propriété

1. Dans le menu **options** , sélectionnez **paramètres...**, ou sélectionnez **afficher la boîte de dialogue des paramètres** dans la barre d’outils.
2. Dans la liste **afficher dans la fenêtre principale** , sélectionnez les propriétés que vous souhaitez afficher dans la vue de **données** de **Inspect**.
3. Dans la liste **afficher dans l’info-bulle d’informations** , sélectionnez les propriétés que vous souhaitez afficher dans une info-bulle.
4. Pour afficher les propriétés que l’élément d’interface utilisateur peut ne pas prendre en charge, activez la case à cocher **afficher les propriétés non prises en charge** .
5. Cliquez sur **OK**.

### <a name="to-configure-viewing-options"></a>Pour configurer les options d’affichage

- Dans le menu **options** ou dans la barre d’outils, vous pouvez sélectionner les options d’affichage suivantes.

| Lorsque cette option est sélectionnée | **Inspecter**                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toujours visible                | Apparaît en haut de toute autre fenêtre à l’écran.                                                                                                                                                                                  |
| Mode MSAA                    | Affiche des informations sur les propriétés de Microsoft Active Accessibility.                                                                                                                                                                      |
| Mode UI Automation           | Affiche les informations de propriété UI Automation.                                                                                                                                                                                       |
| Affichage Windows visible uniquement    | Disponible uniquement en mode MSAA.                                                                                                                                                                                                       |
| Affichage brut                     | Présente l' [affichage brut](uiauto-treeoverview.md) de l’arborescence UI Automation ou de l’arborescence MSAA dans l' **arborescence** .                                                                                                             |
| Affichage de contrôle                 | Présente l' [affichage de contrôle](uiauto-treeoverview.md) de l’arborescence UI Automation dans l' **arborescence** . Disponible en mode UI Automation uniquement.                                                                            |
| Affichage de contenu                 | Présente l' [affichage du contenu](uiauto-treeoverview.md) de l’arborescence UI Automation dans l' **arborescence** . Disponible en mode UI Automation uniquement.                                                                            |
| Barre d’outils survol active         | Active les boutons de la barre d’outils au pointage de la souris, au lieu d’un clic de souris.                                                                                                                                                      |
| Signal sonore en cas d’erreur                | Émet un signal sonore quand une erreur est détectée lors d’une opération UI Automation ou MSAA.                                                                                                                                                          |
| \_Indicateur SPI SCREENREADER       | Suppose qu’un lecteur d’écran est présent. Cet indicateur indique qu’une application doit fournir des informations textuelles au lieu de graphiques. Vous ne devez pas supposer que cet indicateur est défini simplement parce qu’un lecteur d’écran est présent.         |
| Afficher le rectangle de surbrillance     | Met en surbrillance un rectangle autour de l’élément ayant le focus.                                                                                                                                                                              |
| Afficher la surbrillance du signe insertion         | Met en surbrillance le signe insertion. Disponible uniquement en mode MSAA.                                                                                                                                                                                 |
| Afficher l’info-bulle d’informations     | Affiche les informations de propriété dans une info-bulle.                                                                                                                                                                                           |
| Surveiller le focus                  | Suit le focus clavier. Quand cette option est sélectionnée, un hook d’événement de focus asynchrone est installé et déplace le signe insertion vers le coin supérieur gauche de l’élément ayant le focus. L' **inspection** peut ainsi actualiser ses propriétés en environ une seconde. |
| Attention                  | Suit le signe insertion. Disponible uniquement en mode MSAA.                                                                                                                                                                                    |
| Curseur Watch                 | Suit le curseur.                                                                                                                                                                                                                |
| Bulles d’info-bulle               | Suit les info-bulles.                                                                                                                                                                                                              |
| Afficher l’arborescence                    | Affiche l' **arborescence** .                                                                                                                                                                                                        |

## <a name="verifying-accessibility-navigation"></a>Vérification de la navigation dans l’accessibilité

Une fois que vous avez sélectionné un élément d’interface utilisateur à l’aide de l' **inspection**, vous pouvez vérifier que l’élément expose la navigation Windows Automation correcte pour les produits de technologie d’assistance.

### <a name="verify-accessibility-navigation"></a>Vérifier la navigation d’accessibilité

1. Ouvrez **inspection** et l’application que vous voulez tester.
2. Sélectionnez l’élément d’interface utilisateur à partir duquel vous souhaitez démarrer la navigation.
3. Dans la vue de **données** , vérifiez que l’élément expose les propriétés appropriées relatives à la navigation.
4. Utilisez l' **arborescence** , le menu de **navigation** ou les boutons de navigation de la barre d’outils pour naviguer dans l’interface utilisateur et vérifier que chaque élément expose les propriétés de navigation appropriées.
    > [!Note]  
    > Les options du menu de **navigation** et les boutons de la barre d’outils de navigation varient en fonction de l’emplacement de l’élément sélectionné dans l’arborescence.

## <a name="interacting-with-ui-elements"></a>Interaction avec les éléments d’interface utilisateur

Windows Automation expose des méthodes qui permettent aux produits de technologie d’assistance d’interagir avec un élément d’interface utilisateur comme si la souris ou le clavier était utilisé (par exemple, pour cliquer sur un bouton). Le menu **inspecter** l’action permet aux testeurs d’appeler les méthodes d’automatisation Windows sur un élément (par exemple, **Invoke. Invoke** appelle la méthode [**IUIAutomationInvokePattern :: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) ).

### <a name="interact-with-ui-elements"></a>Interagir avec les éléments d’interface utilisateur

1. Ouvrez **inspection** et l’application que vous voulez tester.
2. Sélectionnez l’élément d’interface utilisateur avec lequel vous souhaitez interagir.
3. Dans le menu **action** ou la barre d’outils, sélectionnez l’action qui correspond à la méthode Windows Automation que vous souhaitez appeler.

Le menu **action** contient les éléments d' **actualisation** et de focus, ainsi que d’autres éléments qui varient selon que le mode UI Automation ou **le** mode MSAA est sélectionné. En mode UI Automation, les autres éléments reflètent les modèles de contrôle pris en charge par l’élément d’interface utilisateur actuellement sélectionné. En mode MSAA, les autres éléments se composent toujours des éléments suivants :

| Action                | Description                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Actualiser               | Actualise l’interface utilisateur. Disponible en mode MSAA et UI Automation.                                               |
| Action par défaut        | Exécute l’action par défaut pour l’élément.                                                                          |
| Priorité                 | Définit le focus sur l’élément. Disponible en mode MSAA et UI Automation.                                                  |
| Sélectionnez                | Sélectionne l’élément.                                                                                                  |
| Étendre la sélection      | Étend la sélection des éléments pour inclure tous les éléments entre le premier élément sélectionné et l’élément actuel. |
| Ajouter à la sélection      | Sélectionne l’élément actuel (tel qu’un élément de liste).                                                                    |
| Supprimer de la sélection | Supprime l’élément actuel de la sélection.                                                                       |
| SetAccValue           | Affecte la chaîne spécifiée à la valeur Microsoft Active Accessibility de l’élément.                                 |
| Enfant ayant le focus         | Navigue jusqu’à l’enfant de l’élément qui a actuellement le focus.                                                       |
| HitTest au curseur     | Navigue jusqu’à l’enfant de l’élément spécifié par le curseur de la souris.                                                      |
| HitTest...            | Ouvre la boîte de dialogue **HitTest** .                                                                                     |



 

## <a name="keyboard-shortcuts"></a>Raccourcis clavier

La plupart des éléments de menu peuvent être appelés à l’aide d’un raccourci clavier, même lorsque l’option **inspecter** n’est pas l’application active. Notez cependant que les touches de raccourci sont en conflit avec certaines applications.

Les touches de raccourci clavier suivantes activent les différentes options du menu :



| Pour                                                                                                                                       | Utiliser ce raccourci clavier |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Appelle l’action par défaut de l’objet sous le curseur (action par défaut). Disponible uniquement en mode MSAA.                                       | CTRL+MAJ+F2              |
| Sélectionnez l’objet sous le curseur (Select). Disponible uniquement en mode MSAA.                                                                        | Ctrl+Maj+F3              |
| Définissez le focus clavier sur l’objet situé sous le curseur (Focus).                                                                                   | CTRL + Maj + F4              |
| Accédez à l’objet frère précédent à partir de celui situé sous le curseur. Cette commande permet d’accéder aux objets uniquement au sein d’un conteneur (frère précédent). | CTRL+MAJ+F5              |
| Déplacer vers le parent de l’objet (parent).                                                                                                            | Ctrl+Maj+F6              |
| Accède au premier enfant de l’objet actuel (premier enfant).                                                                                     | CTRL + MAJ + F7              |
| Accédez à l’objet frère suivant à partir de celui situé sous le curseur. Cette commande permet d’accéder aux objets uniquement au sein d’un conteneur (frère suivant).         | CTRL + MAJ + F8              |
| Atteindre le dernier enfant de l’objet actuel (dernier enfant).                                                                                       | Ctrl+Maj+F9              |
| Déplacer vers l’objet sous le curseur de la souris (HitTest au curseur). Disponible uniquement en mode MSAA.                                                      | CTRL+MAJ+1               |
| Copiez le contenu de la vue de données dans le presse-papiers (copier tout).                                                                                  | CTRL+MAJ+4               |
| Actualiser le contenu de la vue de données (Actualiser).                                                                                                 | CTRL+MAJ+5               |
| Regardez l’objet qui a le focus (Regardez le focus).                                                                                                   | CTRL+MAJ+6               |
| Placez le curseur sur l’objet frère situé à gauche de celui où se trouve le curseur (à gauche). Disponible uniquement en mode MSAA.                                        | CTRL+MAJ+7               |
| Accédez à l’objet frère situé au-dessus de l’objet sur lequel le curseur se trouve (haut). Disponible uniquement en mode MSAA.                                                | CTRL+MAJ+8               |
| Placez le curseur sur l’objet frère situé sous celui où se trouve le curseur (vers le bas). Disponible uniquement en mode MSAA.                                                 | CTRL+MAJ+9               |
| Accédez à l’objet frère situé à droite de celui où se trouve le curseur (à droite). Disponible uniquement en mode MSAA.                                      | CTRL + MAJ + 0               |

## <a name="related-topics"></a>Rubriques connexes

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Outils de test](testing-tools.md)
- [Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
- [UI Automation Verify](ui-automation-verify.md)
- [Visionneuse de l’étendue de l’ergonomie (AccScope)](accscope.md)
