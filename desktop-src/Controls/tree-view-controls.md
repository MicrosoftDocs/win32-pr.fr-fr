---
title: À propos des contrôles Tree-View
description: Un contrôle Tree-View est une fenêtre qui affiche une liste hiérarchique d’éléments, tels que les en-têtes d’un document, les entrées d’un index ou les fichiers et répertoires d’un disque.
ms.assetid: 10cc7949-dd77-412d-bad1-db8d8a049582
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08743a7ac138a6cea5f766dd91aee2ec714acc2d4c8b98e1f2bee26c42ff9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769811"
---
# <a name="about-tree-view-controls"></a>À propos des contrôles Tree-View

Un contrôle Tree-View est une fenêtre qui affiche une liste hiérarchique d’éléments, tels que les en-têtes d’un document, les entrées d’un index ou les fichiers et répertoires d’un disque. Chaque élément est constitué d’une étiquette et d’une image bitmap facultative, et chaque élément peut être associé à une liste de sous-éléments. En cliquant sur un élément, l’utilisateur peut développer ou réduire la liste associée de sous-éléments.

L’illustration suivante montre un contrôle d’arborescence simple avec un nœud racine, un nœud développé et un nœud réduit. Le contrôle utilise une image bitmap pour l’élément sélectionné et une autre image bitmap pour d’autres éléments.

![capture d’écran montrant cinq nœuds dans une hiérarchie ; le texte d’un nœud est sélectionné, mais les nœuds ne sont pas liés les uns aux autres par des lignes](images/tv-simple.png)

Après avoir créé un contrôle d’arborescence, vous pouvez ajouter, supprimer, réorganiser ou manipuler des éléments en envoyant des messages au contrôle. Chaque message comporte une ou plusieurs macros correspondantes que vous pouvez utiliser au lieu d’envoyer le message explicitement.

Les rubriques suivantes sont présentées dans cette section.

