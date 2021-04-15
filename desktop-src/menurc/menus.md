---
title: Menus (menus et autres ressources)
description: Cette section traite des menus.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\menus.htm
keywords:
- ressources, menus
- menus, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c376aa1d2f55fa482ca7a2f98f57ae15236bf26b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383523"
---
# <a name="menus-menus-and-other-resources"></a>Menus (menus et autres ressources)

Cette section décrit les menus et explique comment les utiliser.

### <a name="in-this-section"></a>Dans cette section



| Nom                                 | Description                                                  |
|--------------------------------------|--------------------------------------------------------------|
| [À propos des menus](about-menus.md)       | Discute des menus.<br/>                                  |
| [Utilisation des menus](using-menus.md)       | Fournit des exemples de code de tâches liées aux menus.<br/> |
| [Référence du menu](menu-reference.md) | Contient la référence de l’API.<br/>                       |



 

### <a name="menu-functions"></a>Fonctions de menu



| Nom                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)                                 | Ajoute un nouvel élément à la fin de la barre de menus, du menu déroulant, du sous-menu ou du menu contextuel spécifiés. Vous pouvez utiliser cette fonction pour spécifier le contenu, l’apparence et le comportement de l’élément de menu. <br/>                                                                                                                                                                                                  |
| [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)                           | Définit l’état de l’attribut coché de l’élément de menu spécifié comme étant activé ou désactivé.<br/>                                                                                                                                                                                                                                                                                                      |
| [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)                 | Vérifie un élément de menu spécifié et en fait un élément radio. En même temps, la fonction efface tous les autres éléments de menu dans le groupe associé et efface l’indicateur de type d’élément de radio pour ces éléments.<br/>                                                                                                                                                                                                    |
| [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu)                                 | Crée un menu. Le menu est initialement vide, mais il peut être rempli avec les éléments de menu à l’aide des fonctions [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)et [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) . <br/>                                                                                                                                                                        |
| [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu)                       | Crée un menu déroulant, un sous-menu ou un menu contextuel. Le menu est initialement vide. Vous pouvez insérer ou ajouter des éléments de menu à l’aide de la fonction [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) . Vous pouvez également utiliser la fonction [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) pour insérer des éléments de menu et la fonction [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) pour ajouter des éléments de menu.<br/>                                                  |
| [**DeleteMenu**](/windows/desktop/api/Winuser/nf-winuser-deletemenu)                                 | Supprime un élément du menu spécifié. Si l’élément de menu ouvre un menu ou un sous-menu, cette fonction détruit le handle du menu ou du sous-menu et libère la mémoire utilisée par le menu ou le sous-menu. <br/>                                                                                                                                                                                                     |
| [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                               | Détruit le menu spécifié et libère toute mémoire occupée par le menu. <br/>                                                                                                                                                                                                                                                                                                                          |
| [**DrawMenuBar**](/windows/desktop/api/Winuser/nf-winuser-drawmenubar)                               | Redessine la barre de menus de la fenêtre spécifiée. Si la barre de menus change après la création de la fenêtre par le système, cette fonction doit être appelée pour dessiner la barre de menus modifiée. <br/>                                                                                                                                                                                                                         |
| [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem)                         | Active, désactive ou grise l’élément de menu spécifié. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu)                                       | Met fin au menu actif du thread appelant.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu)                                       | Récupère un handle du menu assigné à la fenêtre spécifiée. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)                         | Récupère des informations sur la barre de menus spécifiée.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions) | Récupère les dimensions de la bitmap de coche par défaut. Le système affiche ce bitmap en regard des éléments de menu sélectionnés. Avant d’appeler la fonction [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) pour remplacer la bitmap de coche par défaut d’un élément de menu, une application doit déterminer la taille correcte de la bitmap en appelant [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions). <br/> |
| [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem)                 | Détermine l’élément de menu par défaut dans le menu spécifié.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo)                               | Récupère des informations sur un menu spécifié.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuItemCount**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemcount)                     | Récupère le nombre d’éléments dans le menu spécifié. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid)                           | Récupère l’identificateur d’élément de menu d’un élément de menu situé à la position spécifiée dans un menu. <br/>                                                                                                                                                                                                                                                                                                    |
| [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)                       | Récupère des informations sur un élément de menu.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**GetMenuItemRect**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemrect)                       | Récupère le rectangle englobant pour l’élément de menu spécifié.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)                             | Récupère les indicateurs de menu associés à l’élément de menu spécifié. Si l’élément de menu ouvre un sous-menu, cette fonction retourne également le nombre d’éléments dans le sous-menu. <br/>                                                                                                                                                                                                                                |
| [**GetMenuString**](/windows/desktop/api/Winuser/nf-winuser-getmenustringa)                           | Copie la chaîne de texte de l’élément de menu spécifié dans la mémoire tampon spécifiée. <br/>                                                                                                                                                                                                                                                                                                                      |
| [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)                                 | Récupère un handle vers le menu déroulant ou le sous-menu activé par l’élément de menu spécifié. <br/>                                                                                                                                                                                                                                                                                                         |
| [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)                           | Permet à l’application d’accéder au menu fenêtre (également appelé menu système ou menu contrôle) pour copier et modifier. <br/>                                                                                                                                                                                                                                                                  |
| [**HiliteMenuItem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem)                         | Met en surbrillance ou supprime la mise en surbrillance d’un élément dans une barre de menus. <br/>                                                                                                                                                                                                                                                                                                                                |
| [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)                         | Insère un nouvel élément de menu à la position spécifiée dans un menu.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**IsMenu**](/windows/desktop/api/Winuser/nf-winuser-ismenu)                                         | Détermine si un handle est un handle de menu. <br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                                     | Charge la ressource de menu spécifiée à partir du fichier exécutable (. exe) associé à une instance d’application. <br/>                                                                                                                                                                                                                                                                                        |
| [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)                     | Charge le modèle de menu spécifié en mémoire. <br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**MenuItemFromPoint**](/windows/desktop/api/Winuser/nf-winuser-menuitemfrompoint)                   | Détermine l’élément de menu, le cas échéant, à l’emplacement spécifié.<br/>                                                                                                                                                                                                                                                                                                                                  |
| [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)                                 | Modifie un élément de menu existant. Cette fonction est utilisée pour spécifier le contenu, l’apparence et le comportement de l’élément de menu. <br/>                                                                                                                                                                                                                                                                           |
| [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu)                                 | Supprime un élément de menu ou détache un sous-menu du menu spécifié. Si l’élément de menu ouvre un menu déroulant ou un sous-menu, [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu) ne détruit pas le menu ou sa poignée, ce qui permet de réutiliser le menu. Avant d’appeler cette fonction, la fonction [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) doit récupérer un handle vers le menu ou sous-menu déroulant. <br/>                         |
| [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu)                                       | Assigne un nouveau menu à la fenêtre spécifiée. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)                 | Définit l’élément de menu par défaut pour le menu spécifié.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)                               | Définit des informations pour un menu spécifié.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)                 | Associe la bitmap spécifiée à un élément de menu. Si l’élément de menu est activé ou désactivé, le système affiche l’image bitmap appropriée en regard de l’élément de menu. <br/>                                                                                                                                                                                                                                   |
| [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)                       | Modifie les informations relatives à un élément de menu.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)                         | Affiche un menu contextuel à l’emplacement spécifié et effectue le suivi de la sélection des éléments dans le menu. Le menu contextuel peut apparaître n’importe où sur l’écran.<br/>                                                                                                                                                                                                                                             |
| [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)                     | Affiche un menu contextuel à l’emplacement spécifié et effectue le suivi de la sélection des éléments dans le menu contextuel. Le menu contextuel peut apparaître n’importe où sur l’écran.<br/>                                                                                                                                                                                                                                    |



 

