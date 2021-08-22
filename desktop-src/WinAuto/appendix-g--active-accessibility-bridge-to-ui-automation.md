---
title: Annexe G Active Accessibility Bridge à UI Automation
description: Cette annexe contient des informations sur Microsoft Active Accessibility Bridge.
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14991f869706a16c4def8fdaf49ae255e3ddf413eec416cefd1e151ee470cc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052967"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>Annexe G : Active Accessibility Bridge à UI Automation

Cette annexe contient des informations sur Microsoft Active Accessibility Bridge. Le pont Active Accessibility permet aux applications qui implémentent Microsoft Active Accessibility d’accéder aux applications qui implémentent l’automatisation de l’interface utilisateur de Microsoft. en utilisant conjointement microsoft Active Accessibility et UI Automation, les clients basés sur Active Accessibility microsoft, tels qu’un screenreader sur Windows XP, peuvent interagir par programmation avec les fournisseurs ui automation, tels qu’une application Windows Presentation Foundation (WPF). Il fait partie de l’API de base native d’UI Automation (UIAutomationCore.dll).

Le pont Active Accessibility mappe les propriétés et les événements UI Automation à ceux de Microsoft Active Accessibility. Les tableaux suivants mappent les méthodes et propriétés de l’interface Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à UI Automation. Utilisez ces tableaux pour déterminer les pratiques de codage appropriées pour le développement de votre client Microsoft Active Accessibility.

### <a name="navigation-and-hierarchy-properties"></a>Propriétés de navigation et de hiérarchie



| IAccessible, propriété                                                     | Propriété UI Automation          |
|--------------------------------------------------------------------------|---------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Non implémenté                 |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Dérivé de l’arborescence UI Automation |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Dérivé de l’arborescence UI Automation |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | Non implémenté                 |



 

### <a name="descriptive-properties-and-methods"></a>Propriétés et méthodes descriptives



