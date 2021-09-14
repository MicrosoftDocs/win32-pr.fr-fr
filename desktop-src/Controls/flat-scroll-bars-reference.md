---
title: Barre de défilement plate
description: Cette section contient des informations sur les éléments de programmation utilisés pour contrôler les barres de défilement plat.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf1c1d49bf4b54d65adbe784d1e4da62adfe35c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006303"
---
# <a name="flat-scroll-bar"></a>Barre de défilement plate

Cette section contient des informations sur les éléments de programmation utilisés pour contrôler les barres de défilement plat.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                    | Contenu                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barres de défilement plat](flat-scroll-bars.md) | Microsoft Internet Explorer 4,0 a introduit une nouvelle technologie visuelle appelée barres de défilement plat. Fonctionnellement, les barres de défilement plat se comportent comme des barres de défilement standard. La différence est que vous pouvez personnaliser leur apparence dans une plus grande mesure par rapport aux barres de défilement standard.<br/> |



 

### <a name="functions"></a>Fonctions




| Rubrique | Contenu | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a> | Active ou désactive les boutons de direction de la barre de défilement plate. Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a> | Obtient les informations pour une barre de défilement en 2D. Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a> | Obtient la position du curseur dans une barre de défilement plate. Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a> | Obtient les propriétés d’une barre de défilement en 2D. Cette fonction peut également être utilisée pour déterminer si <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> a été appelé pour cette fenêtre. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a> | Obtient les propriétés d’une barre de défilement en 2D. Cette fonction peut également être utilisée pour déterminer si <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> a été appelé pour cette fenêtre.<blockquote>[!Note]<br />Identique à <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a> | Obtient la plage de défilement pour une barre de défilement en 2D. Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a> | Définit les informations pour une barre de défilement en 2D. Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a> | Définit la position actuelle du curseur dans une barre de défilement plate. Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a> | Définit les propriétés d’une barre de défilement en 2D. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a> | Définit la plage de défilement d’une barre de défilement en 2D. Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a> | Affiche ou masque une barre de défilement en 2D. Si les barres de défilement plat ne sont pas initialisées pour la fenêtre, cette fonction appelle la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> standard. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> | Initialise des barres de défilement plates pour une fenêtre particulière. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a> | Désinitialise les barres de défilement plat pour une fenêtre particulière. La fenêtre spécifiée reviendra aux barres de défilement standard. <br /> | 




 

 

 





