---
title: Outils d’accessibilité-AccEvent (Observateur d’événements accessible)
description: AccEvent (Observateur d’événements accessible) permet aux développeurs et aux testeurs de valider que les éléments d’interface utilisateur d’une application déclenchent des événements Microsoft UI Automation et Microsoft Active Accessibility appropriés lorsque des modifications de l’interface utilisateur se produisent.
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e6fa4896c0cfe3155536537099b1c00af8ebe5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010728"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a>Outils d’accessibilité-AccEvent (Observateur d’événements accessible)

**AccEvent (Observateur d’événements accessible)** permet aux développeurs et aux testeurs de valider que les éléments d’interface utilisateur d’une application déclenchent des événements Microsoft UI Automation et Microsoft Active Accessibility appropriés lorsque des modifications de l’interface utilisateur se produisent. Les modifications apportées à l’interface utilisateur peuvent se produire lorsque le focus est modifié ou lorsqu’un élément d’interface utilisateur est appelé, sélectionné ou a une modification d’État ou de propriété.

**AccEvent** est installé avec le kit de développement logiciel (SDK) Windows. Il se trouve dans le \\ dossier bin \\ < *version* > \\ < *Platform*> du chemin d’installation du kit de développement logiciel (Accevent.exe).

> [!NOTE]
> **AccEvent** est un outil hérité. nous vous recommandons d’utiliser à la place l' [accessibilité Informations](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Spécifications

**AccEvent** peut être utilisé pour examiner les données d’accessibilité sur les systèmes qui n’ont pas d’automatisation d’interface utilisateur, ils ont été écrits à l’origine pour Microsoft Active Accessibility. Pour examiner l’Automation d’interface utilisateur, UI Automation doit être présent sur le système. Pour plus d’informations, consultez la section « Configuration requise » d' [UI Automation](entry-uiauto-win32.md).