| IAccessible                                                                          | Automatisation de l’interface utilisateur                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | Pour plus d’informations, consultez les types de contrôle et la table accRole.                                                                                                                                                                                                                                                                     |
| [**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Pour plus d’informations, consultez les types de contrôle et la table accRole.                                                                                                                                                                                                                                                                     |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | AccessKeyPropertyor AcceleratorKeyProperty; Si les deux sont présents, AccessKeyProperty est prioritaire.                                                                                                                                                                                                                         |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | NameProperty                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | ControlTypeProperty. Pour plus d’informations, consultez les types de contrôle et la table accRole.                                                                                                                                                                                                                                                |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Pour plus d’informations, consultez les types de contrôle et la table accRole.                                                                                                                                                                                                                                                                     |
| [**Obtient \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | ValueProperty pris en charge sur les types de contrôle qui prennent en charge le modèle de contrôle [value](uiauto-implementingvalue.md) ou modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) . Les valeurs RangeValue sont cohérentes avec le comportement de Microsoft Active Accessibility (0 à 100). Les éléments de valeur utilisent une chaîne. |
| [**put \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | ValueProperty pris en charge sur les types de contrôle qui prennent en charge le modèle de contrôle [value](uiauto-implementingvalue.md) ou le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md)                                                                                                                                      |
| [**Obtient \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | HelpTextProperty                                                                                                                                                                                                                                                                                                         |
| [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Non implémenté                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | Non implémenté                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>Types de contrôles et accRole

Le rôle par défaut de Microsoft Active Accessibility est [**\_ \_ client du système de rôle**](object-roles.md). Si aucune action par défaut n’est trouvée pour un type de contrôle, le pont Active Accessibility utilise également les modèles de contrôle disponibles suivants : [Invoke](uiauto-implementinginvoke.md), [ExpandCollapse](uiauto-implementingexpandcollapse.md)et [Toggle](uiauto-implementingtoggle.md). Par exemple, un contrôle GroupBox n’a pas d’action par défaut. S’il prend en charge ExpandCollapse, le pont Active Accessibility l’utilise pour l’action par défaut.



| Type de contrôle UI Automation                              | accRole                                                                     | Action par défaut                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [Button](uiauto-supportbuttoncontroltype.md)           | [**\_PUSHBUTTON système de rôle \_**](object-roles.md)     | Appuyez sur                                                    |
| [Calendrier](uiauto-supportcalendarcontroltype.md)       | [**\_client du système de rôle \_**](object-roles.md)             | Aucun                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**système de rôle \_ \_ CHECKBUTTON**](object-roles.md)   | Cochez/décochez (bascule)                                   |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**\_ComboBox système de rôle \_**](object-roles.md)         | Aucun                                                     |
| Custom                                                  | [**\_client du système de rôle \_**](object-roles.md)             | Aucun                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**\_liste des systèmes de rôles \_**](object-roles.md)                 | Aucun                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**\_ListItem du système de rôle \_**](object-roles.md)         | Aucun                                                     |
| [Document](uiauto-supportdocumentcontroltype.md)       | [**\_document système de rôle \_**](object-roles.md)         | Aucun                                                     |
| [Modifier](uiauto-supporteditcontroltype.md)               | [**\_texte du système de rôle \_**](object-roles.md)                 | Aucun                                                     |
| [Groupe](uiauto-supportgroupcontroltype.md)             | [**\_regroupement du système de rôle \_**](object-roles.md)         | Aucun                                                     |
| [En-tête](uiauto-supportheadercontroltype.md)           | [**\_liste des systèmes de rôles \_**](object-roles.md)                 | Aucun                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**système de rôle \_ \_ COLUMNHEADER**](object-roles.md) | Cliquez sur                                                    |
| [Lien hypertexte](uiauto-supporthyperlinkcontroltype.md)     | [**\_lien système de rôle \_**](object-roles.md)                 | Jump (mappe à Invoke)                                    |
| [Image](uiauto-supportimagecontroltype.md)             | [**\_graphique du système de rôle \_**](object-roles.md)           | Aucun                                                     |
| [Liste](uiauto-supportlistcontroltype.md)               | [**\_liste des systèmes de rôles \_**](object-roles.md)                 | Aucun                                                     |
| [ListItem](uiauto-supportlistitemcontroltype.md)       | [**\_ListItem du système de rôle \_**](object-roles.md)         | Double-clic                                             |
| [Menu](uiauto-supportmenucontroltype.md)               | [**système de rôle \_ \_ MENUPOPUP**](object-roles.md)       | Aucun                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**barre de menus du \_ système de rôle \_**](object-roles.md)           | Aucun                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**système de rôle \_ \_ MenuItem**](object-roles.md)         | Exécuter ou ouvrir/fermer pour les éléments de menu qui ont des enfants. |
| [Volet](uiauto-supportpanecontroltype.md)               | [**\_volet système de rôle \_**](object-roles.md)                 | Aucun                                                     |
| [ProgressBar](uiauto-supportprogressbarcontroltype.md) | [**\_PROGRESSBAR du système de rôle \_**](object-roles.md)   | Aucun                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**RadioButton du système de rôle \_ \_**](object-roles.md)   | Vérification                                                    |
| [ScrollBar](uiauto-supportscrollbarcontroltype.md)     | [**\_ScrollBar système de rôle \_**](object-roles.md)       | Aucun                                                     |
| [Curseur](uiauto-supportslidercontroltype.md)           | [**\_curseur système de rôle \_**](object-roles.md)             | Aucun                                                     |
| [Spinner](uiauto-supportspinnercontroltype.md)         | [**\_SPINBUTTON du système de rôle \_**](object-roles.md)     | Aucun                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**système de rôle \_ \_ SPLITBUTTON**](object-roles.md)   | Aucun                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**\_STATUSBAR du système de rôle \_**](object-roles.md)       | Aucun                                                     |
| [Tab](uiauto-supporttabcontroltype.md)                 | [**système de rôle \_ \_ PAGETABLIST**](object-roles.md)   | Aucun                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**système de rôle \_ \_ PAGETAB**](object-roles.md)           | Commutateur                                                   |
| [Table](uiauto-supporttablecontroltype.md)             | [**\_table système des rôles \_**](object-roles.md)               | Aucun                                                     |
| [Text](uiauto-supporttextcontroltype.md)               | [**système de rôle \_ \_ STATICTEXT**](object-roles.md)     | Aucun                                                     |
| [Flash](uiauto-supportthumbcontroltype.md)             | [**\_indicateur de système de rôle \_**](object-roles.md)       | Aucun                                                     |
| [Spreadsheet](uiauto-supporttitlebarcontroltype.md)       | [**\_TITLEBAR système de rôle \_**](object-roles.md)         | Aucun                                                     |
| [Barre](uiauto-supporttoolbarcontroltype.md)         | [**\_ \_ barre d’outils système de rôle**](object-roles.md)           | Aucun                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**\_ \_ info-bulle du système de rôle**](object-roles.md)           | Aucun                                                     |
| [Arbres](uiauto-supporttreecontroltype.md)               | [**\_structure du système de rôle \_**](object-roles.md)           | Aucun                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**système de rôle \_ \_ OUTLINEITEM**](object-roles.md)   | Développer ou réduire                                       |
| [Window](uiauto-supportwindowcontroltype.md)           | [**\_fenêtre système de rôle \_**](object-roles.md)             | Aucun                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>Propriétés UI Automation et accState



