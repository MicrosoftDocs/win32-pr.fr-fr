---
title: List-View les styles de fenêtre (CommCtrl. h)
description: Les styles de fenêtre suivants sont spécifiques aux contrôles d’affichage de liste.
ms.assetid: 8b57239b-112e-4fb6-b394-15501bd3f5b3
topic_type:
- apiref
api_name:
- LVS_ALIGNLEFT
- LVS_ALIGNMASK
- LVS_ALIGNTOP
- LVS_AUTOARRANGE
- LVS_EDITLABELS
- LVS_ICON
- LVS_LIST
- LVS_NOCOLUMNHEADER
- LVS_NOLABELWRAP
- LVS_NOSCROLL
- LVS_NOSORTHEADER
- LVS_OWNERDATA
- LVS_OWNERDRAWFIXED
- LVS_REPORT
- LVS_SHAREIMAGELISTS
- LVS_SHOWSELALWAYS
- LVS_SINGLESEL
- LVS_SMALLICON
- LVS_SORTASCENDING
- LVS_SORTDESCENDING
- LVS_TYPEMASK
- LVS_TYPESTYLEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e326f4508d08f1052747e64ea5eba184f45f7e73a1cb55539255a27fd8c8c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412024"
---
# <a name="list-view-window-styles"></a>Styles de fenêtre List-View

Les styles de fenêtre suivants sont spécifiques aux contrôles d’affichage de liste.



| Constante                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**LVS \_ ALIGNLEFT**</dt> </dl>                   | Les éléments sont alignés à gauche en mode icône et petite icône. <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**LVS \_ ALIGNMASK**</dt> </dl>                   | Alignement actuel du contrôle. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**LVS \_ ALIGNTOP**</dt> </dl>                      | Les éléments sont alignés avec le haut du contrôle List-View en mode icône et petite icône. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**réorganisation LVS \_**</dt> </dl>             | Les icônes restent automatiquement organisées en mode icône et petite icône. <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**LVS \_ EDITLABELS**</dt> </dl>                | Le texte de l’élément peut être modifié sur place. La fenêtre parente doit traiter le code de notification [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) . <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**\_icône LVS**</dt> </dl>                                  | Ce style spécifie l’affichage des icônes. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**\_liste LVS**</dt> </dl>                                  | Ce style spécifie la vue liste. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS \_ NOCOLUMNHEADER**</dt> </dl>    | Les en-têtes de colonne ne sont pas affichés dans la vue rapport. Par défaut, les colonnes ont des en-têtes dans la vue rapport. <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**LVS \_ NOLABELWRAP**</dt> </dl>             | Le texte de l’élément est affiché sur une seule ligne en mode icône. Par défaut, le texte de l’élément peut être renvoyé à la ligne en mode icône. <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS \_ NOscroll**</dt> </dl>                      | Le défilement est désactivé. Tous les éléments doivent se trouver dans la zone cliente. Ce style n’est pas compatible avec **la \_ liste LVS** ou les styles de **\_ rapport LVS** . Pour plus d’informations, consultez l’article Q137520 de la base de connaissances. <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**LVS \_ NOSORTHEADER**</dt> </dl>          | Les en-têtes de colonnes ne fonctionnent pas comme des boutons. Ce style peut être utilisé si le fait de cliquer sur un en-tête de colonne dans la vue rapport n’effectue pas d’action, telle que le tri. <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**LVS \_ OWNERDATA**</dt> </dl>                   | [Version 4,70](common-control-versions.md). Ce style spécifie un contrôle d’affichage de liste virtuel. Pour plus d’informations sur ce style de contrôle de liste, consultez [à propos des contrôles de List-View](list-view-controls-overview.md). <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**LVS \_ OWNERDRAWFIXED**</dt> </dl>    | La fenêtre propriétaire peut peindre des éléments dans la vue rapport. Le contrôle List-View envoie un message [**WM \_ DRAWITEM**](wm-drawitem.md) pour peindre chaque élément ; il n’envoie pas de messages distincts pour chaque sous-élément. Le membre **iItemData** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contient les données d’élément pour l’élément de vue de liste spécifié. <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**\_rapport LVS**</dt> </dl>                            | Ce style spécifie la vue rapport. Lorsque vous utilisez le \_ style de rapport LVS avec un contrôle List-View, la première colonne est toujours alignée à gauche. Vous ne pouvez pas utiliser LVCFMT \_ Right pour modifier cet alignement. Pour plus d’informations sur l’alignement des colonnes, consultez [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) . <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**LVS \_ SHAREIMAGELISTS**</dt> </dl> | La liste d’images n’est pas supprimée lorsque le contrôle est détruit. Ce style permet d’utiliser les mêmes listes d’images avec plusieurs contrôles de vue de liste. <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**LVS \_ SHOWSELALWAYS**</dt> </dl>       | La sélection, le cas échéant, est toujours affichée, même si le contrôle n’a pas le focus. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**LVS \_ SINGLESEL**</dt> </dl>                   | Un seul élément à la fois peut être sélectionné. Par défaut, plusieurs éléments peuvent être sélectionnés. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**LVS \_ SmallIcon**</dt> </dl>                   | Ce style spécifie la petite vue des icônes. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**LVS \_ SORTASCENDING**</dt> </dl>       | Les index d’éléments sont triés en fonction du texte de l’élément dans l’ordre croissant. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**LVS \_ SORTDESCENDING**</dt> </dl>    | Les index d’éléments sont triés en fonction du texte de l’élément dans l’ordre décroissant. <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**LVS \_ TYPEMASK**</dt> </dl>                      | Détermine le style de fenêtre actuel du contrôle. <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**LVS \_ TYPESTYLEMASK**</dt> </dl>       | Détermine les styles de fenêtre qui contrôlent l’alignement des éléments et l’apparence et le comportement de l’en-tête. <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Remarques

Pour les styles **LVS \_ SORTASCENDING** et **LVS \_ SORTDESCENDING** , les index d’éléments sont triés en fonction du texte de l’élément dans l’ordre croissant ou décroissant, respectivement. Étant donné que la **\_ liste LVS** et les vues de **\_ rapport LVS** affichent les éléments dans le même ordre que leurs index, les résultats du tri sont immédiatement visibles pour l’utilisateur. L' **\_ icône LVS** et les vues **LVS \_ SmallIcon** n’utilisent pas d’index d’élément pour déterminer la position des icônes. Avec ces vues, les résultats du tri ne sont pas visibles par l’utilisateur.

Vous pouvez utiliser le masque **LVS \_ TYPEMASK** pour isoler les styles de fenêtre qui correspondent à la vue actuelle **: LVS \_ Icon**, **LVS \_ List**, **LVS \_ rapport** et **LVS \_ SmallIcon**.

Vous pouvez utiliser le masque **LVS \_ ALIGNMASK** pour isoler les styles de fenêtre qui spécifient l’alignement des éléments : **LVS \_ ALIGNLEFT** et **LVS \_ ALIGNTOP**.

Vous pouvez utiliser le **masque \_ LVS TYPESTYLEMASK** pour isoler les styles de fenêtre qui contrôlent l’alignement des éléments (**LVS \_ ALIGNLEFT** et **LVS \_ ALIGNTOP**) et ceux qui contrôlent l’apparence et le comportement de l’en-tête (LVS NOCOLUMNHEADER et **LVS \_** NOSORTHEADER).**\_**

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Styles et affichages de liste](list-view-controls-overview.md)
</dt> </dl>

 

 





