---
title: Prise en charge d'UI Automation pour les contrôles standard
description: cette rubrique identifie les contrôles de Windows standard pris en charge par Microsoft UI Automation. la prise en charge complète est fournie uniquement pour les contrôles de la version 6 de ComCtrl32.dll (disponible avec Windows XP et versions ultérieures).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- clients, prise en charge d’UI Automation pour les contrôles standard
- clients, prise en charge du contrôle standard
- clients, contrôles Win32
- UI Automation, prise en charge des contrôles standard
- UI Automation, prise en charge du contrôle standard
- UI Automation, contrôles Win32
- prise en charge pour les contrôles
- prise en charge du contrôle standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403490"
---
# <a name="ui-automation-support-for-standard-controls"></a>Prise en charge d'UI Automation pour les contrôles standard

cette rubrique identifie les contrôles de Windows standard pris en charge par Microsoft UI Automation. la prise en charge complète est fournie uniquement pour les contrôles de la version 6 de ComCtrl32.dll (disponible avec Windows XP et versions ultérieures).

> [!Note]  
> le contrôle RichEdit est pris en charge uniquement pour les versions fournies avec Windows Vista (dans RichEd20.dll version 3,1 et ultérieure, et MsftEdit.dll version 4,1 et versions ultérieures).

 

Le tableau suivant répertorie les noms de classes des contrôles standard pris en charge, ainsi que les types de contrôle UI Automation correspondants.



| Nom de la classe          | Type de contrôle        |
|---------------------|---------------------|
| Button              | Button              |
| Button              | RadioButton         |
| Bouton              | Group               |
| Bouton              | CheckBox            |
| Bouton              | Hyperlink           |
| Bouton              | SplitButton         |
| Bouton              | CheckBox            |
| ComboBoxEx32        | ComboBox            |
| ComboBox            | ComboBox            |
| Modifier                | Document            |
| Modifier                | Modifier                |
| SysLink             | Hyperlink           |
| statique              | Texte                |
| statique              | Image               |
| SysIPAddress32      | Custom              |
| SysHeader32         | Header/HeaderItem   |
| SysListView32       | DataGrid            |
| SysListView32       | List                |
| ListBox             | List                |
| ListBox             | ListItem            |
| \#32768             | Menu                |
| \#32768             | MenuItem            |
| msctls \_ progress32  | ProgressBar         |
| RichEdit            | Document. Consultez la remarque. |
| RichEdit20A         | Document            |
| RichEdit20W         | Document            |
| RichEdit50W         | Document            |
| ScrollBar           | Curseur              |
| msctls \_ trackbar32  | Curseur              |
| msctls \_ updown32    | Spinner             |
| msctls \_ statusbar32 | StatusBar           |
| SysTabControl32     | Onglet                 |
| SysTabControl32     | TabItem             |
| ToolbarWindow32     | ToolBar             |
| ToolbarWindow32     | MenuItem            |
| ToolbarWindow32     | Bouton              |
| ToolbarWindow32     | CheckBox            |
| ToolbarWindow32     | RadioButton         |
| ToolbarWindow32     | Séparateur           |
| info-bulles \_ Class32   | Info-bulle             |
| \#32774             | Info-bulle             |
| ReBarWindow32       | Barre d’outils             |
| SysTreeView32       | Arborescence                |
| SysTreeView32       | TreeItem            |



 

Les contrôles répertoriés dans le tableau suivant ne sont pas pris en charge.



| Nom de la classe                                    | Type de contrôle |
|-----------------------------------------------|--------------|
| SysAnimate32                                  | Image        |
| SysPager                                      | Spinner      |
| SysDateTimePick32                             | Custom       |
| SysMonthCal32                                 | Calendrier     |
| MS \_ WINNOTE                                   | Info-bulle      |
| VBBubble                                      | Info-bulle      |
| ScrollBar (quand il est utilisé comme contrôle autonome) | Curseur       |
| SuperGrid                                     | Custom       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




