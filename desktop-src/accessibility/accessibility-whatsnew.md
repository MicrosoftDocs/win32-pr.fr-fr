---
description: décrit les innovations récentes et les mises à jour apportées aux fonctionnalités d’accessibilité, aux outils, à la documentation et aux exemples de Windows.
title: nouveautés de Windows accessibilité pour les développeurs
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 6cffebe307b06aceb506e8576e2a9c99c395c1257f575c6be3757a9426df2459
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954479"
---
# <a name="new-windows-accessibility-features-tools-documentation-and-samples-for-developers"></a>Windows nouvelles fonctionnalités d’accessibilité, outils, documentation et exemples pour les développeurs

la plate-forme Windows est constamment mise à jour avec de nouvelles fonctionnalités d’accessibilité et d’automatisation pour les développeurs.

[installez les outils et le kit de développement logiciel (SDK)](https://developer.microsoft.com/windows/downloads/#_blank) sur Windows 10 et vous êtes prêt à créer une application de Windows universelle ou à découvrir comment vous pouvez utiliser votre code d’application existant sur Windows.

pour plus d’informations sur les outils les plus récents disponibles pour tester l’implémentation de l’accessibilité de vos applications web et Windows, consultez [test de l’accessibilité](accessibility-testwithuia.md).

## <a name="whats-new-for-windows-10-may-2019-update-version-1903"></a>nouveautés de Mise à jour de mai 2019 de Windows 10 (Version 1903)

les fonctionnalités, outils, conseils pour les développeurs, exemples et vidéos suivants ont été mis à disposition pour le [Mise à jour de mai 2019 de Windows 10](https://blogs.windows.com/windowsexperience/2019/04/08/releasing-the-may-2019-update-to-the-release-preview-ring/#oTrOrMWFFgWJuCqO.97).

| Libérer | Plateforme | Fonctionnalité | Description | Lien |
| --- | --- | --- | --- | --- |
| 1903 | Win32 | UI Automation prend en charge IAccessible2 | Les clients UI Automation peuvent désormais accéder en toute transparence aux informations des fournisseurs IAccessible2 tels que le navigateur Chrome. | n/a |
| 1903 | UWP | Visibilité de la barre de défilement  | Les barres de défilement sont masquées automatiquement lorsqu’elles ne sont pas en interaction avec. | [UISettings. AutoHideScrollBars, propriété](/uwp/api/windows.ui.viewmanagement.uisettings.autohidescrollbars) |
| 1903 | Win32 | UI Automation prend en charge le balisage structuré | Prévu, mais non limité à, l’analyse MathML. | n/a |

## <a name="whats-new-for-windows-10-october-2018-update-version-1809"></a>nouveautés de Mise à jour d’octobre 2018 de Windows 10 (Version 1809)

les fonctionnalités, outils, conseils pour les développeurs, exemples et vidéos suivants ont été mis à disposition pour le [Mise à jour d’octobre 2018 de Windows 10](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/#R6DJStjqlIkK34BT.97).

| Libérer | Plateforme | Fonctionnalité | Description | Lien |
| --- | --- | --- | --- | --- |
| 1809 | Win32 | UI Automation prend en charge les événements de modification de position de texte active | Les fournisseurs UI Automation peuvent définir explicitement une position de départ dans une plage de texte. Les clients peuvent ensuite transmettre cette position à un utilisateur. Par exemple, si un utilisateur clique sur un lien vers une ancre sur la même page (un lien de signet), le nouvel emplacement est fourni au à. | [Interface IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | UI Automation prend en charge la fusion d’événements | Améliore les performances en tentant de détecter, de filtrer et d’ignorer les événements de recherche en continu MSAA et UIA séquentiels en double déclenchés par certains fournisseurs. | [Interface IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | UI Automation prend en charge le comportement de récupération de connexion | Les messages d’un client UI Automation à un fournisseur sont suspendus (par défaut, deux secondes) si le fournisseur ne répond pas. Cela réduit la fréquence des délais d’attente étendus et minimise l’inondation d’un fournisseur non réactif avec des événements et des demandes. | [Interface IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | UWP | Services de lecture d’écran améliorés | SUR les clients, vous connaissez l’emplacement audible de lecture d’écran (contrôle ou contenu) et le mode de lecture. | [ScreenReaderService, classe](/uwp/api/windows.ui.accessibility.screenreaderservice) |
| 1809 | Win32, UWP | UI Automation prend en charge les fenêtres de boîte de dialogue | Les fournisseurs UI Automation peuvent marquer des éléments UIA spécifiquement comme des fenêtres de boîte de dialogue. L’ATs présente souvent des dialogues de manière différente pour les utilisateurs.  | [IUIAutomationElement9](https://review.docs.microsoft.com/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/><br/>[ContentDialog, classe](/uwp/api/windows.ui.xaml.controls.contentdialog) |
| 1809 |  UWP | Mise à l’échelle du texte  | Met à l’échelle la taille du texte dans les applications et les pages Web. | [Événement UISettings. TextScaleFactorChanged](/uwp/api/windows.ui.viewmanagement.uisettings.textscalefactorchanged)<br/><br/>[Mise à l’échelle du texte](/windows/uwp/design/input/text-scaling) |