La fonction suivante est obsolète.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a></td>
<td>Insère un nouvel élément de menu dans un menu, en déplaçant d’autres éléments vers le menu.
<blockquote>
[!Note]<br />
La fonction <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a> a été remplacée par la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenuitema"><strong>InsertMenuItem</strong></a> . Toutefois, vous pouvez toujours utiliser <strong>InsertMenu</strong>, si vous n’avez pas besoin des fonctionnalités étendues de <strong>InsertMenuItem</strong>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="menu-notifications"></a>Notifications de menu



| Nom                                                  | Description                                                                                                                                                                          |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM, \_ commande**](wm-command.md)                     | Envoyé lorsque l’utilisateur sélectionne un élément de commande dans un menu, lorsqu’un contrôle envoie un message de notification à sa fenêtre parente, ou lorsqu’une touche d’accès rapide est traduite. <br/> |
| [**WM \_ CONTEXTMENU**](wm-contextmenu.md)             | Indique à une fenêtre que l’utilisateur a cliqué avec le bouton droit de la souris (*cliquez avec le bouton droit*) dans la fenêtre.<br/>                                                                            |
| [**\_ENTERMENULOOP WM**](wm-entermenuloop.md)         | Informe la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été entrée. <br/>                                                                                  |
| [**\_EXITMENULOOP WM**](wm-exitmenuloop.md)           | Informe la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été quittée. <br/>                                                                                   |
| [**\_GETTITLEBARINFOEX WM**](wm-gettitlebarinfoex.md) | Envoyé pour demander des informations étendues de barre de titre. Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .<br/>                                  |
| [**la \_ MENUCOMMAND WM**](wm-menucommand.md)             | Envoyé lorsque l’utilisateur effectue une sélection à partir d’un menu. <br/>                                                                                                                        |
| [**\_MENUDRAG WM**](wm-menudrag.md)                   | Envoyé au propriétaire d’un menu glisser-déplacer lorsque l’utilisateur fait glisser un élément de menu. <br/>                                                                                               |
| [**\_MENUGETOBJECT WM**](wm-menugetobject.md)         | Envoyé au propriétaire d’un menu glisser-déplacer lorsque le curseur de la souris entre dans un élément de menu ou se déplace du centre de l’élément vers le haut ou le bas de l’élément. <br/>                |
| [**\_MENURBUTTONUP WM**](wm-menurbuttonup.md)         | Envoyé lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve sur un élément de menu. <br/>                                                                                   |
| [**\_NEXTMENU WM**](wm-nextmenu.md)                   | Envoyé à une application lorsque la touche de direction droite ou gauche est utilisée pour basculer entre la barre de menus et le menu système. <br/>                                                      |
| [**\_UNINITMENUPOPUP WM**](wm-uninitmenupopup.md)     | Envoyé lorsqu’un menu ou sous-menu déroulant a été détruit. <br/>                                                                                                                |



 

