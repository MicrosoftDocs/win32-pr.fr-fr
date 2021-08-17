---
title: Outils d’accessibilité-AccScope
description: L’outil AccScope permet aux développeurs et aux testeurs d’évaluer l’accessibilité de leur application pendant le développement et la conception de l’application, plutôt que dans les phases de test tardive du cycle de développement d’une application.
ms.assetid: 7C4D78CD-CDDA-8369-B747-6224C152A997
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e55aa40822b786ee69185abe753bb0bacd65345d042526a126b4c8343a2639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327719"
---
# <a name="accessibility-tools---accscope"></a>Outils d’accessibilité-AccScope

L’outil **AccScope** permet aux développeurs et aux testeurs d’évaluer l’accessibilité de leur application pendant le développement et la conception de l’application, plutôt que dans les phases de test tardive du cycle de développement d’une application. Le test peut même démarrer dès les premières phases de prototypage. **AccScope** peut visualiser la manière dont un lecteur d’écran expose les informations UI Automation fournies par une application, et peut afficher les zones où vous pouvez ajouter des informations ou une prise en charge à votre application pour améliorer son accessibilité.

> [!NOTE]
> **AccScope** est un outil hérité. nous vous recommandons d’utiliser à la place l' [accessibilité Informations](https://accessibilityinsights.io/) .

## <a name="about-accscope"></a>À propos de AccScope

**AccScope** est installé avec le kit de développement logiciel (SDK) Windows. Il se trouve dans le \\ dossier bin \\ < *version* > \\ < *Platform* > \\ AccScope du chemin d’installation du kit de développement logiciel (SDK). Exécutez le programme AccScope.exe.

**AccScope** est une application de bureau, pas une application du windows Store Windows. vous pouvez l’utiliser pour examiner n’importe quelle application qui s’affiche sous la forme d’une fenêtre, y compris une application de bureau ou une application du windows Store Windows.

Vous devrez peut-être exécuter **AccScope** en tant qu’administrateur la première fois que vous l’utilisez pour activer le mode narrateur.

**AccScope** est disponible dans le cadre des binaires des outils d’accessibilité, dans le SDK Windows. Il n’est pas distribué comme un téléchargement exe distinct et n’existe pas dans les kits de développement logiciel précédents.

## <a name="file-menu-options"></a>Options du menu fichier

- Sélectionnez **Actualiser** pour actualiser toutes les informations dans **AccScope** afin qu’elles correspondent à l’état actuel de la fenêtre cible. Pour une interface utilisateur qui contient un grand nombre d’éléments, cette exécution peut prendre plusieurs secondes.
- Activez ou désactivez la case à cocher **toujours visible** pour modifier le comportement de fenêtrage de l’interface utilisateur **AccScope** . L’option **toujours visible** est activée par défaut.
- Sélectionnez **quitter** pour quitter **AccScope**.

## <a name="view-options"></a>Options d’affichage

- Sélectionnez **plein écran** pour exécuter l’outil **AccScope** dans un affichage plein écran (puis utilisez la tabulation pour afficher la fenêtre cible). Si **AccScope** et l’application cible s’exécutent en mode plein écran, le positionnement, les rectangles englobants et la visualisation globale des éléments correspondent entre votre application et la vue **AccScope** .
    > [!Note]  
    > **AccScope** et sa cible doivent être exécutées sur le même affichage.

     

- Sélectionnez **focus automatique** pour permettre à AccScope de modifier la fenêtre cible chaque fois qu’un utilisateur déplace le focus vers la fenêtre (à l’aide de la souris ou du clavier).
- Sélectionnez **actualisation automatique** pour activer le mode **AccScope** qui actualise toutes les données d’accessibilité de la fenêtre cible toutes les 5 secondes. Cela est utile si les données Microsoft UI Automation de la fenêtre cible changent constamment.
- Sélectionnez **régions dynamiques** pour mettre en surbrillance les régions actives qui émettent des notifications dans la fenêtre cible. Le déclenchement d’un événement de zone dynamique affiche un message rouge qui contient des informations sur la zone dynamique, y compris son nom et sa valeur « Aria-Live » (ou la valeur ARIA équivalente pour les applications qui n’utilisent pas directement HTML, mais qui utilisent le concept de régions dynamiques dans la prise en charge d’UI Automation).

## <a name="element-mode"></a>Mode d’élément

Vous pouvez choisir d’afficher une fenêtre cible par le biais de l’un des modes suivants :

