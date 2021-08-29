---
title: Vue d'ensemble des types de contrôle UI Automation
description: Les types de contrôle Microsoft UI Automation sont des propriétés qui servent d’identificateurs connus qui indiquent le type de contrôle représenté par un élément d’interface utilisateur particulier, tel qu’une zone de liste déroulante ou un bouton.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- UI Automation, vue d’ensemble des types de contrôle
- UI Automation, UIA_LocalizedControlTypePropertyId propriété
- types de contrôle, à propos de
- types de contrôle, conditions requises
- types de contrôle, conditions préalables
- types de contrôles, prédéfinis
- types de contrôles, propriété UIA_LocalizedControlTypePropertyId
- types de contrôles prédéfinis
- UIA_LocalizedControlTypePropertyId, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef59d46e8f0ad00d2613bcec43ee914c71c9edbc1c8501cd2a714df2b883f63f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795478"
---
# <a name="ui-automation-control-types-overview"></a>Vue d'ensemble des types de contrôle UI Automation

Les types de contrôle Microsoft UI Automation sont des propriétés qui servent d’identificateurs connus qui indiquent le type de contrôle représenté par un élément d’interface utilisateur particulier, tel qu’une zone de liste déroulante ou un bouton. Les applications clientes utilisent le type pour identifier les fonctionnalités d’un contrôle et pour déterminer comment interagir avec lui.

Cette rubrique contient les sections suivantes :

