---
description: L’objet PenInputPanel vous permet d’ajouter facilement une entrée de stylet sur place à vos applications.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: PenInputPanel, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 58d27b97bb6683f32c145b92c1fda65fe0a786d5cb502e644580b57366119840
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708339"
---
# <a name="peninputpanel-class"></a>PenInputPanel, classe

\[Déconseillé. **PenInputPanel** a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).\]

L’objet **PenInputPanel** vous permet d’ajouter facilement une entrée de stylet sur place à vos applications.

L’objet **PenInputPanel** est disponible sous la forme d’un objet pouvant être attaché qui vous permet d’ajouter des fonctionnalités du panneau de saisie Tablet PC à des contrôles existants. L’interface utilisateur est en grande partie mandatée par la langue d’entrée actuelle. Vous avez la possibilité de choisir la méthode d’entrée par défaut pour l’objet **PenInputPanel** , à savoir l’écriture manuscrite ou le clavier. L’utilisateur final peut basculer entre les méthodes d’entrée à l’aide des boutons de l’interface utilisateur.

**PenInputPanel** possède les types de membres suivants :

-   [Énumérations](#enumerations)
-   [Événements](#events)
-   [Interfaces](#interfaces)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="enumerations"></a>Énumérations

La classe **PenInputPanel** possède ces énumérations.



| Énumération                    | Description                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [**PanelType**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | Définit le type d’entrée actuellement disponible dans l’objet **PenInputPanel** .<br/> |



 

### <a name="events"></a>Événements

La classe **PenInputPanel** contient ces événements.



| Événement                                                  | Description                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**InputFailed**](peninputpanel-inputfailed.md)       | Se produit lorsque le focus d’entrée est modifié avant que l’objet **PenInputPanel** ait pu insérer une entrée d’utilisateur dans le contrôle attaché.<br/> |
| [**PanelChanged**](peninputpanel-panelchanged.md)     | Se produit lorsque l’objet **PenInputPanel** change entre des dispositions.<br/>                                                            |
| [**PanelMoving**](peninputpanel-panelmoving.md)       | Se produit lorsque l’objet **PenInputPanel** est déplacé.<br/>                                                                          |
| [**VisibleChanged**](peninputpanel-visiblechanged.md) | Se produit lorsque l’objet **PenInputPanel** est affiché ou masqué.<br/>                                                         |



 

### <a name="interfaces"></a>Interfaces

La classe **PenInputPanel** définit ces interfaces.



| Interface          | Description                                                             |
|:-------------------|:------------------------------------------------------------------------|
| **IPenInputPanel** | Cet objet implémente l’interface com **IPenInputPanel** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **PenInputPanel** possède ces méthodes.



| Méthode                                                         | Description                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | Envoie l’encre collectée au module de reconnaissance et publie le résultat de la reconnaissance.<br/>                                                                                                                      |
| [**EnableTsf**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | Quand la **valeur true est affectée**, **PenInputPanel** tente d’envoyer du texte au contrôle attaché via Text Services Framework (TSF) et permet d’utiliser l’interface utilisateur de correction.<br/>    |
| [**DéplacerVers**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | Définit la position de l’objet **PenInputPanel** sur une position d’écran statique.<br/>                                                                                                               |
| [**Générer**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | Met à jour et restaure les propriétés **PenInputPanel** en fonction des paramètres du panneau de saisie Tablet PC, positionne automatiquement le panneau de saisie du stylet et définit l’interface utilisateur sur le panneau par défaut.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **PenInputPanel** possède les propriétés suivantes.



| Propriété                                                                  | Type d’accès           | Description                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | Lecture/écriture<br/> | Obtient ou définit le handle de fenêtre du contrôle auquel l’objet **PenInputPanel** est attaché.<br/>                                                                     |
| [**Affichage automatique**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui spécifie si l’objet **PenInputPanel** s’affiche lorsque le focus est défini à l’aide du stylet.<br/>                                           |
| [**Emploie**](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | Lecture seule<br/>  | Obtient une valeur booléenne qui spécifie si l’objet **PenInputPanel** est en cours de traitement de l’encre.<br/>                                                               |
| [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | Lecture/écriture<br/> | Obtient ou définit le type de panneau actuellement utilisé pour l’entrée dans l’objet **PenInputPanel** .<br/>                                                                |
| [**DefaultPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | Lecture/écriture<br/> | Obtient ou définit le type de panneau par défaut utilisé pour l’entrée dans l’objet **PenInputPanel** .<br/>                                                         |
| [**Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | Lecture/écriture<br/> | Obtient ou définit le nom de chaîne du Factoid utilisé dans la reconnaissance.<br/>                                                                                                    |
| [**Hauteur**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | Lecture seule<br/>  | Obtient la hauteur de l’objet **PenInputPanel** dans les coordonnées clientes.<br/>                                                                                              |
| [**HorizontalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | Lecture/écriture<br/> | Obtient ou définit le décalage entre le bord gauche de l’objet **PenInputPanel** et le bord gauche du contrôle auquel il est attaché.<br/>                             |
| [**Gauche**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | Lecture seule<br/>  | Obtient l’emplacement horizontal (ou axe des x) du bord gauche de l’objet **PenInputPanel** , en coordonnées d’écran.<br/>                                                   |
| [**Retour au début**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | Lecture seule<br/>  | Obtient l’emplacement vertical, ou axe y, de l’emplacement du bord supérieur de l’objet **PenInputPanel** , en coordonnées d’écran.<br/>                                                      |
| [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | Lecture/écriture<br/> | Obtient ou définit le décalage entre le bord horizontal le plus proche de l’objet **PenInputPanel** et le bord horizontal le plus proche du contrôle auquel il est attaché.<br/> |
| [**Parent**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique si l’objet **PenInputPanel** est visible.<br/>                                                                                |
| [**Largeur**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | Lecture seule<br/>  | Obtient la largeur de l’objet **PenInputPanel** dans les coordonnées clientes.<br/>                                                                                               |



 

## <a name="remarks"></a>Remarques

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Programmation du panneau de saisie à l’aide de la classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