- **Contrôle feuille**: affiche une vue UI Automation des éléments de **contrôle** avec des relations parent-enfant, en d’autres termes une vue de contrôles interactifs de niveau feuille. Utilisez cette option pour voir si tous les contrôles interactifs s’affichent correctement dans l’arborescence UI Automation pour un affichage de **contrôle** .
- **Modèle de texte**: affiche les plages de texte visibles des conteneurs **TextPattern** à partir de la fenêtre cible. Utilisez cette option pour représenter visuellement les plages de texte visibles des éléments **TextPattern** d’UI Automation.
- **Narrateur**: affiche les éléments UI Automation que le narrateur peut identifier à l’aide de la métaphore « navigation d’élément » du narrateur.
- **Filtre personnalisé**: affiche une arborescence de contrôle filtrée avec un choix de sous-ensembles de contrôle : **Button**, **CheckBox**, **ComboBox**, **Grid**, **Hyperlink**, **List**, **menu** ou **table**.

La modification du paramètre de **mode d’élément** déclenche une actualisation de la visualisation. Pour une interface utilisateur qui contient un grand nombre d’éléments, cette exécution peut prendre plusieurs secondes.

## <a name="layout-options"></a>Options de disposition

Vous pouvez sélectionner **visuel** ou **liste** comme mode de visualisation pour la disposition **AccScope** . L’élément **visuel** place les éléments dans l’espace de coordonnées dans la même relation que la fenêtre cible. **Répertorie** les éléments d’une liste décroissante alignée à gauche dans la fenêtre **AccScope** et l’ordre de la liste équivaut à l’ordre de tabulation ou à l’ordre de lecture.

- Sélectionnez une option dans **afficher les images** pour contrôler le moment où les rectangles simples pour les éléments d’image sont remplacés par l’image réelle (ou une petite fenêtre d’affichage de cette image, car les rectangles sont souvent plus petits que l’image réelle). La valeur par défaut est **on Hover**, qui affiche l’image lorsque vous naviguez dans **AccScope** et pointez la souris sur le rectangle pour un élément image. Les autres choix sont **toujours** ou **jamais**.
- Sélectionnez **afficher l’info-bulle** pour afficher les informations sur l’élément de base chaque fois que vous pointez la souris sur un élément dans la visualisation **AccScope** . Si le **mode d’élément** est un **contrôle feuille** ou un **modèle de texte** , les informations affichées dans l’info-bulle sont les propriétés UI Automation au niveau de l’élément dont la priorité est la plus élevée. Si le **mode d’élément** est **narrateur** , les informations incluent le texte que le narrateur lira pour l’élément.
- Sélectionnez **afficher les nombres** pour afficher les numéros de séquence qui indiquent l’ordre de rendu du contrôle dans la disposition. Le modèle de nombre est basé sur le paramètre de **mode d’élément** :
    - **Contrôle feuille**: les nombres indiquent l’ordre dans lequel les contrôles terminaux s’affichent dans l’arborescence UI Automation.
    - **Modèle de texte**: les nombres indiquent l’ordre dans lequel les plages de texte s’affichent dans une plage de documents.
    - **Narrateur**: le nombre indique l’ordre dans lequel les éléments sont rendus dans la navigation des éléments du narrateur.

## <a name="choosing-a-window"></a>Choix d’une fenêtre

Dans la **fenêtre** étiquette, vous trouverez une liste déroulante qui répertorie toutes les fenêtres HWND actuellement actives sur le système. Le texte de chaque fenêtre qui s’affiche dans la liste déroulante est le titre de la fenêtre, ainsi qu’un ID de fenêtre hexadécimale entre crochets. Choisissez l’une des ces pour modifier la fenêtre cible sur laquelle **AccScope** fait l’État. Vous pouvez choisir de nouveau le même élément pour avoir le même comportement qu’une **actualisation** explicite.

## <a name="using-the-accscope-visualization"></a>Utilisation de la visualisation AccScope

L’image ci-dessous est une capture d’écran de la visualisation **AccScope** . Cette capture d’écran particulière montre l’outil **AccScope** qui affiche la fenêtre de niveau supérieur pour la sortie de l' [exemple d’accessibilité XAML](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) , s’exécutant en tant qu’application sur le même ordinateur. Cette capture d’écran montre le mode par défaut des éléments de **contrôle feuille** et la valeur **visuelle** pour la **disposition**.

![Capture d’écran de la visualisation AccScope](images/accscopescreenshot.png)

Notez que cette visualisation représente les contrôles dans l’espace de coordonnées approximatifs que vous pouvez voir dans l’application. Mais au lieu de vous montrer les visuels XAML, ou le texte complet des contrôles de texte, il affiche les valeurs de propriété de **nom** qui proviennent de chaque élément de contrôle, à l’aide d’UI Automation.

Outre les options de menu décrites précédemment, vous pouvez également utiliser ces techniques :