-   [Styles d’arborescence](#tree-view-styles)
-   [Éléments parents et enfants](#parent-and-child-items)
-   [Étiquettes d’élément](#item-labels)
-   [Modification des étiquettes d’arborescence](#tree-view-label-editing)
-   [Position de l’élément d’arborescence](#tree-view-item-position)
-   [Vue d’ensemble des États des éléments d’arborescence](#tree-view-item-states-overview)
-   [Sélection de l’élément](#item-selection)
-   [Informations sur l’élément](#item-information)
-   [Listes d’images en mode arborescence](#tree-view-image-lists)
-   [Opérations de glisser-déplacer](#drag-and-drop-operations)
-   [Messages de notification de contrôle d’arborescence](#tree-view-control-notification-messages)
-   [Traitement par défaut des messages de contrôle Tree-View](#default-tree-view-control-message-processing)
-   [Rubriques connexes](#related-topics)

## <a name="tree-view-styles"></a>Styles de Tree-View

Les styles d’arborescence gouvernent les aspects de l’apparence d’un contrôle Tree-View. Vous définissez les styles initiaux lorsque vous créez le contrôle Tree-View. Vous pouvez récupérer et modifier les styles après avoir créé le contrôle Tree-View à l’aide des fonctions [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) et [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

Le style [**TV \_ HASLINES**](tree-view-control-window-styles.md) améliore la représentation graphique d’une hiérarchie de contrôle Tree-View en dessinant des lignes qui lient des éléments enfants à leur élément parent, comme indiqué dans l’illustration suivante.

![capture d’écran montrant la disposition précédente, mais avec des lignes joignant les nœuds ; la première ligne descend du nœud racine.](images/tv-haslines.png)

En soi, ce style ne dessine pas de lignes à la racine de la hiérarchie. Pour ce faire, vous devez combiner les styles [**TV \_ HASLINES**](tree-view-control-window-styles.md) et [**TV \_ LINESATROOT**](tree-view-control-window-styles.md) . Le résultat est représenté dans l’illustration suivante.

![capture d’écran montrant la disposition précédente, mais avec une ligne horizontale supplémentaire menant au nœud racine](images/tv-rootlines.png)

L‘utilisateur peut développer ou réduire la liste des éléments enfants d‘un élément parent en double-cliquant sur l‘élément parent. Un contrôle d’arborescence avec le style [**TV \_ HASBUTTONS**](tree-view-control-window-styles.md) style ajoute un bouton à gauche de chaque élément parent. L’utilisateur peut cliquer sur le bouton une fois au lieu de double-cliquer sur l’élément parent pour développer ou réduire l’enfant. **Téléviseurs \_ HASBUTTONS** n’ajoute pas de boutons aux éléments situés à la racine de la hiérarchie. Pour ce faire, vous devez combiner les [**téléviseurs \_ HASLINES**](tree-view-control-window-styles.md), les téléviseurs [**\_ LINESATROOT**](tree-view-control-window-styles.md)et les **téléviseurs \_ HASBUTTONS**. Cette combinaison de styles est présentée dans l’illustration suivante.

![capture d’écran montrant la disposition précédente, mais avec des boutons de développement/réduction à chaque vertex de deux lignes](images/tv-hasbuttons.png)

Le style de [**\_ cases à cocher TV**](tree-view-control-window-styles.md) crée des cases à cocher en regard de chaque élément. Si vous souhaitez utiliser le style de case à cocher, vous devez définir le style de **\_ cases à cocher TV** (avec [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)) après avoir créé le contrôle d’arborescence et avant de remplir l’arborescence. Dans le cas contraire, les cases à cocher peuvent apparaître désactivées, en fonction des problèmes de synchronisation. L’illustration suivante montre le style de case à cocher.

![capture d’écran montrant l’organisation précédente, mais avec une case à cocher en regard de chaque nœud ; deux cases à cocher sont sélectionnées](images/tv-haschecks.png)

Le style [**TV \_ FULLROWSELECT**](tree-view-control-window-styles.md) affiche la mise en surbrillance de la sélection pour s’étendre sur toute la largeur du contrôle, et pas seulement sur l’élément lui-même. L’illustration suivante montre ce style.

![capture d’écran montrant la disposition d’origine de cinq nœuds sans lignes, mais la sélection de la sélection étend la largeur complète du contrôle](images/tv-fullrow.png)

Le style [**TV \_ EDITLABELSs**](tree-view-control-window-styles.md) permet à l’utilisateur de modifier les étiquettes des éléments de l’arborescence. Pour plus d’informations sur la modification des étiquettes, consultez Modification des étiquettes d' [arborescence](#tree-view-label-editing).

Pour plus d’informations sur ces styles et d’autres, consultez [styles de fenêtre de contrôle d’arborescence](tree-view-control-window-styles.md).

## <a name="parent-and-child-items"></a>Éléments parents et enfants

Tout élément d’un contrôle Tree-View peut avoir une liste de sous-éléments, appelés *éléments enfants*, qui lui est associé. Un élément qui a un ou plusieurs éléments enfants est appelé un *élément parent*. Un élément enfant est affiché sous son élément parent et est mis en retrait pour indiquer qu’il est subordonné au parent. Un élément qui n’a pas de parent apparaît en haut de la hiérarchie et est appelé *élément racine*.

Pour ajouter un élément à un contrôle Tree-View, envoyez le message [**TVM \_ INSERTITEM**](tvm-insertitem.md) au contrôle. Le message retourne un handle vers le type HTREEITEM, qui identifie de façon unique l’élément. Lorsque vous ajoutez un élément, vous devez spécifier le descripteur de l’élément parent du nouvel élément. Si vous spécifiez la valeur **null** ou la \_ valeur racine TVI à la place d’un descripteur d’élément parent dans la structure [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , l’élément est ajouté en tant qu’élément racine.

À tout moment, l‘état d‘une liste d‘éléments parents pour des éléments enfants peut être développé ou réduit. Lorsque l’état est développé, les éléments enfants apparaissent sous l’élément parent. Lorsqu'il est réduit, les éléments enfants ne sont pas affichés. La liste bascule automatiquement entre les États développés et réduits lorsque l’utilisateur double-clique sur l’élément parent ou, si le parent a le style [**TV \_ HASBUTTONS**](tree-view-control-window-styles.md) , lorsque l’utilisateur clique sur le bouton associé à l’élément parent. Une application peut développer ou réduire les éléments enfants à l’aide du message de [**\_ développement TVM**](tvm-expand.md) .

Un contrôle Tree-View envoie la fenêtre parente un message de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) lorsque la liste des éléments enfants d’un élément parent est sur le point d’être développée ou réduite. La notification donne à une application la possibilité d’empêcher la modification ou de définir des attributs de l’élément parent qui dépendent de l’état de la liste d’éléments enfants. Après avoir modifié l’état de la liste, le contrôle Tree-View envoie la fenêtre parente un message de notification [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .

Lorsqu’une liste d’éléments enfants est développée, elle est mise en retrait par rapport à l’élément parent. Vous pouvez définir la quantité de mise en retrait à l’aide du message [**TVM \_ SETINDENT**](tvm-setindent.md) ou récupérer la valeur actuelle à l’aide du message [**TVM \_ GETINDENT**](tvm-getindent.md) .

Un contrôle Tree-View utilise la mémoire allouée à partir du tas du processus qui crée le contrôle Tree-View. Le nombre maximal d’éléments dans une arborescence est basé sur la quantité de mémoire disponible dans le tas.

## <a name="item-labels"></a>Étiquettes d’élément

En général, vous spécifiez le texte de l’étiquette d’un élément lors de l’ajout de l’élément au contrôle Tree-View. Le message [**TVM \_ INSERTITEM**](tvm-insertitem.md) inclut une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui définit les propriétés de l’élément, y compris une chaîne contenant le texte de l’étiquette.

Un contrôle Tree-View alloue de la mémoire pour stocker chaque élément ; le texte des étiquettes d’élément occupe une partie importante de cette mémoire. Si votre application gère une copie des chaînes dans le contrôle Tree-View, vous pouvez réduire les besoins en mémoire du contrôle en spécifiant la \_ valeur LPSTR TEXTCALLBACK dans le membre **PszText** de [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) au lieu de passer des chaînes réelles à l’arborescence. L’utilisation de LPSTR \_ TEXTCALLBACK fait en sorte que le contrôle d’arborescence récupère le texte de l’étiquette d’un élément à partir de la fenêtre parente chaque fois que l’élément doit être redessiné. Pour récupérer le texte, le contrôle d’arborescence envoie un message de notification [TVN \_ GETDISPINFO](tvn-getdispinfo.md) , qui comprend l’adresse d’une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . La fenêtre parente doit remplir les membres appropriés de la structure incluse.

## <a name="tree-view-label-editing"></a>Modification des étiquettes Tree-View

L’utilisateur peut modifier directement les étiquettes des éléments dans un contrôle Tree-View qui a le style [**TV \_ EDITLABELS**](tree-view-control-window-styles.md) . L’utilisateur commence la modification en cliquant sur l’étiquette de l’élément qui a le focus. Une application commence la modification à l’aide du message [**TVM \_ EDITLABEL**](tvm-editlabel.md) . Le contrôle Tree-View notifie la fenêtre parente lorsque la modification commence et lorsqu’elle est annulée ou terminée. Lorsque la modification est terminée, la fenêtre parente est chargée de mettre à jour l’étiquette de l’élément, le cas échéant.

Lorsque la modification d’étiquette commence, un contrôle Tree-View envoie sa fenêtre parente un message de notification [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) . En traitant cette notification, une application peut autoriser la modification de certaines étiquettes et empêcher la modification des autres. Si vous retournez la valeur zéro, la modification est retournée, et la valeur différente de zéro l’empêche.

Lorsque la modification d’étiquette est annulée ou terminée, un contrôle d’arborescence envoie sa fenêtre parente à un message de notification [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) . Le paramètre *lParam* est l’adresse d’une structure [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . Le paramètre *Item* est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui identifie l’élément et comprend le texte modifié. La fenêtre parente est responsable de la mise à jour de l’étiquette de l’élément s’il souhaite conserver la nouvelle étiquette. Le membre **pszText** de **TVITEM** est égal à zéro si la modification est annulée.

Pendant la modification des étiquettes, en général en réponse au message de notification [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) , vous pouvez récupérer le handle du contrôle d’édition utilisé pour la modification des étiquettes à l’aide du message [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) . Vous pouvez envoyer au contrôle d’édition un message [**em \_ SETLIMITTEXT**](em-setlimittext.md) pour limiter la quantité de texte qu’un utilisateur peut entrer ou sous-classer le contrôle d’édition pour intercepter et ignorer les caractères non valides. Notez, toutefois, que le contrôle d’édition s’affiche uniquement *après* l’envoi de TVN \_ BEGINLABELEDIT.

## <a name="tree-view-item-position"></a>Position de l’élément de Tree-View

La position initiale d’un élément est définie lorsque l’élément est ajouté au contrôle Tree-View à l’aide du message [**TVM \_ INSERTITEM**](tvm-insertitem.md) . Le message comprend une structure [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) qui spécifie le descripteur de l’élément parent et le handle de l’élément après lequel le nouvel élément doit être inséré. Le deuxième descripteur doit identifier soit un élément enfant du parent donné, soit l’une des valeurs suivantes : TVI \_ First, TVI \_ Last ou TVI \_ sort.

Quand TVI \_ First ou TVI \_ Last est spécifié, le contrôle Tree-View place le nouvel élément au début ou à la fin de la liste des éléments enfants de l’élément parent donné. Quand TVI \_ sort est spécifié, le contrôle Tree-View insère le nouvel élément dans la liste des éléments enfants dans l’ordre alphabétique en fonction du texte des étiquettes d’élément.

Vous pouvez placer la liste des éléments enfants d’un élément parent dans l’ordre alphabétique à l’aide du message [**TVM \_ SORTCHILDREN**](tvm-sortchildren.md) . Le message comprend un paramètre qui spécifie si tous les niveaux d’éléments enfants décroissant de l’élément parent donné sont également triés par ordre alphabétique.

Le message [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) vous permet de trier des éléments enfants en fonction de critères que vous définissez. Lorsque vous utilisez ce message, vous spécifiez une fonction de rappel définie par l’application que le contrôle d’arborescence peut appeler chaque fois que l’ordre relatif de deux éléments enfants doit être déterminé. La fonction de rappel reçoit des valeurs définies par l’application 2 32 bits pour les éléments comparés et une troisième valeur 32 bits que vous spécifiez lors de l’envoi de **TVM \_ SORTCHILDRENCB**.

## <a name="tree-view-item-states-overview"></a>Présentation des États de Tree-View élément

Chaque élément d’un contrôle Tree-View a un état actuel. Les informations d’état de chaque élément incluent un jeu d’indicateurs binaires, ainsi que des index de liste d’images qui indiquent l’image d’état de l’élément et l’image de superposition. Les indicateurs binaires indiquent si l’élément est sélectionné, désactivé, développé et ainsi de suite. Pour l’essentiel, un contrôle d’arborescence définit automatiquement l’état d’un élément pour refléter les actions de l’utilisateur, telles que la sélection d’un élément. Toutefois, vous pouvez également définir l’état d’un élément à l’aide du message [**TVM \_ SETITEM**](tvm-setitem.md) , et vous pouvez récupérer l’état actuel d’un élément à l’aide du message [**TVM \_ GETITEM**](tvm-getitem.md) . Pour obtenir la liste complète des États des éléments, consultez [États des éléments de contrôle d’arborescence](tree-view-control-item-states.md).

L’état actuel d’un élément est spécifié par le membre d' **État** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) . Un contrôle d’arborescence peut modifier l’état d’un élément pour refléter une action de l’utilisateur, par exemple sélectionner l’élément ou définir le focus sur l’élément. En outre, une application peut modifier l'état d'un élément pour désactiver ou masquer l'élément ou pour spécifier une image de superposition ou d'état.

Lorsque vous spécifiez ou modifiez l’état d’un élément, le membre **statemask** de [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) spécifie les bits d’État à définir, et le membre d' **État** contient les nouvelles valeurs pour ces bits.

Pour définir l’image de superposition d’un élément, **statemask** doit inclure la valeur [**Tvis \_ OVERLAYMASK**](tree-view-control-item-states.md) et **State** doit inclure l’index de base un de l’image de superposition décalée vers la gauche 8 bits à l’aide de la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . L’index peut être égal à zéro pour ne spécifier aucune image de superposition.

Une image d’État s’affiche en regard de l’icône d’un élément pour indiquer un état défini par l’application. Les images d’État sont contenues dans une *liste d’images d’État* spécifiée par l’envoi d’un message [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) . Pour définir l’image d’état d’un élément, incluez la valeur [**\_ STATEIMAGEMASK Tvis**](tree-view-control-item-states.md) dans le membre **Statemask** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) . Les bits 12 à 15 du membre d' **État** de la structure spécifient l’index dans la liste d’images d’état de l’image à dessiner.

Pour définir l’index d’image d’État, utilisez [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask). Cette macro prend un index et définit les bits 12 à 15 de manière appropriée. Pour indiquer que l’élément n’a pas d’image d’État, définissez l’index sur zéro. Cette Convention signifie que l’image zéro dans la liste d’images d’État ne peut pas être utilisée comme image d’État. Pour isoler les bits 12 à 15 du membre d' **État** , utilisez le masque [**Tvis \_ STATEIMAGEMASK**](tree-view-control-item-states.md) . Pour plus d’informations sur les images de superposition et d’État, consultez [listes d’images en mode arborescence](#tree-view-image-lists).

## <a name="item-selection"></a>Sélection de l’élément

Un contrôle Tree-View notifie la fenêtre parente lorsque la sélection passe d’un élément à un autre en envoyant les messages de notification [TVN \_ SELCHANGING](tvn-selchanging.md) et [TVN \_ SELCHANGED](tvn-selchanged.md) . Les deux notifications incluent une valeur qui spécifie si la modification est le résultat d’un clic de souris ou d’une touche. Les notifications incluent également des informations sur l’élément qui obtient la sélection et l’élément qui perd la sélection. Vous pouvez utiliser ces informations pour définir des attributs d’élément qui dépendent de l’état de sélection de l’élément. Le retour de la **valeur true** en réponse à TVN \_ SELCHANGING empêche la sélection de changer et la **valeur false** autorise la modification.

Une application peut modifier la sélection en envoyant le message [**TVM \_ SELECTITEM**](tvm-selectitem.md) .

## <a name="item-information"></a>Informations sur l’élément

Les contrôles d’arborescence prennent en charge un certain nombre de messages qui récupèrent des informations sur les éléments du contrôle.

Le message [**TVM \_ GETITEM**](tvm-getitem.md) peut récupérer le handle et les attributs d’un élément. Les attributs d’un élément incluent son état actuel, les index dans la liste d’images du contrôle des images bitmap sélectionnées et non sélectionnées de l’élément, un indicateur qui indique si l’élément a des éléments enfants, l’adresse de la chaîne d’étiquette de l’élément et la valeur 32 bits définie par l’application de l’élément.

Le message [**TVM \_ GETNEXTITEM**](tvm-getnextitem.md) récupère l’élément d’arborescence qui porte la relation spécifiée à l’élément actuel. Le message peut récupérer le parent d’un élément, l’élément visible suivant ou précédent, le premier élément enfant, et ainsi de suite.

Le message [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) récupère le rectangle englobant d’un élément d’arborescence. Les messages [**TVM \_ GETCOUNT**](tvm-getcount.md) et [**TVM \_ GETVISIBLECOUNT**](tvm-getvisiblecount.md) récupèrent le nombre d’éléments dans un contrôle Tree-View et le nombre d’éléments pouvant être entièrement visibles dans la fenêtre du contrôle Tree-View, respectivement. Vous pouvez vous assurer qu’un élément particulier est visible à l’aide du message [**TVM \_ ENSUREVISIBLE**](tvm-ensurevisible.md) .

## <a name="tree-view-image-lists"></a>Tree-View les listes d’images

Chaque élément d’un contrôle Tree-View peut avoir quatre images bitmap qui lui sont associées.

-   Une image, telle qu’un dossier ouvert, s’affiche lorsque l’élément est sélectionné.
-   Une image, telle qu’un dossier fermé, s’affiche lorsque l’élément n’est pas sélectionné.
-   Image de superposition dessinée de façon transparente sur l’image sélectionnée ou non sélectionnée.
-   Image d’État, qui est une image supplémentaire affichée à gauche de l’image sélectionnée ou non sélectionnée. Vous pouvez utiliser des images d’État, telles que des cases à cocher activées et désactivées, pour indiquer les États des éléments définis par l’application.

Par défaut, un contrôle d’arborescence n’affiche pas d’images d’élément. Pour afficher des images d’élément, vous devez créer des listes d’images et les associer au contrôle. Pour plus d’informations sur les listes d’images, consultez [listes d’images](image-lists.md).

Un contrôle Tree-View peut avoir deux listes d’images : une liste d’images normales et une liste d’images d’État. Une liste d’images normale stocke les images sélectionnées, non sélectionnées et de superposition. Une liste d’images d’État stocke des images d’État. Utilisez la fonction [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) pour créer une liste d’images et utilisez d’autres fonctions de liste d’images pour ajouter des bitmaps à la liste d’images. Ensuite, pour associer la liste d’images au contrôle Tree-View, utilisez le message [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) . Le message [**TVM \_ GETIMAGELIST**](tvm-getimagelist.md) récupère un handle vers l’une des listes d’images d’un contrôle Tree-View. Ce message est utile si vous devez ajouter d’autres images à la liste.

En plus des images sélectionnées et non sélectionnées, la liste d’images normales d’un contrôle Tree-View peut contenir jusqu’à quatre images de superposition. Les images de superposition sont identifiées par un index de base un et sont conçues pour être dessinées de manière transparente sur les images sélectionnées et non sélectionnées. Pour affecter un index de masque de superposition à une image dans la liste d’images normales, appelez la fonction [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) .

Par défaut, tous les éléments affichent la première image dans la liste d’images normale pour les États sélectionnés et non sélectionnés. Par ailleurs, par défaut, les éléments n’affichent pas les images de superposition ou les images d’État. Vous pouvez modifier ces comportements par défaut pour un élément en envoyant le message [**TVM \_ INSERTITEM**](tvm-insertitem.md) ou [**TVM \_ SETITEM**](tvm-setitem.md) . Ces messages utilisent la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) pour spécifier des index de liste d’images pour un élément.

Pour spécifier les images sélectionnées et non sélectionnées d’un élément, définissez les \_ bits d’image TVIF SELECTEDIMAGE et TVIF \_ dans le membre **Mask** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) et spécifiez des index à partir de la liste d’images normale du contrôle dans les membres **iSelectImage** et **IImage** . Vous pouvez également spécifier la \_ valeur I IMAGECALLBACK dans **ISelectImage** et **IImage** au lieu de spécifier des index. Cela amène le contrôle à interroger sa fenêtre parente pour obtenir un index de liste d’images chaque fois que l’élément est sur le point d’être redessiné. Le contrôle envoie le message de notification [TVN \_ GETDISPINFO](tvn-getdispinfo.md) pour récupérer l’index.

Pour associer une image de superposition à un élément, utilisez la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) pour spécifier un index de masque de superposition dans le membre d' **État** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) de l’élément. Vous devez également définir les bits [**Tvis \_ OVERLAYMASK**](tree-view-control-item-states.md) dans le membre **stateMask** . Les index de masque de superposition sont basés sur un seul ; un index de zéro indique qu’aucune image de superposition n’a été spécifiée.

Les images d’État sont stockées dans une liste d’images d’État distincte et sont identifiées par leur index. Pour spécifier la liste d’images d’État, envoyez un message de [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) . Contrairement au contrôle List-View, qui utilise un index de base un pour identifier les images d’État, les images d’état de contrôle d’arborescence sont identifiées par un index de base zéro. Toutefois, un index de zéro indique que l’élément n’a pas d’image d’État. Par conséquent, l’image zéro ne peut pas être utilisée comme image d’État. Pour plus d’informations sur les États d’élément et les images d’État, consultez [vue d’ensemble des États d’élément d’arborescence](#tree-view-item-states-overview).

## <a name="drag-and-drop-operations"></a>Opérations de glisser-déplacer

Un contrôle Tree-View notifie la fenêtre parente lorsque l’utilisateur commence à faire glisser un élément. La fenêtre parente reçoit un message de notification [TVN \_ BEGINDRAG](tvn-begindrag.md) lorsque l’utilisateur commence à faire glisser un élément avec le bouton gauche de la souris et un message de notification [TVN \_ BEGINRDRAG](tvn-beginrdrag.md) lorsque l’utilisateur commence à faire glisser le bouton droit. Vous pouvez empêcher un contrôle d’affichage d’arborescence d’envoyer ces notifications en donnant au contrôle de l’arborescence le style [**\_ DISABLEDRAGDROP TV**](tree-view-control-window-styles.md) .

Vous obtenez une image à afficher pendant une opération glisser à l’aide du message [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) . Le contrôle Tree-View crée une image bitmap de glissement basée sur l’étiquette de l’élément déplacé. Le contrôle Tree-View crée ensuite une liste d’images, y ajoute le bitmap et retourne le handle à la liste d’images.

Vous devez fournir du code faisant glisser réellement l'élément. Cela implique généralement l’utilisation des fonctionnalités de glissement des fonctions de liste d’images et le traitement des messages [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) et [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (ou [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) envoyés à la fenêtre parente après le début de l’opération glisser.

Si les éléments d’un contrôle Tree-View doivent être les cibles des opérations de glisser-déplacer, vous devez savoir quand le pointeur de la souris se trouve sur un élément cible. Vous pouvez le trouver à l’aide du message [**TVM \_ HITTEST**](tvm-hittest.md) . Vous spécifiez l’adresse d’une structure [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) qui contient les coordonnées actuelles du pointeur de la souris. Quand la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retourne, la structure contient un indicateur qui spécifie l’emplacement du pointeur de la souris par rapport au contrôle Tree-View. Si le pointeur se trouve sur un élément dans le contrôle Tree-View, la structure contient également le handle de l’élément.

Vous pouvez indiquer qu’un élément est la cible d’une opération de glisser-déplacer en utilisant le message [**TVM \_ SETITEM**](tvm-setitem.md) pour définir l’État sur la valeur [**Tvis \_ DROPHILITED**](tree-view-control-item-states.md) . Un élément avec cet état est dessiné dans le style utilisé pour indiquer une cible de glissement-déplacement.

## <a name="tree-view-control-notification-messages"></a>Tree-View les messages de notification de contrôle

Un contrôle Tree-View envoie les messages de notification suivants à sa fenêtre parente sous la forme de messages de notification [**WM \_**](wm-notify.md) .



| Notification                                    | Description                                                                            |
|-------------------------------------------------|----------------------------------------------------------------------------------------|
| [TVN \_ BEGINDRAG](tvn-begindrag.md)             | Signale le début d’une opération de glisser-déplacer.                                        |
| [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md)   | Signale le début de la modification des étiquettes sur place.                                           |
| [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)           | Signale que le bouton droit de la souris a commencé une opération de glisser-déplacer.             |
| [TVN \_ DELETEITEM](tvn-deleteitem.md)           | Signale la suppression d’un élément spécifique.                                               |
| [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)       | Signale la fin de la modification de l’étiquette.                                                      |
| [TVN \_ GETDISPINFO](tvn-getdispinfo.md)         | Demande des informations nécessaires au contrôle d’arborescence pour afficher un élément.           |
| [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md)       | Signale que la liste des éléments enfants d’un élément parent a été développée ou réduite.            |
| [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md)     | Signale que la liste des éléments enfants d’un élément parent est sur le point d’être développée ou réduite. |
| [TVN \_](tvn-keydown.md)                 | Signale un événement de clavier.                                                              |
| [TVN \_ SELCHANGED](tvn-selchanged.md)           | Signale que la sélection est passée d’un élément à un autre.                       |
| [TVN \_ SELCHANGING](tvn-selchanging.md)         | Signale que la sélection est sur le point d’être modifiée d’un élément à un autre.            |
| [TVN \_ SETDISPINFO](tvn-setdispinfo.md)         | Avertit une fenêtre parente qu’elle doit mettre à jour les informations qu’elle gère pour un élément. |



 

## <a name="default-tree-view-control-message-processing"></a>Traitement par défaut des messages de contrôle Tree-View

Cette section décrit le traitement des messages de fenêtre effectué par un contrôle Tree-View. Les messages spécifiques aux contrôles d’arborescence sont décrits dans d’autres sections de ce document. ils ne sont donc pas inclus ici.



| Message                                            | Traitement effectué                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM, \_ commande**](/windows/desktop/menurc/wm-command)               | Traite les messages de notification du contrôle d’édition en cours de [ \_ mise à jour](en-update.md) et en [ \_ KILLFOCUS](en-killfocus.md) et transfère toutes les autres notifications de contrôle d’édition à la fenêtre parente. Il n'y a pas de valeur de retour.                                                                                                                                                                                                                                                                                                |
| [**création de WM \_**](/windows/desktop/winmsg/wm-create)                 | Alloue de la mémoire et initialise des structures de données internes. Retourne zéro en cas de réussite, ou-1 dans le cas contraire.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_destructeur WM**](/windows/desktop/winmsg/wm-destroy)               | Libère toutes les ressources système associées au contrôle. Elle retourne zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_activer WM**](/windows/desktop/winmsg/wm-enable)                 | Active ou désactive le contrôle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)         | Efface l’arrière-plan de la fenêtre à l’aide de la couleur d’arrière-plan actuelle pour le contrôle d’arborescence. Elle retourne **true**.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)         | Retourne une combinaison des valeurs DLGC \_ WANTARROWS et DLGC \_ WANTCHARS.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Retourne le handle de la police d’étiquette actuelle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**\_HSCROLL WM**](wm-hscroll.md)                  | Fait défiler le contrôle d’arborescence. Elle retourne la **valeur true** si le défilement se produit, ou **false** dans le cas contraire.                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM- \_ touche**](/windows/desktop/inputdev/wm-keydown)             | Envoie le message de notification [ \_ keyverse TVN](tvn-keydown.md) à la fenêtre parente pour toutes les clés. Envoie le message de notification [nm \_ de retour (arborescence)](nm-return-tree-view-.md) lorsque l’utilisateur appuie sur la touche entrée. Il déplace le signe insertion lorsque l’utilisateur appuie sur les touches de direction ou sur la touche PG. suiv, PG. suiv, début, fin ou retour arrière. Elle fait défiler le contrôle d’arborescence quand l’utilisateur appuie sur la touche CTRL en combinaison avec ces touches. Elle retourne la **valeur true** si une clé est traitée, ou **false** dans le cas contraire. |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)         | Repeint l’élément ayant le focus, le cas échéant, et envoie un message de notification [nm \_ KILLFOCUS (arborescence)](nm-killfocus-tree-view.md) à la fenêtre parente.                                                                                                                                                                                                                                                                                                                                                                  |
| [**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk) | Annule la modification des étiquettes et, si vous avez double-cliqué sur un élément, envoie le message de notification [nm \_ DBLCLK (arborescence)](nm-dblclk-tree-view.md) à la fenêtre parente. Si la fenêtre parente retourne 0, le contrôle Tree-View bascule l’état développé de l’élément, en envoyant à la fenêtre parente les messages de notification [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) et [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) . Il n'y a pas de valeur de retour.                                                                             |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)     | Active/désactive l’état développé si l’utilisateur a cliqué sur le bouton associé à un élément parent. Si l’utilisateur a cliqué sur une étiquette d’élément, le contrôle Tree-View sélectionne et définit le focus sur l’élément. Si l’utilisateur déplace la souris avant de relâcher le bouton de la souris, le contrôle Tree-View commence une opération de glisser-déplacer. Il n'y a pas de valeur de retour.                                                                                                                                                                          |
| [**\_peinture WM**](/windows/desktop/gdi/wm-paint)                      | Peint la région non valide du contrôle Tree-View. Elle retourne zéro. Si le paramètre *wParam* est non **null**, le contrôle suppose que la valeur est un handle vers un contexte de périphérique (HDC) et peint à l’aide de ce contexte de périphérique.                                                                                                                                                                                                                                                                                      |
| [**\_RBUTTONDOWN WM**](/windows/desktop/inputdev/wm-rbuttondown)     | Vérifie si l’utilisateur a cliqué sur un élément et qu’une opération glisser a commencé. Si l’opération a commencé, elle envoie un message de notification [TVN \_ BEGINRDRAG](tvn-beginrdrag.md) à la fenêtre parente et met en surbrillance la cible de déplacement. Dans le cas contraire, il envoie un message de notification [nm \_ RCLICK (arborescence)](nm-rclick-tree-view.md) à la fenêtre parente. Il n'y a pas de valeur de retour.                                                                                                                                           |
| [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)           | Repeint l’élément ayant le focus, le cas échéant, et envoie un message de notification [nm \_ SetFocus](nm-setfocus.md) à la fenêtre parente.                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_SetFont WM**](/windows/desktop/winmsg/wm-setfont)               | Enregistre le handle de police spécifié et repeint le contrôle d’affichage d’arborescence à l’aide de la nouvelle police.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_SETREDRAW WM**](/windows/desktop/gdi/wm-setredraw)              | Définit ou efface l’indicateur de redessin. Le contrôle Tree-View est redessiné après la définition de l’indicateur de redessin. Elle retourne zéro.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**taille du WM \_**](/windows/desktop/winmsg/wm-size)                     | Recalcule les variables internes qui dépendent de la taille de la zone cliente du contrôle Tree-View. Elle retourne **true**.                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**\_STYLECHANGED WM**](/windows/desktop/winmsg/wm-stylechanged)     | Annule la modification des étiquettes et redessine le contrôle Tree-View à l’aide des nouveaux styles. Elle retourne zéro.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_SYSCOLORCHANGE WM**](/windows/desktop/gdi/wm-syscolorchange)    | Redessine le contrôle d’arborescence à l’aide de la nouvelle couleur si l’indicateur de redessin est défini. Il n'y a pas de valeur de retour.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_minuteur WM**](/windows/desktop/winmsg/wm-timer)                   | Commence à modifier une étiquette d’élément. Si l’utilisateur clique sur l’étiquette de l’élément ayant le focus, le contrôle Tree-View définit un minuteur au lieu de passer immédiatement en mode édition. La minuterie permet à l’arborescence d’éviter d’entrer en mode édition si l’utilisateur double-clique sur l’étiquette. Elle retourne zéro.                                                                                                                                                                                                                       |
| [**\_VSCROLL WM**](wm-vscroll.md)                  | Fait défiler le contrôle d’arborescence. Elle retourne la **valeur true** si le défilement se produit, ou **false** dans le cas contraire.                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[EXEMPLE : CustDTv illustre un dessin personnalisé dans un contrôle TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 