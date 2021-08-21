---
title: Identificateurs d’objets (winuser. h)
description: Cette rubrique décrit les identificateurs d’objets Microsoft Active Accessibility, les valeurs 32 bits qui identifient les catégories d’objets accessibles dans une fenêtre.
ms.assetid: dc1603f8-29e5-4acd-817a-c6957feaff6c
topic_type:
- apiref
api_name:
- OBJID_ALERT
- OBJID_CARET
- OBJID_CLIENT
- OBJID_CURSOR
- OBJID_HSCROLL
- OBJID_NATIVEOM
- OBJID_MENU
- OBJID_QUERYCLASSNAMEIDX
- OBJID_SIZEGRIP
- OBJID_SOUND
- OBJID_SYSMENU
- OBJID_TITLEBAR
- OBJID_VSCROLL
- OBJID_WINDOW
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b91bf70333d4ba7d607e465851f7f217aec43b0a081ec020017321fe30a7ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565064"
---
# <a name="object-identifiers-winuserh"></a>Identificateurs d’objets (winuser. h)

Cette rubrique décrit les identificateurs d’objets Microsoft Active Accessibility, les valeurs 32 bits qui identifient les *catégories* d’objets accessibles dans une fenêtre. Les serveurs Microsoft Active Accessibility et les fournisseurs UI Automation de Microsoft utilisent les identificateurs d’objet pour déterminer l’objet auquel une demande de message [**WM \_ GETOBJECT**](wm-getobject.md) fait référence.

Les clients reçoivent ces valeurs dans leur fonction de rappel [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) et les utilisent pour identifier des parties d’une fenêtre. Les serveurs utilisent ces valeurs pour identifier les parties correspondantes d’une fenêtre lors de l’appel de [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) ou lors de la réponse au message [**WM \_ GETOBJECT**](wm-getobject.md) .

Les serveurs peuvent définir des ID d’objet personnalisés pour identifier d’autres catégories d’objets au sein de leurs applications. Des valeurs positives doivent être affectées aux ID d’objet personnalisés, car Microsoft Active Accessibility réserve zéro et toutes les valeurs négatives pour les identificateurs d’objet standard suivants.

Les constantes suivantes sont définies dans winuser. h :



| Constante                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**\_alerte objid**</dt> </dl>                                     | Alerte associée à une fenêtre ou à une application. Les boîtes de message fournies par le système sont les seuls éléments d’interface utilisateur qui envoient des événements avec cet identificateur d’objet. Les applications serveur ne peuvent pas utiliser les fonctions **AccessibleObjectFrom**_X_ avec cet identificateur d’objet. Il s’agit d’un problème connu avec Microsoft Active Accessibility.<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**\_signe insertion objid**</dt> </dl>                                     | Barre d’insertion de texte (signe insertion) dans la fenêtre.<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**\_client objid**</dt> </dl>                                  | Zone cliente de la fenêtre. Dans la plupart des cas, le système d’exploitation contrôle les éléments Frame et l’objet client contient tous les éléments contrôlés par l’application. Les serveurs traitent uniquement les messages [**WM \_ GETOBJECT**](wm-getobject.md) dans lesquels *lParam* est \_ un client objid, \_ une fenêtre objid ou un identificateur d’objet personnalisé.<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**\_curseur objid**</dt> </dl>                                  | Pointeur de la souris. Il n’y a qu’un seul pointeur de souris dans le système et il n’est pas un enfant d’une fenêtre.<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**OBJID \_ HSCROLL**</dt> </dl>                               | Barre de défilement horizontale de la fenêtre.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**OBJID \_ NATIVEOM**</dt> </dl>                            | En réponse à cet identificateur d’objet, les applications tierces peuvent exposer leur propre modèle objet. Les applications tierces peuvent retourner n’importe quelle interface COM en réponse à cet identificateur d’objet.<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**\_menu objid**</dt> </dl>                                        | Barre de menus de la fenêtre.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**OBJID \_ QUERYCLASSNAMEIDX**</dt> </dl> | Identificateur d’objet qui Oleacc.dll utilise en interne. Pour plus d’informations, consultez [annexe F : valeurs de l’identificateur d’objet pour objid \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**OBJID \_ SIZEGRIP**</dt> </dl>                            | La poignée de dimensionnement de la fenêtre : un composant Frame facultatif situé dans le coin inférieur droit du cadre de la fenêtre.<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**\_son objid**</dt> </dl>                                     | Objet son. Les objets sons n’ont pas d’emplacements d’écran ou d’enfants, mais ils ont des attributs Name et State. Il s’agit des enfants de l’application qui lit le son.<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**OBJID \_ SYSMENU**</dt> </dl>                               | Menu système de la fenêtre.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**\_titre objid**</dt> </dl>                            | Barre de titre de la fenêtre.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**OBJID \_ VSCROLL**</dt> </dl>                               | Barre de défilement verticale de la fenêtre.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**\_fenêtre objid**</dt> </dl>                                  | La fenêtre elle-même plutôt qu’un objet enfant.<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