| accState                                                                                      | Propriété UI Automation                                                                                                                                                        | Changement d’état des déclencheurs |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**système d’état \_ \_ vérifié**](object-state-constants.md)                 | Pour ControlType = "checkbox", utilisez ToggleState. on. Pour « RadioButton », utilisez [ **SelectionItemPattern :: IsSelected**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Oui                   |
| [**système d’État pouvant être \_ \_ actif**](object-state-constants.md)             | IsKeyboardFocusableProperty                                                                                                                                                   | Non                    |
| [**système d’état \_ \_ concentré**](object-state-constants.md)                 | HasKeyboardFocusProperty                                                                                                                                                      | Non                    |
| [**système d’état \_ \_ protégé**](object-state-constants.md)             | IsPasswordProperty                                                                                                                                                            | Non                    |
| [**système d’État en \_ \_ lecture seule**](object-state-constants.md)               | IsReadOnlyProperty (modèle de contrôle de valeur et modèle de contrôle RangeValue)                                                                                                     | Non                    |
| [**système d’état \_ \_ non disponible**](object-state-constants.md)         | IsEnabledProperty                                                                                                                                                             | Oui                   |
| [**système d’état \_ \_ lié**](object-state-constants.md)                   | ControlTypeProperty = "lien hypertexte"                                                                                                                                             | Non                    |
| [**système d’état \_ \_ sélectionnable**](object-state-constants.md)           | SelectionItemPattern est pris en charge                                                                                                                                             | Non                    |
| [**système d’état \_ \_ sélectionné**](object-state-constants.md)               | IsSelectedProperty (modèle de contrôle SelectionItem)                                                                                                                            | Non                    |
| [**système d’état \_ \_ réduit**](object-state-constants.md)             | ExpandCollapseState = réduit                                                                                                                                               | Oui                   |
| [**système d’état \_ \_ développé**](object-state-constants.md)               | ExpandCollapseState = Expanded ou PartiallyExpanded                                                                                                                           | Oui                   |
| [**\_HASPOPUP système d’état \_**](object-state-constants.md)               | Éléments de menu qui prennent en charge développer/réduire                                                                                                                                       | Non                    |
| [**système d’état \_ \_ mixte**](object-state-constants.md)                     | ToggleState = indéterminé                                                                                                                                                   | Non                    |
| [**système d’état \_ \_ dimensionnable**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanResize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | Non                    |
| [**système d’état \_ \_ mobile**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanMove**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | Non                    |
| [**système d’état \_ \_ multisélectionnable**](object-state-constants.md) | [**IUIAutomationSelectionPattern::CanSelectMultiple**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | Non                    |



 

### <a name="selection-and-focus"></a>Sélection et Focus



| IAccessible                                                            | Automatisation de l’interface utilisateur                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**IUIAutomation :: FocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | Pour plus d’informations, consultez les propriétés UI Automation et le tableau accSelect SELFLAGs.             |
| [**Obtient \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**SelectionPattern :: GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>Propriétés UI Automation et accSelect SELFLAGs



| accSelect SELFLAGs                                                  | Propriété UI Automation                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**SELFLAG \_ aucun**](selflag.md)                       | Non disponible                                                                                                                  |
| SELFLAG \_ TAKFOCUS                                                   | [**IUIAutomationElement :: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**SELFLAG \_ TAKESELECTION**](selflag.md)     | [**IUIAutomationSelectionItemPattern :: SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**SELFLAG \_ ADDSELECTION**](selflag.md)       | [**IUIAutomationSelectionItemPattern::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| SELFLAG \_ TAKEREMOVESELECTION                                        | [**IUIAutomationSelectionItemPattern::RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**SELFLAG \_ EXTENDSELECTION**](selflag.md) | Non disponible                                                                                                                  |



 

### <a name="spatial-mapping"></a>Mappage spatial



| IAccessible                                                 | Automatisation de l’interface utilisateur                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | BoundingRectangleProperty                                                                                                            |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**IRawElementProviderFragmentRoot::ElementProviderFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>Événements



| System-Level les constantes d’événement                                                             | Automatisation de l’interface utilisateur                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**\_MENUPOPUPSTART du système d’événements \_**](event-constants.md)     | [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) (Remarque : doit vérifier s’il s’agit d’une fenêtre indépendante.) |
| [**\_MENUPOPUPEND du système d’événements \_**](event-constants.md)         | [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                |
| [**\_MENUSTART du système d’événements \_**](event-constants.md)               | [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md)                                          |
| [**\_MENUEND du système d’événements \_**](event-constants.md)                   | [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md)                                              |
| [**\_son du système d’événements \_**](event-constants.md)                       |                                                                                                                         |
| [**\_alerte du système d’événements \_**](event-constants.md)                       |                                                                                                                         |
| [**\_CAPTURESTART du système d’événements \_**](event-constants.md)         |                                                                                                                         |
| [**\_CAPTUREEND du système d’événements \_**](event-constants.md)             |                                                                                                                         |
| [**\_DIALOGSTART du système d’événements \_**](event-constants.md)           |                                                                                                                         |
| [**\_DIALOGEND du système d’événements \_**](event-constants.md)               |                                                                                                                         |
| [**\_MOVESIZESTART du système d’événements \_**](event-constants.md)       |                                                                                                                         |
| [**\_MOVESIZEEND du système d’événements \_**](event-constants.md)           |                                                                                                                         |
| [**\_CONTEXTHELPSTART du système d’événements \_**](event-constants.md) |                                                                                                                         |
| [**\_CONTEXTHELPEND du système d’événements \_**](event-constants.md)     | Non pertinent                                                                                                            |
| [**\_DRAGDROPSTART du système d’événements \_**](event-constants.md)       |                                                                                                                         |
| [**\_DRAGDROPEND du système d’événements \_**](event-constants.md)           |                                                                                                                         |
| [**\_SWITCHSTART du système d’événements \_**](event-constants.md)           | Non pertinent                                                                                                            |
| [**\_SWITCHEND du système d’événements \_**](event-constants.md)               | Non pertinent                                                                                                            |
| [**\_MINIMIZESTART du système d’événements \_**](event-constants.md)       |                                                                                                                         |
| [**\_MINIMIZEEND du système d’événements \_**](event-constants.md)           |                                                                                                                         |
| [**\_premier plan du système d’événements \_**](event-constants.md)             |                                                                                                                         |
| [**\_SCROLLINGSTART du système d’événements \_**](event-constants.md)     | Non disponible                                                                                                           |
| [**\_SCROLLINGEND du système d’événements \_**](event-constants.md)         | Non disponible                                                                                                           |



 



| Object-Level les constantes d’événement                                                           | Automatisation de l’interface utilisateur                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**Focus de l' \_ objet événement \_**](event-constants.md)                     | AutomationFocusChangedEvent                                                            |
| [**VALUECHANGE de l’objet d’événement \_ \_**](event-constants.md)         | ValueProperty (modèle de contrôle de valeur et modèle de contrôle RangeValue)                   |
| [**sélection de l’objet d’événement \_ \_**](event-constants.md)             | ElementSelectedEvent (modèle de contrôle SelectionItem)                                   |
| [**SELECTIONADD de l’objet d’événement \_ \_**](event-constants.md)       | ElementAddedToSelectionEvent (modèle de contrôle SelectionItem)                           |
| [**SELECTIONREMOVE de l’objet d’événement \_ \_**](event-constants.md) | ElementRemovedFromSelectionEvent                                                       |
| [**SELECTIONWITHIN de l’objet d’événement \_ \_**](event-constants.md) | EventsSelectionInvalidatedEvent                                                        |
| [**EVENT, \_ objet \_ STATECHANGE**](event-constants.md)         | Voir les propriétés UI Automation et la table accState pour les États qui déclenchent un changement d’État |



 

 

 