- Cliquez sur le rectangle d’un élément dans visualisations **visuelles** ou **liste** pour afficher une fenêtre contextuelle des **Propriétés de UIA** . Cette liste répertorie un certain nombre de propriétés d’Automation d’interface utilisateur importantes pour cet élément, notamment certaines propriétés [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) standard et d’autres informations telles que les valeurs Aria et une **Description du fournisseur**.
- Cliquez avec le bouton droit sur le rectangle d’un élément dans les visualisations **visuelles** ou de **liste** pour afficher un menu contextuel pour l’exercice des modèles pris en charge par l’élément. Par exemple, si un élément prend en charge [**InvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern), le menu contextuel contient un élément pour **Invoke**. Sélectionnez cet élément et l’API de modèle appropriée est testée dans l’application correspondante. **AccScope** prend en charge cette fonctionnalité pour les modèles suivants : **Invoke**, **ExpandCollapse**, **Toggle**, **SelectionItem**, **ScrollItem**.
- Ajustez le curseur de **transparence** pour modifier l’opacité/la transparence de la fenêtre **AccScope** . Par défaut, il est affiché sous la forme d’une opacité de 100%. Rendre la fenêtre partiellement transparente peut être utile pour afficher les parties de la fenêtre cible via l’interface utilisateur **AccScope** tout en utilisant le mode **supérieur Always on** .
- S’ils sont affichés, utilisez les barres de défilement horizontale et verticale pour modifier le centre d’affichage de la visualisation. Cela est utile si vous utilisez l’option de disposition **visuelle** , mais pas l’option d’affichage **plein écran** , tout en laissant la fenêtre **AccScope** petite en comparaison avec la fenêtre cible.

## <a name="testing-the-narrator-scenario"></a>Test du scénario du narrateur

Le scénario du narrateur est l’aspect le plus important à tester lors de l’utilisation de **AccScope**, qui est spécifiquement conçu pour visualiser le fonctionnement de la navigation des éléments du narrateur de base lorsqu’il est appliqué à votre application.

Pour tester le scénario du narrateur, utilisez les options de configuration **AccScope** suivantes :

- **Mode d’élément**: **narrateur**
- **Disposition**: **visuel**
- Options de **disposition** : **afficher l’info-bulle** et **afficher les nombres** les deux sélectionnés

Voici quelques aspects spécifiques de votre application pour tester le scénario du narrateur :

- **Ordre des éléments :** Vérifiez que l’ordre dans lequel le narrateur lit vos contrôles est exact, en fonction des chiffres (cercles verts) affichés dans les visualisations. Si les éléments ne sont pas dans l’ordre attendu pour la lecture, modifiez la structure de l’interface utilisateur de l’application et l’arborescence UI Automation obtenue, puis effectuez un test à nouveau jusqu’à ce que vous ayez vérifié que vos éléments se trouvent dans l’ordre de lecture attendu.
- **Texte parlé :** Déplacez la souris dans la visualisation et pointez sur chacun des rectangles d’élément pour afficher les info-bulles pour chaque élément. En mode narrateur, les info-bulles affichent une entrée de **texte narrateur** qui est littéralement le texte que le narrateur lit. En général, ce texte est composé du **nom** et du **type de contrôle**. Vérifiez qu’il s’agit des bonnes informations pour chaque contrôle de votre interface utilisateur. Si des informations sont incorrectes, modifiez les propriétés UI Automation via les techniques activées par votre infrastructure d’interface utilisateur particulière pour ce faire. (Si **le type de contrôle** est inattendu, vous devrez peut-être utiliser un autre contrôle, car il est souvent exclusivement contrôlé par les implémentations de contrôle de l’infrastructure d’interface utilisateur.) Ensuite, testez à nouveau et vérifiez que le **texte du narrateur** est correct.
- **Disposition des éléments :** Vérifiez chacun des cas suivants :
    - Vérifiez que les éléments redondants ne sont pas exposés par Narrator. un exemple d’élément redondant est le contrôle d’évaluation de chaque élément de mosaïque Windows Store.
    - Vérifiez que les éléments importants (éléments dont l’utilisateur a besoin pour accomplir les tâches clés dans l’application) s’affichent dans la navigation des éléments du narrateur.
    - Si vous utilisez la disposition **visuelle** et qu’un élément est manquant parce que les contrôles se chevauchent, basculez en mode **liste** pour voir la séquence que le narrateur signale.
    - Vérifiez que la structure de l’arborescence UI Automation est précise et attendue pour votre application.

## <a name="related-topics"></a>Rubriques connexes

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Outils de test](testing-tools.md)
- [Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
- [UI Automation Verify](ui-automation-verify.md)
- [Accessibilité Microsoft](https://www.microsoft.com/accessibility/)