**AccEvent** est installé dans le cadre de l’ensemble d’outils de la SDK Windows, il n’est pas distribué en tant que téléchargement de fichier exécutable distinct. le SDK Windows comprend tous les outils liés à l’accessibilité documentés dans cette section. [obtient le SDK Windows.](https://developer.microsoft.com/) (Il existe également un kit de développement logiciel (SDK) à partir de cette page, si vous avez besoin d’une version précédente.)

Pour exécuter **AccEvent**, recherchez AccEvent.exe dans le \\ dossier bin \\ < *version* > \\ < *Platform*> et exécutez-le (vous n’êtes généralement pas obligé d’exécuter en tant qu’administrateur).

## <a name="the-accessible-event-watcher-window"></a>Fenêtre Observateur d’événements accessible

Lorsque vous lancez **AccEvent**, la fenêtre principale s’affiche. La fenêtre principale **AccEvent** affiche les événements UI Automation ou Microsoft Active Accessibility déclenchés par les applications en cours d’exécution. La fenêtre principale contient les éléments principaux suivants :

- Barre de titre. Affiche le mode d’opération et l’État actuels.
- Barre de menus. Fournit l’accès à la fonctionnalité **AccEvent** .
- Vue de données. Affiche des informations sur chaque événement, y compris l’ID d’événement et les propriétés sélectionnées de l’élément d’interface utilisateur qui a déclenché l’événement.

**AccEvent** a une interface utilisateur graphique uniquement ; Il n’y a pas d’arguments de ligne de commande pour cet outil, mais vous pouvez utiliser d’autres outils pour traiter le journal de sortie en tant que texte.

L’illustration suivante montre la fenêtre principale de **AccEvent** .

![interface utilisateur de l’outil observateur d’événements accessible](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a>Tâches d’observateur d’événements accessibles

Cette section contient des informations sur les tâches **AccEvent** couramment utilisées.

### <a name="configuring-the-operating-mode"></a>Configuration du mode d’opération

Vous utilisez le menu **mode** pour configurer le mode d’opération **AccEvent** et sélectionner des paramètres qui contrôlent le comportement de l’outil. Vous pouvez sélectionner les options suivantes.



| Lorsque cette option est sélectionnée | **AccEvent** effectue cette                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toujours visible                | Apparaît en haut de toute autre interface utilisateur à l’écran.                                                                                                                                                                                    |
| Événements UIA                   | Affiche des informations sur les événements UI Automation.                                                                                                                                                                                             |
| WinEvents (en contexte)       | Affiche des informations sur les événements de Active Accessibility Microsoft (WinEvents) passés aux fonctions de raccordement qui résident dans l’espace d’adressage du serveur. Pour plus d’informations, consultez [fonctions de raccordement dans le contexte](in-context-hook-functions.md).         |
| WinEvents (hors contexte)   | Affiche des informations sur les événements de Active Accessibility Microsoft (WinEvents) passés aux fonctions de raccordement qui résident dans l’espace d’adressage du client. Pour plus d’informations, consultez [fonctions de raccordement hors contexte](out-of-context-hook-functions.md). |
| Afficher le rectangle de surbrillance     | Met en surbrillance un rectangle autour de l’élément d’interface utilisateur qui a déclenché l’événement sélectionné.                                                                                                                                                                 |
| Afficher l’info-bulle d’informations     | Affiche des informations d’événement dans une info-bulle.                                                                                                                                                                                                        |
| Paramètres                     | affiche la boîte de dialogue **Paramètres d’événements UIA** ou **Paramètres WinEvent** .                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a>Filtrage des événements UI Automation

pour configurer les événements UI Automation et les propriétés qui s’affichent dans la fenêtre **AccEvent** , cliquez sur le menu **Mode** , sélectionnez **UIA événements**, puis sélectionnez **Paramètres**. la boîte de dialogue **Paramètres d’événements UIA** s’affiche. Vous pouvez également utiliser cette boîte de dialogue pour filtrer les événements.

la boîte de dialogue **Paramètres d’événements UIA** contient les volets suivants :

- **Événements globaux**

    Activez la case à cocher **FocusChangedEvent** pour afficher des informations sur les événements de modification de focus globaux.

- **Type d'événement**

    Sélectionnez les événements qui vous intéressent.

- **Portée**

    Sélectionnez l’élément d’interface utilisateur auquel vous souhaitez que **AccEvent** écoute les événements.

- **Inclure les événements de**

    Sélectionnez **enfants immédiats** si vous souhaitez afficher les événements des éléments enfants immédiats de l’élément d’interface utilisateur sélectionné dans le volet **étendue** . Si vous souhaitez afficher les événements de tous les éléments descendants, sélectionnez **tous les descendants**.

- **Propriétés des états**

    Sélectionnez les propriétés que vous souhaitez afficher après chaque événement dans la fenêtre principale. Si l’option **afficher l’info-bulle d’informations** est sélectionnée dans le menu **mode** , les propriétés sélectionnées sont également affichées dans une info-bulle.

### <a name="filtering-active-accessibility-events"></a>Filtrage des événements de Active Accessibility

pour configurer les événements et propriétés Microsoft Active Accessibility qui s’affichent dans la fenêtre **AccEvent** , cliquez sur le menu **Mode** , sélectionnez **WinEvents (en contexte)** ou **WinEvents (hors contexte)**, puis sélectionnez **Paramètres**. la boîte de dialogue **WinEvent Paramètres** s’affiche. Vous pouvez également utiliser cette boîte de dialogue pour filtrer les événements.

la boîte de dialogue **WinEvent Paramètres** contient les volets suivants :

- **Objets**

    Sélectionnez les objets pour lesquels vous souhaitez que **AccEvent** écoute les événements. **AccEvent** peut écouter les événements provenant de fenêtres, du curseur ou du signe insertion. La **fenêtre** est sélectionnée par défaut.

- **Événements**

    Sélectionnez les événements qui vous intéressent. Tous les événements sont affichés par défaut.

- **Informations sur l’événement**

    Sélectionnez les informations que vous souhaitez afficher après le nom de chaque événement dans la fenêtre principale.

- **Propriétés des objets**

    Sélectionnez les propriétés que vous souhaitez afficher après chaque événement dans la fenêtre principale. Si l’option **afficher l’info-bulle d’informations** est sélectionnée dans le menu **mode** , les propriétés sélectionnées sont également affichées dans une info-bulle. Le **nom**, le **rôle** et l' **État** sont sélectionnés par défaut.

- **Filtrage**

    Sélectionnez l’une des cases d’option dans la section filtrage pour filtrer les événements déclenchés par les fenêtres spécifiées dans le champ **HWND** . La case d’option **ne pas filtrer** est sélectionnée par défaut.

    - Sélectionnez la case d’option **exclure** pour afficher uniquement les événements déclenchés à partir d’objets autres que les fenêtres spécifiées.
    - Sélectionnez la case d’option **inclure uniquement** et spécifiez un ou plusieurs descripteurs de fenêtre pour afficher uniquement les événements déclenchés à partir de ces fenêtres.
    - Activez la case à cocher **et les descendants** pour inclure les événements déclenchés par les descendants des fenêtres spécifiées.

- **Options**

    Sélectionnez l’une des options suivantes :

    

    | Lorsque cette option est sélectionnée                                  | **AccEvent** effectue cette                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Utiliser Invoke                                                    | Utilise [IDispatch :: Invoke](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) pour récupérer des propriétés d’objet au lieu d’utiliser des méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .                               |
    | Toujours recevoir l’objet (même si aucune propriété d’objet n’est sélectionnée)     | Récupère l’objet associé à l’événement, même si aucun élément n’est sélectionné dans le volet Propriétés de l’objet.                                                                                        |
    | Afficher la propriété par défaut (en plus des propriétés sélectionnées) | Affiche la propriété par défaut, le cas échéant, de l’objet associé à l’événement, ainsi que les éléments sélectionnés dans le volet Propriétés de l’objet.                                                      |
    | Afficher des informations sur les événements à partir de fenêtres invisibles/masquées       | Affiche les éléments sélectionnés dans le volet informations sur l’événement pour tous les objets, y compris ceux des fenêtres invisibles ou masquées.                                                                       |
    | Afficher les informations complètes sur les événements à partir de fenêtres invisibles/masquées  | Affiche les éléments sélectionnés dans le volet d’informations de l’événement, ainsi que les éléments sélectionnés (ou par défaut) dans le volet Propriétés de l’objet, pour tous les objets, y compris ceux des fenêtres invisibles ou masquées. |
    | DebugBreak à l’événement suivant                                      | Provoque l’exception d’un point d’arrêt dans le processus à l’origine de la WinEvent suivante. Cela indique au débogueur de gérer l’exception.                                                        |

### <a name="using-the-event-menu"></a>Utilisation du menu événement

Utilisez le menu **événement** pour effectuer les tâches suivantes :

| Lorsque cette option est sélectionnée | **AccEvent** effectue cette                                    |
|------------------------------|-------------------------------------------------------|
| Démarrer l’écoute              | Démarre l’affichage des informations sur les événements dans la vue de données. |
| Arrêter l’écoute               | Arrête l’affichage des informations sur les événements dans la vue de données.  |
| Effacer l’historique des événements          | Efface le contenu de la vue de données.                 |
| Sélectionner tous les événements            | Sélectionne tous les événements listés dans la vue de données.           |
| Copier les événements sélectionnés         | Copie les événements sélectionnés dans le presse-papiers.          |

### <a name="saving-active-accessibility-events"></a>Enregistrement des événements de Active Accessibility

Pour commencer l’enregistrement des événements dans un fichier texte, ouvrez le menu **fichier** et sélectionnez **Démarrer la journalisation dans un fichier**. **AccEvent** commence à écrire des événements dans le fichier spécifié jusqu’à ce que vous sélectionnez **arrêter la journalisation** dans le menu **fichier** . Le fichier texte peut être utile pour la résolution des problèmes et l’examen ultérieur des événements.

## <a name="related-topics"></a>Rubriques connexes

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Outils de test](testing-tools.md)
- [Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
- [Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
- [UI Automation Verify](ui-automation-verify.md)
- [WinEvents](winevents-infrastructure.md)