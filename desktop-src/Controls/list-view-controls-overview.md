---
title: À propos des contrôles List-View
description: Un contrôle List-View est une fenêtre qui affiche une collection d’éléments.
ms.assetid: 163f7778-690c-4166-b0c5-c7be1a03ae98
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 592684378b4264319d790b1e2e05eb9e0ae37f28
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424329"
---
# <a name="about-list-view-controls"></a>À propos des contrôles List-View

Consultez l' [exemple de contrôle ListView virtuel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw).

Un contrôle List-View est une fenêtre qui affiche une collection d’éléments. Les contrôles de liste offrent plusieurs moyens d’organiser et d’afficher des éléments et sont bien plus flexibles que les [zones de liste](list-boxes.md)simples. Par exemple, des informations supplémentaires sur chaque élément peuvent être affichées dans les colonnes à droite de l’icône et de l’étiquette.

-   [Styles et affichages de liste](#list-view-styles-and-views)
    -   [Styles de List-View étendus](#extended-list-view-styles)
-   [Style de List-View virtuel](#virtual-list-view-style)
    -   [Création d’un contrôle de List-View virtuel](#creating-a-virtual-list-view-control)
    -   [Problèmes de compatibilité](#compatibility-issues)
    -   [Gestion des codes de notification de contrôle de List-View virtuel](#handling-virtual-list-view-control-notification-codes)
    -   [Gestion du cache](#cache-management)
-   [Liste-afficher les zones de travail](#list-view-working-areas)
-   [Liste-afficher les listes d’images](#list-view-image-lists)
-   [Répertorier les éléments et les sous-éléments](#list-view-items-and-subitems)
    -   [Liste-afficher les États des éléments](#list-view-item-states)
    -   [Éléments de rappel et masque de rappel](#callback-items-and-the-callback-mask)
    -   [Liste-afficher la position des éléments](#list-view-item-position)
    -   [Organisation, tri et recherche d’éléments](#arranging-sorting-and-finding-items)
-   [Colonnes de mode liste](#list-view-columns)
-   [Position de défilement de la liste](#list-view-scroll-position)
-   [Modification des étiquettes d’affichage de liste](#list-view-label-editing)
-   [Afficher les couleurs de la liste](#list-view-colors)
-   [Organisation des éléments de liste par groupe](#arranging-list-items-by-group)
-   [Marques d’insertion](#insertion-marks)

## <a name="list-view-styles-and-views"></a>Styles et vues List-View

Les contrôles List-View peuvent afficher des éléments dans cinq vues différentes. Le style de fenêtre du contrôle spécifie la vue par défaut. Des styles de fenêtre supplémentaires spécifient l’alignement des éléments et des fonctionnalités spécifiques aux contrôles. Le tableau suivant décrit les vues.



| Nom de l'affichage             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode icône             | Spécifié par le style de fenêtre d' [**\_ icône LVS**](list-view-window-styles.md) ou en passant l' **\_ \_ icône d’affichage LV** au message [**\_ SETVIEW LVM**](lvm-setview.md) . Chaque élément s'affiche sous forme d'une icône de taille normale, avec une étiquette placée au-dessous. L’utilisateur peut faire glisser les éléments vers n’importe quel emplacement dans la fenêtre de liste.                                                                                                                                                                                                                                         |
| Affichage des petites icônes       | Spécifié par le style de fenêtre [**\_ SmallIcon LVS**](list-view-window-styles.md) ou en passant **VL \_ View \_ SmallIcon** avec [**LVM \_ SETVIEW**](lvm-setview.md). Chaque élément apparaît sous la forme d’une petite icône avec l’étiquette à droite de celui-ci. L’utilisateur peut faire glisser les éléments vers n’importe quel emplacement.                                                                                                                                                                                                                                                       |
| Affichage Liste             | Spécifié par le style de la fenêtre de [**\_ liste LVS**](list-view-window-styles.md) ou en passant la **\_ \_ liste de vue LV** avec [**LVM \_ SETVIEW**](lvm-setview.md). Chaque élément apparaît sous la forme d’une petite icône avec une étiquette à droite de celui-ci. Les éléments sont organisés en colonnes et l’utilisateur ne peut pas les faire glisser vers un emplacement arbitraire.                                                                                                                                                                                                                               |
| Affichage des rapports (détails) | Spécifié par le style de la fenêtre de [**\_ rapport LVS**](list-view-window-styles.md) ou en passant les détails de la **\_ vue \_ LV** avec le [**LVM \_ SETVIEW**](lvm-setview.md). Chaque élément apparaît sur sa propre ligne, avec les informations organisées en colonnes. La colonne la plus à gauche est toujours justifiée à gauche et contient la petite icône et l’étiquette. Les colonnes suivantes contiennent des sous-éléments tels que spécifiés par l’application. Chaque colonne possède un en-tête, sauf si vous spécifiez également le style de fenêtre [**LVS \_ NOCOLUMNHEADER**](list-view-window-styles.md) . |
| Mode Mosaïque             | **Version 6 et versions ultérieures.** Spécifié en passant **la \_ \_ vignette de la vue LV** avec [**LVM \_ SETVIEW**](lvm-setview.md). Chaque élément apparaît sous la forme d’une icône de taille complète avec une étiquette d’une ou plusieurs lignes à côté.                                                                                                                                                                                                                                                                                                                                                        |



 

Les captures d’écran suivantes utilisent des affichages pour montrer différentes quantités d’informations sur chacun des sept animaux familiers. Les vues montrent comment les informations peuvent apparaître sur Windows Vista. Les styles visuels du contrôle ont été définis sur le thème « Explorer » à l’aide de [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

La capture d’écran suivante montre le mode Détails.

![capture d’écran qui affiche des informations dans cinq colonnes et sept lignes](images/lv-detailsview.png)

La capture d’écran suivante montre l’affichage des icônes.

![capture d’écran qui affiche uniquement le nom de chaque animal de compagnie et une icône indiquant l’espèce](images/lv-iconview.png)

La capture d’écran suivante montre le mode liste.

![capture d’écran qui montre, pour chaque animal de compagnie, une grande icône à côté du nom, de la race et du prix de l’animal de compagnie](images/lv-listview.png)

La capture d’écran suivante montre l’affichage en mosaïque.

![affichage en mosaïque.](images/lv-tileview.png)

Vous pouvez modifier le type d’affichage après avoir créé un contrôle List-View. Pour récupérer et modifier le style de la fenêtre, utilisez les fonctions [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) et [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) . Pour déterminer les styles de fenêtre de l’affichage actuel, utilisez la valeur [**LVS \_ TYPEMASK**](list-view-window-styles.md) .

Vous pouvez contrôler la façon dont les éléments sont organisés en mode icône ou petite icône en spécifiant le style de fenêtre [**LVS \_ ALIGNTOP**](list-view-window-styles.md) (valeur par défaut) ou [**LVS \_ ALIGNLEFT**](list-view-window-styles.md) .

Vous pouvez modifier l’alignement après avoir créé un contrôle List-View. Pour déterminer l’alignement actuel, utilisez la valeur [**LVS \_ ALIGNMASK**](list-view-window-styles.md) .

Des styles de fenêtre supplémentaires fournissent d’autres options, par exemple si un utilisateur peut modifier des étiquettes ou sélectionner plusieurs éléments à la fois. Pour obtenir une liste complète, consultez [styles de fenêtre d’affichage de liste](list-view-window-styles.md).

### <a name="extended-list-view-styles"></a>Styles de List-View étendus

Les styles de contrôle de liste étendus fournissent des options telles que les cases à cocher, les barres de défilement plat, le quadrillage et le suivi à chaud. Pour obtenir une liste complète, consultez [Extended List-View styles](extended-list-view-styles.md). Vous n’accédez pas aux styles de vue de liste étendus de la même manière que les styles de fenêtre standard. Vous n’utilisez pas les fonctions [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) et [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour apporter des modifications de style étendues.

Il existe deux messages qui définissent et récupèrent les informations de style étendu, [**LVM \_ SETEXTENDEDLISTVIEWSTYLE**](lvm-setextendedlistviewstyle.md) et [**LVM \_ GETEXTENDEDLISTVIEWSTYLE**](lvm-getextendedlistviewstyle.md). Au lieu d’envoyer les messages de manière explicite, vous pouvez utiliser les macros correspondantes suivantes : [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle), [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)et [**ListView \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle).

## <a name="virtual-list-view-style"></a>Style de List-View virtuel

Un affichage de liste virtuel est un contrôle List-View qui a le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) . Ce style permet au contrôle de gérer des millions d’éléments, car le propriétaire reçoit la charge de gestion des données d’élément. Cela vous permet d’utiliser le contrôle Virtual List-View avec de grandes bases de données d’informations, où des méthodes spécifiques d’accès aux données sont déjà en place.

Un contrôle List-View virtuel gère très peu les informations sur les éléments. À l’exception des informations de sélection d’élément et de focus, le propriétaire du contrôle doit gérer toutes les informations d’élément. D’autres processus demandent des informations d’élément au propriétaire à l’aide de codes de notification [LVN \_ GETDISPINFO](lvn-getdispinfo.md) .

Étant donné que ce type de contrôle de liste est destiné aux jeux de données volumineux, il est recommandé de mettre en cache les données d’élément demandées pour améliorer les performances de récupération. Le mode liste fournit un mécanisme d’affinage du cache pour faciliter l’optimisation du cache. L’indicateur est implémenté sous la forme d’un code de notification [LVN \_ ODCACHEHINT](lvn-odcachehint.md) .

### <a name="creating-a-virtual-list-view-control"></a>Création d’un contrôle de List-View virtuel

Vous pouvez créer des contrôles d’affichage de liste virtuels à l’aide de la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant le style de fenêtre [**LVS \_ OWNERDATA**](list-view-window-styles.md) dans le cadre du paramètre de fonction *dwStyle* . Le basculement dynamique vers et depuis le style **LVS \_ OWNERDATA** n’est pas pris en charge.

Vous pouvez utiliser le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) en association avec la plupart des autres styles de fenêtre, à l’exception du style [**LVS \_ SORTASCENDING**](list-view-window-styles.md) ou [**LVS \_**](list-view-window-styles.md) SORTDESCENDING. Tous les contrôles de liste virtuelle affichent par défaut le style de [**\_ réorganisation LVS**](list-view-window-styles.md) .

Pour permettre l’affichage des éléments dans la liste, vous devez d’abord envoyer le message [**\_ SETITEMCOUNT LVM**](lvm-setitemcount.md) , explicitement ou à l’aide de la macro [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) .

Les messages suivants ne sont pas pris en charge sous le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) : [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md), [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md), [**LVM \_ SETTILEINFO**](lvm-settileinfo.md)et [**LVM \_ MAPIDTOINDEX**](lvm-mapidtoindex.md).

### <a name="compatibility-issues"></a>Problèmes de compatibilité

Les quatre styles de vue de liste (icône, petite icône, liste et rapport) prennent en charge le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) . Les contrôles List-View qui ont le style **LVS \_ OWNERDATA** ne stockent pas d’informations spécifiques à l’élément. Par conséquent, les seuls indicateurs d’état d’élément valides que vous pouvez appliquer à un élément sont [**Lvis \_ Selected**](list-view-item-states.md) et [**Lvis \_ Focused**](list-view-item-states.md). Aucune autre information d’État n’est stockée. En particulier, le contrôle List-View ne conserve pas les images d’État ou de superposition pour chaque élément. Toutefois, vous pouvez faire en sorte que le contrôle de vue de liste interroge votre application sur ces images en lui envoyant un message [**\_ SETCALLBACKMASK LVM**](lvm-setcallbackmask.md) .

La plupart des messages de contrôle d’affichage de liste et les macros associées sont entièrement pris en charge. Toutefois, certains messages présentent des limitations ou ne sont pas pris en charge lorsque vous utilisez le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) . Le tableau suivant récapitule les messages affectés.



| Message                                             | Limitation                                                                                                                                                                                                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**réorganisation LVM \_**](lvm-arrange.md)                 | Ne prend pas en charge le style **LVA \_ SNAPTOGRID** .                                                                                                                                                                                                                 |
| [**\_DELETEALLITEMS LVM**](lvm-deleteallitems.md)   | Définit le nombre d’éléments à zéro et efface toutes les variables de sélection internes, mais ne supprime pas réellement les éléments. Il effectue un rappel de notification.                                                                                                           |
| [**LVM \_ DELETEITEM**](lvm-deleteitem.md)           | Est pris en charge pour l’intégrité de la sélection uniquement et ne supprime pas réellement un élément.                                                                                                                                                                                 |
| [**\_GETITEMSTATE LVM**](lvm-getitemstate.md)       | Retourne uniquement les États de focus et de sélection (autrement dit, les États stockés par le contrôle List-View).                                                                                                                                                                |
| [**\_GETNEXTITEM LVM**](lvm-getnextitem.md)         | Ne prend pas en charge les critères de recherche List-View **LVNI \_ Cut**, **LVNI \_ Hidden** ou **LVNI \_ DROPHILITED**. Tous les autres critères sont pris en charge.                                                                                                                     |
| [**\_GETWORKAREAS LVM**](lvm-getworkareas.md)       | Non prise en charge.                                                                                                                                                                                                                                               |
| [**INSERTITEM de LVM \_**](lvm-insertitem.md)           | Est pris en charge pour l’intégrité de la sélection uniquement.                                                                                                                                                                                                                      |
| [**\_SETITEM LVM**](lvm-setitem.md)                 | Non prise en charge. Pour définir l’état de l’élément, utilisez le message [**ListView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .                                                                                                                                               |
| [**\_SETITEMCOUNT LVM**](lvm-setitemcount.md)       | Définit le nombre d’éléments actuellement dans la liste. Si le contrôle d’affichage de liste envoie une notification qui demande des données pour tout élément jusqu’à la valeur maximale définie, le propriétaire doit être prêt à fournir ces données. Les paramètres de message prennent en charge les contrôles de liste virtuels. |
| [**\_SETITEMPOSITION LVM**](lvm-setitemposition.md) | Non prise en charge.                                                                                                                                                                                                                                               |
| [**\_SETITEMSTATE LVM**](lvm-setitemstate.md)       | Autorise uniquement la modification des États de sélection et de focus pour l’élément.                                                                                                                                                                                          |
| [**\_SETITEMTEXT LVM**](lvm-setitemtext.md)         | Non prise en charge. Il incombe à l’application de conserver les textes des éléments.                                                                                                                                                                            |
| [**\_SETWORKAREAS LVM**](lvm-setworkareas.md)       | Non prise en charge.                                                                                                                                                                                                                                               |
| [**\_SORTITEMS LVM**](lvm-sortitems.md)             | Non prise en charge. Il incombe à l’application de présenter les éléments dans l’ordre souhaité.                                                                                                                                                             |



 

### <a name="handling-virtual-list-view-control-notification-codes"></a>Gestion des codes de notification de contrôle de List-View virtuel

Les contrôles List-View avec le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) envoient les mêmes codes de notification que les autres contrôles de vue de liste et deux autres : [LVN \_ ODCACHEHINT](lvn-odcachehint.md) et [LVN \_ ODFINDITEM](lvn-odfinditem.md). Voici les notifications les plus courantes que le contrôle List-View avec le style **LVS \_ OWNERDATA** envoie.



|      Notification                    |     Description                         |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LVN \_ GETDISPINFO](lvn-getdispinfo.md) | Un contrôle Virtual List-View gère très peu les informations sur les éléments. Par conséquent, il envoie souvent le code de notification [LVN \_ GETDISPINFO](lvn-getdispinfo.md) pour demander des informations sur l’élément. Ce message est traité à peu près de la même façon que les éléments de rappel dans un contrôle de liste standard. Étant donné que le nombre d’éléments pris en charge par le contrôle peut être très volumineux, la mise en cache des données d’élément améliore les performances. Lors de la gestion de LVN \_ GETDISPINFO, le propriétaire du contrôle tente d’abord de fournir les informations d’élément demandées à partir du cache (pour plus d’informations, consultez [gestion du cache](#cache-management)). Si l’élément demandé n’est pas mis en cache, le propriétaire doit être prêt à fournir les informations par d’autres moyens. |
| [LVN \_ ODCACHEHINT](lvn-odcachehint.md) | Une vue de liste virtuelle envoie le code de notification [LVN \_ ODCACHEHINT](lvn-odcachehint.md) pour faciliter l’optimisation du cache. Le code de notification fournit des valeurs d’index inclusives pour une plage d’éléments qu’il est recommandé de mettre en cache. À la réception du code de notification, le propriétaire doit être prêt à charger le cache avec les informations relatives à l’élément pour la plage demandée afin que les informations soient immédiatement disponibles lorsqu’un message [LVN \_ GETDISPINFO](lvn-getdispinfo.md) est envoyé.                                                                                                                                                                                                                                   |
| [LVN \_ ODFINDITEM](lvn-odfinditem.md)   | Le code de notification [LVN \_ ODFINDITEM](lvn-odfinditem.md) est envoyé par un contrôle List-View virtuel lorsque le contrôle a besoin du propriétaire pour rechercher un élément de rappel particulier. Le code de notification est envoyé lorsque le contrôle List-View reçoit un accès à la clé rapide ou lorsqu’il reçoit un message [**\_ FINDITEM LVM**](lvm-finditem.md) . Les informations de recherche sont envoyées sous la forme d’une structure [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , qui est membre de la structure [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . Le propriétaire doit être prêt à rechercher un élément qui correspond aux informations fournies par le contrôle List-View. Le propriétaire retourne l’index de l’élément en cas de réussite, ou-1 si aucun élément correspondant n’est trouvé.               |



 

### <a name="cache-management"></a>Gestion du cache

Un contrôle List-View avec le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) produit un grand nombre de codes de notification [LVN \_ GETDISPINFO](lvn-getdispinfo.md) et, pour faciliter l’optimisation du cache, un message LVN [ \_ ODCACHEHINT](lvn-odcachehint.md) . Les \_ messages LVN ODCACHEHINT fournissent des informations sur les éléments recommandés à inclure dans le cache. Ces messages sont envoyés sous forme de messages de [**\_ notification WM**](wm-notify.md) , avec la valeur *lParam* qui agit comme l’adresse d’une structure [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) .

La structure [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) inclut deux membres entiers, **iFrom** et **ITO**, qui représentent les points de terminaison inclusifs d’une plage d’éléments qui sont les plus susceptibles d’être nécessaires. Le propriétaire doit être prêt à charger le cache avec les informations d’élément pour chacun des éléments dans la plage recommandée.

Le contrôle de liste a souvent besoin d’informations sur l’élément pour le premier élément (décalage 0). Le code de notification [LVN \_ ODCACHEHINT](lvn-odcachehint.md) peut ne pas toujours inclure l’élément 0, mais il doit toujours être inclus dans le cache.

Les derniers éléments de la liste font l’objet d’un accès fréquent. Par conséquent, le propriétaire peut vouloir conserver un deuxième cache qui comprend les éléments à la fin de la liste. La plage demandée à partir de [LVN \_ ODCACHEHINT](lvn-odcachehint.md) peut être vérifiée par rapport au cache de fin pour qu’elle soit disponible automatiquement au lieu de recharger la même plage de fin à chaque fois.

## <a name="list-view-working-areas"></a>List-View les zones de travail

Les contrôles List-View prennent en charge les zones de travail, qui sont des zones virtuelles rectangulaires que le contrôle List-View utilise pour réorganiser ses éléments. Une zone de travail n’est pas une fenêtre et ne peut pas avoir de bordure visible. Par défaut, le contrôle d’affichage de liste n’a pas de zones de travail. En créant une zone de travail, vous pouvez créer une bordure vide à gauche, en haut ou à droite des éléments ou provoquer l’affichage d’une barre de défilement horizontale quand il n’y en a pas normalement.

Lorsqu’une zone de travail est créée, les éléments qui se trouvent dans la zone de travail deviennent membres de la zone de travail. De même, si un élément est déplacé dans une zone de travail, l’élément devient membre de cette zone de travail. Si un élément ne se trouve dans aucune zone de travail, il devient automatiquement membre de la première zone de travail (index 0). Pour placer un nouvel élément dans une zone de travail spécifique, vous devez d’abord créer l’élément, puis utiliser le [**\_ SETITEMPOSITION LVM**](lvm-setitemposition.md) ou le message [**LVM \_ SETITEMPOSITION32**](lvm-setitemposition32.md) pour le déplacer dans la zone de travail de votre choix.

L’illustration suivante est un exemple de contrôle List-View qui contient quatre zones de travail, chacune dans un autre quadrant de la zone cliente.

![capture d’écran d’un contrôle List-View avec une zone de travail dans chaque quadrant de la zone cliente](images/working.jpg)

Plusieurs zones de travail peuvent être utilisées pour la création de différentes zones dans une vue. Vous pouvez créer des zones dans une vue unique qui ont des significations différentes. Par exemple, une vue d’un système de fichiers peut avoir une zone pour les fichiers en lecture/écriture et une autre zone pour les fichiers en lecture seule. L’utilisateur peut catégoriser les éléments en les plaçant dans des zones de travail différentes. Si un fichier est déplacé dans la zone en lecture seule, il est automatiquement en lecture seule.

Plusieurs zones de travail peuvent se croiser, mais les éléments qui se trouvent dans l’intersection deviennent membres de la zone avec l’index inférieur ; par conséquent, il est préférable d’éviter cette situation. Lorsque vous triez plusieurs zones de travail, les éléments sont triés par rapport aux autres éléments dans la même zone de travail.

Le nombre de zones de travail peut être récupéré avec le message [**LVM \_ GETNUMBEROFWORKAREAS**](lvm-getnumberofworkareas.md) . Les zones de travail sont modifiées à l’aide du message [**\_ SETWORKAREAS LVM**](lvm-setworkareas.md) et peuvent être récupérées avec le message [**LVM \_ GETWORKAREAS**](lvm-getworkareas.md) . Ces deux messages prennent l’adresse d’un tableau de structures [**Rect**](/previous-versions//dd162897(v=vs.85)) comme *lParam* et le nombre de structures **Rect** comme *wParam*. Les membres **gauche** et **supérieur** de ces structures spécifient les coordonnées de l’angle supérieur gauche (l’origine) de la zone de travail, tandis que les membres **droits** et **inférieurs** spécifient le coin inférieur droit de la zone de travail. Toutes les coordonnées sont exprimées en coordonnées clientes de la vue liste. Le nombre maximal de zones de travail autorisées est défini par la valeur **LV \_ Max \_ WORKAREAS** .

La modification de la zone de travail n’a aucun effet sur les contrôles d’affichage de liste qui ont la [**\_ liste LVS**](list-view-window-styles.md) ou la vue de [**\_ rapport LVS**](list-view-window-styles.md) , mais les zones de travail sont conservées lorsque le type de vue est modifié. Avec l' [**\_ icône LVS**](list-view-window-styles.md) et les vues [**LVS \_ SmallIcon**](list-view-window-styles.md) , la zone de travail peut être modifiée pour modifier la façon dont les éléments sont affichés. La définition de la largeur de la zone de travail (à gauche) par rapport à la largeur du client du contrôle entraîne l’encapsulation des éléments à cette largeur et la barre de défilement horizontale à afficher. Si vous faites en sorte que la largeur de la zone de travail soit plus étroite que la largeur de la zone cliente du contrôle, les éléments sont encapsulés dans la zone de travail et non dans la zone cliente. La définition du membre de **gauche** ou du **haut** sur une valeur positive entraîne l’affichage des éléments à partir de la zone de travail, en créant un espace vide entre le bord du contrôle et les éléments. Un espace vide peut également être créé entre le bord droit du contrôle et les éléments en faisant en sorte que la largeur de la zone de travail soit inférieure à la largeur du client du contrôle.

## <a name="list-view-image-lists"></a>List-View les listes d’images

Par défaut, un contrôle List-View n’affiche pas d’images d’élément. Pour afficher des images d’élément, vous devez créer des listes d’images et les associer au contrôle. Un contrôle List-View peut avoir trois listes d’images :

-   Liste d’images qui contient les icônes de taille réelle affichées lorsque le contrôle est en mode icône.
-   Liste d’images qui contient de petites icônes affichées lorsque le contrôle est en mode petite icône, liste ou rapport.
-   Liste d’images qui contient des images d’État qui sont affichées à gauche de l’icône de taille complète ou petite. Vous pouvez utiliser des images d’État, telles que des cases à cocher activées et désactivées, pour indiquer les États des éléments définis par l’application. Les images d’État sont affichées en mode icône, en mode petite icône, en mode liste et en mode rapport.

Les listes d’images complètes et petites icônes peuvent également contenir des *images de superposition*, qui sont conçues pour être dessinées de manière transparente sur les icônes d’élément.

Pour utiliser des images de superposition dans un contrôle List-View :

1.  Appelez la fonction [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) pour affecter un index d’image de superposition à une image dans les listes d’images d’icône de taille réelle et réduite. Une image de superposition est identifiée par un index de base un.
2.  Vous pouvez associer un index d’image de superposition à un élément lorsque vous appelez la macro [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) ou [**ListView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) . Utilisez la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) pour spécifier un index d’image de superposition dans le membre d' **État** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) de l’élément. Vous devez également définir les bits [**Lvis \_ OVERLAYMASK**](list-view-item-states.md) dans le membre **stateMask** .

Si une liste d’images d’État est spécifiée, un contrôle d’affichage de liste réserve l’espace à gauche de l’icône de chaque élément pour une image d’État.

Pour associer une image d’État à un élément, utilisez la macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) pour spécifier un index d’image d’État dans le membre d' **État** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . L’index identifie une image dans la liste d’images d’État du contrôle. Bien que les index de liste d’images soient de base zéro, le contrôle utilise des index de base 1 pour identifier les images d’État. Un index d’image d’état de zéro indique qu’un élément n’a pas d’image d’État.

Par défaut, lorsqu’un contrôle List-View est détruit, il détruit les listes d’images qui lui sont assignées. Toutefois, si un contrôle List-View a le style de fenêtre [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) , l’application est responsable de la destruction des listes d’images lorsqu’elles ne sont plus utilisées. Vous devez spécifier ce style si vous assignez les mêmes listes d’images à plusieurs contrôles de vue de liste. dans le cas contraire, plusieurs contrôles peuvent tenter de détruire la même liste d’images.

## <a name="list-view-items-and-subitems"></a>Éléments et sous-éléments List-View

Chaque élément d’un contrôle List-View a une icône, une étiquette, un état actuel et une valeur définie par l’application. En utilisant des messages de liste, vous pouvez ajouter, modifier et supprimer des éléments, ainsi que récupérer des informations sur les éléments.

Chaque élément peut avoir un ou plusieurs sous- *éléments*. Un sous-élément est une chaîne qui, en mode rapport, s’affiche dans une colonne distincte de l’icône et de l’étiquette de l’élément. Pour spécifier le texte d’un sous-élément, utilisez le message [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md) ou [**LVM \_ SETITEM**](lvm-setitem.md) . Tous les éléments d’un contrôle List-View ont le même nombre de sous-éléments. Le nombre de sous-éléments est déterminé par le nombre de colonnes dans le contrôle List-View. Lorsque vous ajoutez une colonne à un contrôle List-View, vous spécifiez son index de sous-élément associé.

La structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) définit un élément de vue de liste ou un sous-élément. Le membre **iItem** est l’index de base zéro de l’élément. Le membre **iSubItem** est l’index de base un d’un sous-élément ou zéro si la structure contient des informations sur un élément. Les membres supplémentaires spécifient le texte, l’icône, l’État et les données d’élément de l’élément. Les *données d’élément* sont une valeur définie par l’application associée à un élément de vue de liste.

Pour ajouter un élément à un contrôle List View, utilisez le message [**LVM \_ INSERTITEM**](lvm-insertitem.md) , en spécifiant l’adresse d’une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Avant d’ajouter plusieurs éléments, vous pouvez envoyer au contrôle un message [**\_ SETITEMCOUNT LVM**](lvm-setitemcount.md) , en spécifiant le nombre d’éléments que le contrôle doit finalement contenir. Ce message permet au contrôle de vue de liste de réallouer ses structures de données internes une seule fois plutôt qu’à chaque fois que vous ajoutez un élément. Vous pouvez déterminer le nombre d’éléments dans un contrôle List-View en utilisant le message [**LVM \_ GETITEMCOUNT**](lvm-getitemcount.md) . Si vous ajoutez un grand nombre d’éléments à un contrôle List-View, vous pouvez accélérer le processus en désactivant le redessinage avant d’ajouter les éléments, puis activer le redessin après l’ajout des éléments. Utilisez le message [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw) pour activer et désactiver le rafraîchissement.

Pour modifier les attributs d’un élément de liste, utilisez le message [**LVM \_ SETITEM**](lvm-setitem.md) , en spécifiant l’adresse d’une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Le membre de **masque** de cette structure spécifie les attributs d’élément que vous souhaitez modifier. Par exemple, pour modifier uniquement le texte d’un élément ou d’un sous-élément, utilisez le message [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md) .

Pour extraire des informations sur un élément de liste, utilisez le message [**LVM \_ GETITEM**](lvm-getitem.md) , en spécifiant l’adresse de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) à remplir. Le membre de **masque** de cette structure spécifie les attributs d’élément à récupérer. Pour récupérer uniquement le texte d’un élément ou d’un sous-élément, utilisez le message [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) .

Pour supprimer un élément de liste, utilisez le message [**LVM \_ DELETEITEM**](lvm-deleteitem.md) . Vous pouvez supprimer tous les éléments d’un contrôle List-View en utilisant le message [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) .

### <a name="list-view-item-states"></a>États de l’élément List-View

L’état d’un élément est une valeur qui spécifie la disponibilité de l’élément, indique les actions de l’utilisateur ou reflète l’état de l’élément. Un contrôle List-View modifie certains bits d’État, par exemple lorsque l’utilisateur sélectionne un élément. Une application peut modifier d’autres bits d’État pour désactiver ou masquer l’élément ou pour spécifier une image de superposition ou une image d’État. Pour plus d’informations sur les images de superposition et les images d’État, consultez listes d’images [en mode liste](#list-view-image-lists).

L’état d’un élément est spécifié par le membre d' **État** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Lorsque vous spécifiez ou modifiez l’état d’un élément, le membre **stateMask** spécifie les bits d’État que vous devez modifier. Vous pouvez modifier l’état d’un élément à l’aide du message [**LVM \_ SETITEMSTATE**](lvm-setitemstate.md) . Vous pouvez spécifier l’état d’un élément lorsque vous le créez ou lorsque vous modifiez ses attributs à l’aide du message [**LVM \_ SETITEM**](lvm-setitem.md) . Pour déterminer l’état actuel d’un élément, utilisez le message [**LVM \_ GETITEMSTATE**](lvm-getitemstate.md) ou [**LVM \_ GETITEM**](lvm-getitem.md) .

Pour définir l’image de superposition d’un élément, le membre **stateMask** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) doit inclure la valeur [**\_ OVERLAYMASK Lvis**](list-view-item-states.md) et le membre d' **État** doit inclure l’index de base un de l’image de superposition décalée vers la gauche 8 bits à l’aide de la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . L’index peut être égal à zéro pour ne spécifier aucune image de superposition.

Pour définir l’image d’état d’un élément, le membre **stateMask** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) doit inclure la valeur [**\_ STATEIMAGEMASK Lvis**](list-view-item-states.md) et le membre d' **État** doit inclure l’index de base un de l’image d’État décalée vers la gauche 12 bits à l’aide de la macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) . L’index peut être égal à zéro pour ne spécifier aucune image d’État.

### <a name="callback-items-and-the-callback-mask"></a>Éléments de rappel et masque de rappel

Pour chacun de ses éléments, un contrôle List-View stocke généralement le texte de l’étiquette, l’index de la liste d’images des icônes de l’élément et un jeu d’indicateurs binaires pour l’état de l’élément. Vous pouvez définir des éléments de rappel ou modifier le masque de rappel du contrôle pour indiquer que l’application, plutôt que le contrôle, stocke une partie ou la totalité de ces informations. Vous souhaiterez peut-être utiliser des rappels si votre application stocke certaines de ces informations.

Un *élément de rappel* dans un contrôle List-View est un élément pour lequel l’application stocke le texte ou l’index de l’icône, ou les deux. Vous pouvez définir des éléments de rappel lorsque vous envoyez le message du [**LVM \_ INSERTITEM**](lvm-insertitem.md) pour ajouter un élément au contrôle List-View. Si l’application stocke le texte pour l’élément ou le sous-élément, définissez le membre **pszText** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) de l’élément sur **LPSTR \_ TEXTCALLBACK**. Si l’application stocke l’index d’icône d’un élément, définissez le membre **IImage** de la structure **LVITEM** de l’élément sur **I \_ IMAGECALLBACK**.

Le *masque de rappel* d’un contrôle List-View est un jeu d’indicateurs binaires qui spécifient les États de l’élément pour lesquels l’application, plutôt que le contrôle, stocke les données actuelles. Le masque de rappel s’applique à tous les éléments du contrôle, contrairement à la désignation de l’élément de rappel, qui s’applique à un élément spécifique. Le masque de rappel a la valeur zéro par défaut, ce qui signifie que le contrôle List-View stocke toutes les informations sur l’état de l’élément. Après avoir créé un contrôle List-View et initialisé ses éléments, vous pouvez envoyer le [**message \_ SETCALLBACKMASK LVM**](lvm-setcallbackmask.md) pour modifier le masque de rappel. Pour récupérer le masque de rappel actuel, envoyez le message [**\_ GETCALLBACKMASK LVM**](lvm-getcallbackmask.md) .

Quand un contrôle List-View doit afficher ou trier un élément de vue liste pour lequel l’application stocke des informations de rappel, le contrôle envoie le code de notification [LVN \_ GETDISPINFO](lvn-getdispinfo.md) à la fenêtre parente du contrôle. Ce message spécifie une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) qui contient le type d’informations requis et identifie l’élément ou le sous-élément à récupérer. La fenêtre parente doit traiter LVN \_ GETDISPINFO pour fournir les données demandées.

Si le contrôle d’affichage de liste détecte une modification dans les informations de rappel d’un élément, telles qu’une modification du texte, de l’icône ou des informations d’État, le contrôle envoie un code de notification [LVN \_ SETDISPINFO](lvn-setdispinfo.md) pour vous avertir de la modification.

Si vous modifiez les attributs ou les bits d’état d’un élément de rappel, vous utilisez le message de [**\_ mise à jour LVM**](lvm-update.md) pour forcer le contrôle à repeindre l’élément. Ce message fait également en sorte que le contrôle réorganise ses éléments s’il a le style [**\_ AutoArrange LVS**](list-view-window-styles.md) . Vous pouvez utiliser le message [**LVM \_ REDRAWITEMS**](lvm-redrawitems.md) pour redessiner une plage d’éléments en invalidant les parties correspondantes de la zone cliente du contrôle List-View.

En utilisant efficacement les éléments de rappel et le masque de rappel, vous pouvez vous assurer que chaque attribut d’élément est conservé dans un seul emplacement. Cela peut simplifier votre application, mais le seul espace enregistré est la mémoire qui serait autrement nécessaire pour stocker des étiquettes d’élément et du texte de sous-élément.

### <a name="list-view-item-position"></a>Position de l’élément de List-View

Chaque élément de l’affichage de liste a une position et une taille que vous pouvez récupérer et définir à l’aide de messages. Vous pouvez également déterminer l’élément, le cas échéant, à une position spécifiée. La position des éléments de mode liste est spécifiée dans les coordonnées de la *vue*, qui correspondent aux coordonnées clientes qui sont décalées par la position de défilement.

Pour récupérer et définir la position d’un élément, utilisez les messages [**LVM \_ GETITEMPOSITION**](lvm-getitemposition.md) et [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) . **LVM \_ GETITEMPOSITION** fonctionne pour tous les affichages, mais **LVM \_ SETITEMPOSITION** fonctionne uniquement pour les affichages icône et petite icône.

Vous pouvez déterminer l’élément, le cas échéant, situé à un emplacement particulier à l' [**aide \_ du message lvm lvm**](lvm-hittest.md) .

Pour récupérer le rectangle englobant d’un élément de liste ou uniquement pour son icône ou son étiquette, utilisez le message [**LVM \_ GETITEMRECT**](lvm-getitemrect.md) .

### <a name="arranging-sorting-and-finding-items"></a>Organisation, tri et recherche d’éléments

Vous pouvez utiliser des messages d’affichage de liste pour organiser et trier des éléments et pour rechercher des éléments en fonction de leurs attributs ou positions. L’organisation repositionne les éléments pour les aligner sur une grille, mais les index des éléments ne changent pas. Le tri modifie la séquence d’éléments (et leurs index correspondants), puis les repositionne en conséquence. Vous pouvez organiser les éléments uniquement dans les affichages icône et petite icône, mais vous pouvez trier les éléments dans n’importe quelle vue. Pour rechercher des éléments, vous envoyez des messages de vue de liste qui spécifient un emplacement ou une propriété de l’élément.

Pour réorganiser les éléments, utilisez le message de [**\_ réorganisation LVM**](lvm-arrange.md) . Vous pouvez vous assurer que les éléments sont disposés à tout moment en spécifiant le style de la fenêtre de [**\_ réorganisation LVS**](list-view-window-styles.md) .

Pour trier les éléments, utilisez le message [**LVM \_ SORTITEMS**](lvm-sortitems.md) . Quand vous triez à l’aide de ce message, vous spécifiez une fonction de rappel définie par l’application appelée par le contrôle List-View pour comparer l’ordre relatif de deux éléments quelconques. Le contrôle passe à la fonction de comparaison les données d’élément associées à chacun des deux éléments. Les données de l’élément sont la valeur spécifiée dans le membre **lParam** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) de l’élément lorsqu’il a été inséré dans la liste. En spécifiant les données d’élément appropriées et en fournissant une fonction de comparaison appropriée, vous pouvez trier les éléments en fonction de leur étiquette, de n’importe quel sous-élément ou de toute autre propriété. Notez que le tri des éléments ne réorganise pas les sous-éléments correspondants. Lorsque les éléments sont réorganisés, leurs sous-éléments correspondants sont transportés avec eux. autrement dit, les lignes entières sont conservées ensemble. Pour trier les colonnes séparément les unes des autres, en détachant les sous-éléments de leurs éléments, vous devez régénérer les colonnes après le tri à l’aide de [**LVM \_ SETITEM**](lvm-setitem.md).

Vous pouvez vous assurer qu’un contrôle List-View est toujours trié en spécifiant le style de fenêtre [**LVS \_ SORTASCENDING**](list-view-window-styles.md) ou [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) . Les contrôles avec ces styles utilisent le texte d’étiquette des éléments pour les trier par ordre croissant ou décroissant. Vous ne pouvez pas fournir de fonction de comparaison lorsque vous utilisez ces styles de fenêtre. Si un contrôle List-View possède l’un de ces styles, un message d' [**\_ INSERTITEM LVM**](lvm-insertitem.md) échoue si vous essayez d’insérer un élément qui a **LPSTR \_ TEXTCALLBACK** comme membre **pszText** de sa structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

Vous pouvez rechercher un élément de liste avec des propriétés spécifiques à l’aide du message [**LVM \_ FINDITEM**](lvm-finditem.md) . Vous pouvez trouver un élément de vue liste qui est dans un état spécifié et qui a une relation spécifiée avec un élément donné à l’aide du message [**\_ GETNEXTITEM LVM**](lvm-getnextitem.md) . Par exemple, vous pouvez récupérer l’élément sélectionné suivant à droite d’un élément spécifié.

## <a name="list-view-columns"></a>List-View les colonnes

Les colonnes contrôlent la façon dont les éléments et leurs sous-éléments sont affichés dans la vue rapport. Chaque colonne a un titre et une largeur et est associée à un sous-élément spécifique ; le sous-élément zéro est l’icône et l’étiquette de l’élément. Les attributs d’une colonne sont définis par une structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) .

Pour ajouter une colonne à un contrôle List View, utilisez le message [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) . Pour supprimer une colonne, utilisez le message [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .

> [!Note]  
> La suppression de la colonne zéro d’un contrôle List-View est uniquement prise en charge dans ComCtl32.dll version 6 et versions ultérieures. La version 5 prend également en charge la suppression de la colonne zéro, mais uniquement après avoir utilisé [**CCM \_ SETVERSION**](ccm-setversion.md) pour définir la version sur 5 ou version ultérieure. Les versions antérieures à la version 5 ne prennent pas en charge la suppression de la colonne zéro.

 

Vous pouvez récupérer et modifier les propriétés d’une colonne existante à l’aide des messages [**LVM \_ GETCOLUMN**](lvm-getcolumn.md) et [**LVM \_ SETCOLUMN**](lvm-setcolumn.md) . Pour récupérer ou modifier la largeur d’une colonne, utilisez les messages [**LVM \_ GETCOLUMNWIDTH**](lvm-getcolumnwidth.md) et [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) .

À moins que le style de fenêtre [**LVS \_ NOCOLUMNHEADER**](list-view-window-styles.md) soit spécifié, les en-têtes de colonne s’affichent dans la vue rapport. L’utilisateur peut cliquer sur un en-tête de colonne, provoquant l’envoi d’un code de notification [**LVN \_ COLUMNCLICK**](lvn-columnclick.md) à la fenêtre parente. En règle générale, la fenêtre parente trie le contrôle d’affichage de liste selon la colonne spécifiée lorsque ce clic se produit. L’utilisateur peut également faire glisser les repères de colonne entre les en-têtes pour dimensionner les colonnes.

Les contrôles List-View peuvent afficher des images en regard des titres des colonnes. Pour implémenter cette fonctionnalité, spécifiez la valeur de l' **\_ image LVCF** et assignez l’index de l’image au membre **IImage** dans la structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) .

Les contrôles List-View peuvent définir l’ordre dans lequel les colonnes sont affichées. Pour implémenter cette fonctionnalité, spécifiez la valeur d' **\_ ordre LVCF** et affectez l’ordre des colonnes au membre **IOrder** dans la structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) . L’ordre des colonnes est de base zéro et est dans l’ordre de gauche à droite. Par exemple, la valeur zéro indique la colonne la plus à gauche.

## <a name="list-view-scroll-position"></a>Position de défilement List-View

À moins que le style de fenêtre [**LVS \_ NoScroll**](list-view-window-styles.md) ne soit spécifié, un contrôle List-View peut faire l’objet d’un défilement pour afficher plus d’éléments que la zone cliente du contrôle ne peut en contenir. Vous pouvez récupérer la position de défilement d’un contrôle List-View et les informations connexes, faire défiler un contrôle d’affichage de liste d’une valeur spécifiée, ou faire défiler un contrôle List View pour qu’un élément de liste spécifié soit visible.

En mode icône ou petite icône, la position de défilement actuelle est définie par l' *origine* de la vue. L’origine de la vue est l’ensemble de coordonnées, par rapport à la zone visible du contrôle List-View, qui correspond aux coordonnées de la vue (0,0). Pour récupérer l’origine de la vue actuelle, utilisez le message [**LVM \_ GETORIGIN**](lvm-getorigin.md) . Ce message doit être utilisé uniquement en mode icône ou petite icône ; elle retourne une erreur dans la vue liste ou rapport.

Dans la vue liste ou rapport, la position de défilement actuelle est définie par l' *index de niveau supérieur*. L’index supérieur est l’index du premier élément visible dans le contrôle List-View. Pour récupérer l’index actuel, utilisez le message [**LVM \_ GETTOPINDEX**](lvm-gettopindex.md) . Ce message retourne un résultat valide uniquement dans une vue de liste ou de rapport ; elle retourne zéro en mode icône ou petite icône.

Vous pouvez utiliser le message [**LVM \_ GETVIEWRECT**](lvm-getviewrect.md) pour récupérer le rectangle englobant de tous les éléments d’un contrôle List-View, par rapport à la zone visible du contrôle.

Le [**message \_ GETCOUNTPERPAGE LVM**](lvm-getcountperpage.md) retourne le nombre d’éléments qui tiennent dans une page du contrôle List-View. Ce message retourne un résultat valide uniquement dans les vues de liste et de rapport ; dans les affichages icône et petite icône, retourne le nombre total d’éléments.

Pour faire défiler un contrôle d’affichage de liste d’une quantité spécifique, utilisez le message de [**\_ défilement LVM**](lvm-scroll.md) . À l’aide du message [**\_ ENSUREVISIBLE LVM**](lvm-ensurevisible.md) , vous pouvez faire défiler le contrôle List-View, si nécessaire, pour vous assurer qu’un élément spécifié est visible.

## <a name="list-view-label-editing"></a>Modification des étiquettes List-View

Un contrôle List-View avec le style de fenêtre [**LVS \_ EDITLABELS**](list-view-window-styles.md) permet à un utilisateur de modifier des étiquettes d’élément sur place. L’utilisateur commence la modification en cliquant sur l’étiquette d’un élément qui a le focus. Une application peut également commencer la modification automatiquement à l’aide du message [**LVM \_ EDITLABEL**](lvm-editlabel.md) . Le contrôle List-View notifie la fenêtre parente lorsque la modification commence et lorsqu’elle est annulée ou terminée. Lorsque la modification est terminée, la fenêtre parente est chargée de mettre à jour l’étiquette de l’élément, le cas échéant.

Lorsque la modification d’étiquette commence, un [contrôle d’édition](edit-controls.md) est créé, positionné et initialisé. Avant qu’il ne soit affiché, le contrôle List-View envoie sa fenêtre parente à un code de notification [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) . Si vous avez besoin de modifier le processus de modification des étiquettes, vous pouvez implémenter un gestionnaire pour cette notification.

Une utilisation pour un gestionnaire de notification [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) consiste à contrôler les étiquettes que l’utilisateur peut modifier. Pour empêcher la modification des étiquettes, retournez une valeur différente de zéro. Pour personnaliser la modification des étiquettes, vous devez faire en sorte que le gestionnaire de notification récupère un handle pour le contrôle d’édition en envoyant un message [**\_ GETEDITCONTROL LVM**](lvm-geteditcontrol.md) au contrôle List-View. Une fois que vous disposez de ce handle, vous pouvez personnaliser le contrôle d’édition en envoyant les messages EM xxx habituels \_ . Par exemple, pour limiter la quantité de texte qu’un utilisateur peut entrer, envoyez le contrôle d’édition à un message [**em \_ LIMITTEXT**](em-limittext.md) . Vous pouvez modifier le texte par défaut du contrôle d’édition avec [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta). Vous pouvez même sous-définir le contrôle d’édition pour intercepter et ignorer les caractères non valides.

Lorsque la modification d’étiquette est annulée ou terminée, un contrôle de liste d’affichage envoie sa fenêtre parente à un code de notification [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) . Le paramètre *lParam* est l’adresse d’une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Le membre d' **élément** de cette structure est une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dont le membre **iItem** identifie l’élément. Si la modification est annulée, le membre **pszText** de la structure **LVITEM** est **null**; Sinon, **pszText** est l’adresse du texte modifié. La fenêtre parente est responsable de la mise à jour de l’étiquette de l’élément si elle souhaite conserver la nouvelle étiquette.

## <a name="list-view-colors"></a>List-View les couleurs

Une application peut récupérer et définir trois couleurs pour un contrôle d’affichage de liste.



| Color                   | Messages utilisés pour récupérer et définir des couleurs                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------|
| Couleur du texte              | [**LVM \_ GETTEXTCOLOR**](lvm-gettextcolor.md), [ **LVM \_ SETTEXTCOLOR**](lvm-settextcolor.md)         |
| Couleur d’arrière-plan du texte   | [**LVM \_ GETTEXTBKCOLOR**](lvm-gettextbkcolor.md), [ **LVM \_ SETTEXTBKCOLOR**](lvm-settextbkcolor.md) |
| Couleur d’arrière-plan de la fenêtre | [**LVM \_ GETBKCOLOR**](lvm-getbkcolor.md), [ **LVM \_ SETBKCOLOR**](lvm-setbkcolor.md)                 |



 

Pour personnaliser l’apparence d’un contrôle List-View de manière plus significative, utilisez [ \_ CUSTOMDRAW nm (mode liste)](nm-customdraw-list-view.md) ou utilisez des styles visuels (consultez [styles](themes-overview.md) visuels et [activation des styles visuels](cookbook-overview.md)).

## <a name="arranging-list-items-by-group"></a>Organisation des éléments de liste par groupe

Les fonctionnalités de regroupement du contrôle List-View vous permettent de regrouper visuellement des ensembles d’éléments liés de manière logique. Les groupes peuvent être créés en fonction des propriétés, des attributs ou d’autres caractéristiques de l’élément. Ces groupes sont généralement séparés sur l’écran par un en-tête horizontal qui contient le nom du groupe. La capture d’écran suivante montre des éléments groupés.

![capture d’écran d’un contrôle List-View, avec des chiens dans un groupe et des chats dans un autre groupe](images/lv-groups.png)

Vous utilisez la structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) pour stocker des informations sur un groupe, telles que le texte d’en-tête et de pied de page, l’état actuel du groupe, et ainsi de suite. L’API de regroupement comprend des messages qui vous permettent de gérer des groupes et des éléments de groupe en ajoutant des éléments à des groupes, en ajoutant des groupes aux affichages, en triant des éléments de groupe et en interrogeant des groupes pour la taille d’élément et d’autres informations. Par exemple, vous pouvez définir et récupérer des paramètres d’affichage pour chaque groupe à l’aide des macros [**ListView \_ SetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupmetrics) et [**ListView \_ GetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupmetrics) .

Le regroupement est disponible dans toutes les vues, à l’exception de la vue liste. Elle n’est pas disponible sur les contrôles qui ont le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

Pour plus d’informations, consultez [utilisation de contrôles List-View](using-list-view-controls.md).

## <a name="insertion-marks"></a>Marques d’insertion

Les marques d’insertion montrent les utilisateurs où les éléments déplacés seront placés. Les marques d’insertion s’affichent actuellement lorsque l’utilisateur fait glisser un élément dans le menu **Démarrer** ou la barre de lancement rapide. La marque d’insertion fonctionne également pour les listes qui sont configurées pour se réorganiser. Quand un utilisateur fait glisser un élément vers un point entre deux autres éléments, la marque d'insertion indique le nouvel emplacement prévu de l'élément. La capture d’écran suivante montre une marque d’insertion.

![capture d’écran montrant une marque d’insertion lors du glissement d’un fichier entre deux autres dans un contrôle List-View](images/insertmark.png)

Les éléments d’API de marque d’insertion permettent de placer des marques d’insertion en fournissant des messages et des indicateurs qui effectuent la détection des accès, qui spécifient l’emplacement et l’apparence de la marque d’insertion par élément, et qui recherchent des informations sur la taille et l’apparence actuelles de la marque d’insertion.

## <a name="see-also"></a>Voir aussi

* [Exemple de contrôle ListView virtuel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)