### <a name="menu-structures"></a>Structures de menu



| Nom                                                       | Description                                                                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)                         | Contient des informations sur le menu à activer. <br/>                                                                                                |
| [**MENUBARINFO**](/windows/win32/api/winuser/ns-winuser-menubarinfo)                         | Contient des informations sur la barre de menus.<br/>                                                                                                                       |
| [**\_ \_ en-tête de modèle menuex**](menuex-template-header.md) | Définit l’en-tête d’un modèle de menu étendu. Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard. <br/> |
| [**\_élément de modèle menuex \_**](menuex-template-item.md)     | Définit un élément de menu dans un modèle de menu étendu. Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard.<br/>  |
| [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)             | Contient des informations sur le menu sur lequel se trouve le curseur de la souris.<br/>                                                                                     |
| [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo)                               | Contient des informations sur un menu.<br/>                                                                                                                   |
| [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)                       | Contient des informations sur un élément de menu. <br/>                                                                                                             |
| [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)               | Définit un élément de menu dans un modèle de menu. <br/>                                                                                                             |
| [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)   | Définit l’en-tête d’un modèle de menu. Un modèle de menu complet se compose d’un en-tête et d’une ou plusieurs listes d’éléments de menu. <br/>                              |
| [**TPMPARAMS**](/windows/win32/api/winuser/ns-winuser-tpmparams)                             | Contient des paramètres étendus pour la fonction [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .<br/>                                                          |



 

 

