---
description: Cette rubrique répertorie les principaux éléments de programmation utilisés avec les menus contextuels (contextuels) et les gestionnaires de menus contextuels. Les gestionnaires de menus contextuels, également appelés gestionnaires de menus contextuels ou gestionnaires de verbes, sont un type de gestionnaire de type de fichier.
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: Référence du menu contextuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f80b62b88750200456da76c22017b3f18fbba584272dc028809771c807ad85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090769"
---
# <a name="shortcut-menu-reference"></a>Référence du menu contextuel

Cette rubrique répertorie les principaux éléments de programmation utilisés avec les menus contextuels (contextuels) et les gestionnaires de menus contextuels. Les gestionnaires de menus contextuels, également appelés gestionnaires de menus contextuels ou gestionnaires de verbes, sont un type de gestionnaire de type de fichier.

## <a name="about-shortcut-menu-implemetation"></a>À propos du menu contextuel implémentation

Il est vivement recommandé d’implémenter un menu contextuel à l’aide de l’une des méthodes de verbe statique. Veuillez consulter les instructions suivantes :

-   Pour utiliser une méthode verbale statique pour implémenter un menu contextuel, consultez la section « personnalisation d’un menu contextuel à l’aide de verbes statiques » de [création de gestionnaires de menus contextuels](context-menu-handlers.md).
-   pour obtenir le comportement dynamique des verbes statiques dans Windows 7 et versions ultérieures, consultez « obtention du comportement dynamique pour les verbes statiques » dans [création de gestionnaires de menus contextuels](context-menu-handlers.md).
-   Pour plus d’informations sur l’implémentation d’un verbe statique et sur les verbes dynamiques à éviter, consultez [choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md).
-   Si vous devez étendre le menu contextuel d’un type de fichier en inscrivant un verbe dynamique pour le type de fichier, suivez les instructions fournies dans [Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md).

### <a name="interfaces"></a>Interfaces



| Rubrique                                        | Contenu                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | Expose les méthodes qui créent ou fusionnent un menu contextuel associé à un objet Shell.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | Expose des méthodes qui créent ou fusionnent un menu contextuel (contexte) associé à un objet Shell. Étend [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) en ajoutant une méthode qui permet aux objets clients de gérer des messages associés à des éléments de menu owner-drawn.<br/>                                                                                                                                                                                                                                                    |
| [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | Expose les méthodes qui créent ou fusionnent un menu contextuel associé à un objet Shell. Permet aux objets clients de gérer des messages associés à des éléments de menu owner-drawn et étend [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) en acceptant une valeur de retour de cette gestion des messages.<br/>                                                                                                                                                                                                                         |
| [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | Expose une méthode qui active le rappel d’un menu contextuel. Par exemple, pour ajouter une icône de bouclier à un **MenuItem** qui requiert une élévation.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | Implémenté par l’affichage des dossiers par défaut créé à l’aide de [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). Une implémentation de [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) prend en charge [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)et [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) et tout transfert de messages nécessaire pour cette fonction. **IContextMenuSite** met également à jour également la barre d’État.<br/> |



 

### <a name="functions"></a>Fonctions



| Rubrique                                                            | Contenu                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | Crée un menu contextuel pour un groupe sélectionné d’objets de dossier de fichiers.<br/>                                                          |
| [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | Définit le prototype pour la fonction de rappel qui reçoit des messages à partir de l’implémentation du menu contextuel par défaut de l’interpréteur de commandes.<br/> |
| [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | Crée un objet qui représente l’implémentation du menu contextuel par défaut de l’interpréteur de commandes.<br/>                                           |



 

### <a name="structures"></a>Structures



| Rubrique                                                  | Contenu                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | Contient les informations nécessaires à [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) pour appeler une commande de menu contextuel.<br/>                                                             |
| [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | Contient des informations étendues sur une commande de menu contextuel. Cette structure est une version étendue de [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) qui permet d’utiliser des valeurs Unicode.<br/> |
| [**DEFCONTEXTMENU**](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | Contient les informations de menu contextuel utilisées par [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).<br/>                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Menus contextuels (menu contextuel) et gestionnaires de menus contextuels](context-menu.md)
</dt> <dt>

[Choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md)
</dt> <dt>

[Verbes et associations de fichiers](fa-verbs.md)
</dt> <dt>

[Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes de sélection multiple](verbs-best-practices.md)
</dt> <dt>

[Création de gestionnaires de menu contextuel](context-menu-handlers.md)
</dt> <dt>

[Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 