-   [Conditions requises pour le type de contrôle UI Automation](#ui-automation-control-type-requisites)
-   [Propriété LocalizedControlType](#the-localizedcontroltype-property)
-   [Types de contrôle UI Automation actuels](#current-ui-automation-control-types)
-   [Rubriques connexes](#related-topics)

## <a name="ui-automation-control-type-requisites"></a>Conditions requises pour le type de contrôle UI Automation

Chaque type de contrôle UI Automation possède un ensemble de conditions qui lui sont associées. Lorsqu’un fournisseur assigne un type de contrôle à un contrôle, le fournisseur doit s’assurer que le contrôle remplit toutes les conditions associées à ce type de contrôle. Les conditions sont les suivantes :

-   Modèles de contrôle UI Automation : chaque type de contrôle a un ensemble de modèles de contrôle que le contrôle doit prendre en charge, un jeu facultatif et un ensemble que le contrôle ne doit pas prendre en charge.
-   Valeurs de propriété UI Automation : chaque type de contrôle possède un jeu de propriétés que le contrôle doit prendre en charge.
-   Événements UI Automation : chaque type de contrôle possède un jeu d’événements que le contrôle doit prendre en charge.
-   Structure de l’arborescence UI Automation : chaque type de contrôle définit la façon dont le contrôle doit apparaître dans la structure de l’arborescence UI Automation.

Lorsqu’un contrôle répond aux conditions d’un type de contrôle particulier, la valeur de la propriété [**IUIAutomationElement :: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (ou [**IUIAutomationElement :: CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) indique ce type de contrôle.

Si votre contrôle ne répond pas aux spécifications d’un type de contrôle particulier, utilisez [**UIA \_ CUSTOMCONTROLTYPEID**](uiauto-controltype-ids.md) comme ID de type de contrôle et décrivez complètement le contrôle à l’aide des modèles de contrôle et des propriétés appropriés. Vous pouvez également définir la propriété [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) sur une chaîne qui décrit le mieux le type de votre contrôle.

## <a name="the-localizedcontroltype-property"></a>Propriété LocalizedControlType

Si vous utilisez un type de contrôle prédéfini pour décrire votre contrôle, utilisez la valeur par défaut pour la propriété [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) et autoriser UI Automation à fournir une chaîne localisée pour que les fournisseurs exposent correctement. Si vous ne pouvez pas utiliser un type de contrôle prédéfini pour décrire votre contrôle, définissez la propriété **UIA \_ LocalizedControlTypePropertyId** sur une chaîne localisée qui décrit avec précision le type de votre contrôle. La chaîne doit être concise, mais suffisamment précise qu’une technologie d’assistance comme un lecteur d’écran peut l’utiliser dans l’interface utilisateur pour informer l’utilisateur du type du contrôle.

## <a name="current-ui-automation-control-types"></a>Types de contrôle UI Automation actuels

Les rubriques suivantes décrivent les types de contrôle UI Automation. Pour chaque type de contrôle, la description comprend l’ensemble de conditions qu’un contrôle du type donné doit prendre en charge :

-   Type de contrôle AppBar
-   [Button (type de contrôle)](uiauto-supportbuttoncontroltype.md)
-   [Calendar (type de contrôle)](uiauto-supportcalendarcontroltype.md)
-   [CheckBox (type de contrôle)](uiauto-supportcheckboxcontroltype.md)
-   [ComboBox (type de contrôle)](uiauto-supportcomboboxcontroltype.md)
-   [DataGrid (type de contrôle)](uiauto-supportdatagridcontroltype.md)
-   [DataItem (type de contrôle)](uiauto-supportdataitemcontroltype.md)
-   [Document (type de contrôle)](uiauto-supportdocumentcontroltype.md)
-   [Modifier le type de contrôle](uiauto-supporteditcontroltype.md)
-   [Group (type de contrôle)](uiauto-supportgroupcontroltype.md)
-   [Header (type de contrôle)](uiauto-supportheadercontroltype.md)
-   [Type de contrôle HeaderItem](uiauto-supportheaderitemcontroltype.md)
-   [HYPERLINK (type de contrôle)](uiauto-supporthyperlinkcontroltype.md)
-   [Image (type de contrôle)](uiauto-supportimagecontroltype.md)
-   [List (type de contrôle)](uiauto-supportlistcontroltype.md)
-   [ListItem (type de contrôle)](uiauto-supportlistitemcontroltype.md)
-   [Menu (type de contrôle)](uiauto-supportmenucontroltype.md)
-   [BarreMenus (type de contrôle)](uiauto-supportmenubarcontroltype.md)
-   [MenuItem (type de contrôle)](uiauto-supportmenuitemcontroltype.md)
-   [Pane (type de contrôle)](uiauto-supportpanecontroltype.md)
-   [ProgressBar (type de contrôle)](uiauto-supportprogressbarcontroltype.md)
-   [RadioButton (type de contrôle)](uiauto-supportradiobuttoncontroltype.md)
-   [ScrollBar (type de contrôle)](uiauto-supportscrollbarcontroltype.md)
-   [Type de contrôle SemanticZoom](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [Separator (type de contrôle)](uiauto-supportseparatorcontroltype.md)
-   [Slider (type de contrôle)](uiauto-supportslidercontroltype.md)
-   [Spinner (type de contrôle)](uiauto-supportspinnercontroltype.md)
-   [SplitButton (type de contrôle)](uiauto-supportsplitbuttoncontroltype.md)
-   [StatusBar (type de contrôle)](uiauto-supportstatusbarcontroltype.md)
-   [Tab (type de contrôle)](uiauto-supporttabcontroltype.md)
-   [TabItem (type de contrôle)](uiauto-supporttabitemcontroltype.md)
-   [Table (type de contrôle)](uiauto-supporttablecontroltype.md)
-   [Text (type de contrôle)](uiauto-supporttextcontroltype.md)
-   [Thumb (type de contrôle)](uiauto-supportthumbcontroltype.md)
-   [TitleBar (type de contrôle)](uiauto-supporttitlebarcontroltype.md)
-   [ToolBar (type de contrôle)](uiauto-supporttoolbarcontroltype.md)
-   [ToolTip (type de contrôle)](uiauto-supporttooltipcontroltype.md)
-   [Tree (type de contrôle)](uiauto-supporttreecontroltype.md)
-   [TreeItem (type de contrôle)](uiauto-supporttreeitemcontroltype.md)
-   [Window (type de contrôle)](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Identificateurs de type de contrôle](uiauto-controltype-ids.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prise en charge des types de contrôle UI Automation](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[Prise en charge d'UI Automation pour les contrôles standard](uiauto-controlsupport.md)
</dt> <dt>

[Notions de base d’UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 