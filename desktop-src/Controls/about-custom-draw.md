---
title: À propos du dessin personnalisé
description: Cette section contient des informations générales sur la fonctionnalité de dessin personnalisée et fournit une vue d’ensemble conceptuelle de la façon dont une application peut prendre en charge le dessin personnalisé.
ms.assetid: dd104661-1e0c-4569-9753-817bcded1894
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121a4df5aa6fab222a5c4387ebdcfba51a7977b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920412"
---
# <a name="about-custom-draw"></a>À propos du dessin personnalisé

Cette section contient des informations générales sur la fonctionnalité de dessin personnalisée et fournit une vue d’ensemble conceptuelle de la façon dont une application peut prendre en charge le dessin personnalisé. Actuellement, les contrôles suivants prennent en charge la fonctionnalité de dessin personnalisée :

-   Contrôles Header
-   Contrôles de liste
-   Contrôles Rebar
-   Contrôles de barre d’outils
-   Contrôles ToolTip
-   Contrôles TrackBar
-   Contrôles d’arborescence

<!-- -->

-   [À propos des messages de notification de dessin personnalisés](#about-custom-draw-notification-messages)
-   [Paint Cycles, dessins de phases et messages de notification](#paint-cycles-drawing-stages-and-notification-messages)
-   [Tirer parti des services de dessin personnalisés](#taking-advantage-of-custom-draw-services)
    -   [Réponse à la notification de prépaint](#responding-to-the-prepaint-notification)
    -   [Demande de notifications spécifiques à un élément](#requesting-item-specific-notifications)
    -   [Dessin de l’élément vous-même](#drawing-the-item-yourself)
    -   [Modification des polices et des couleurs](#changing-fonts-and-colors)
-   [Dessin personnalisé avec les contrôles List-View et Tree-View](#custom-draw-with-list-view-and-tree-view-controls)
    -   [Dessin personnalisé avec des contrôles de List-View](#custom-draw-with-list-view-controls)
-   [Rubriques connexes](#related-topics)

## <a name="about-custom-draw-notification-messages"></a>À propos des messages de notification de dessin personnalisés

Tous les contrôles communs qui prennent en charge les codes de notification [ \_ CUSTOMDRAW](nm-customdraw.md) d’envoi de dessin nm personnalisés à des points spécifiques pendant les opérations de dessin. Ces codes de notification décrivent les opérations de dessin qui s’appliquent à l’ensemble du contrôle, ainsi que les opérations de dessin spécifiques aux éléments dans le contrôle. Comme de nombreux codes de notification, les \_ notifications CUSTOMDRAW nm sont envoyées en tant que messages de notification [**WM \_**](wm-notify.md) .

Le paramètre *lParam* d’une notification de dessin personnalisée est l’adresse d’une structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) ou d’une structure spécifique au contrôle qui contient une structure **NMCUSTOMDRAW** comme premier membre. Le tableau suivant illustre la relation entre les contrôles et les structures qu’ils utilisent.



| Structure                                | Utilisée par                              |
|------------------------------------------|--------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     | Contrôles rebar, TrackBar et Header |
| [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) | Contrôles de liste                   |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) | Contrôles de barre d’outils                     |
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Contrôles ToolTip                     |
| [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) | Contrôles d’arborescence                   |



 

## <a name="paint-cycles-drawing-stages-and-notification-messages"></a>Paint Cycles, dessins de phases et messages de notification

comme toutes les applications Windows, les contrôles communs sont automatiquement peints et effacés en fonction des messages reçus du système ou d’autres applications. Le processus d’un contrôle qui se dessine ou efface lui-même est appelé « *cycle de peinture*». Les contrôles qui prennent en charge les codes de notification [ \_ CUSTOMDRAW](nm-customdraw.md) d’envoi de dessin en nm personnalisés périodiquement à chaque cycle de peinture. Ce code de notification est accompagné d’une structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) ou d’une autre structure qui contient une structure **NMCUSTOMDRAW** en tant que premier membre.

L’une des informations que contient la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) est l’étape actuelle du cycle de peinture. C’est ce que l’on appelle la *phase de dessin* et est représenté par la valeur dans le membre **dwDrawStage** de la structure. Un contrôle informe son parent des quatre étapes de dessin de base. Ces étapes de base, ou globale, de dessin sont représentées dans la structure par les valeurs d’indicateur suivantes (définies dans commctrl. h).



| Valeurs de l’étape de dessin global | Description                        |
|--------------------------|------------------------------------|
| CDDS \_ PRÉpaint           | Avant le début du cycle de peinture.     |
| CDDS \_ POSTPAINT          | Une fois le cycle de peinture terminé. |
| \_PRÉeffacement CDDS           | Avant le début du cycle d’effacement.     |
| CDDS \_ POSTERASE          | Une fois le cycle d’effacement terminé. |



 

Chacune des valeurs précédentes peut être combinée à l' \_ indicateur d’élément CDDS pour spécifier les étapes de dessin spécifiques aux éléments. Pour plus de commodité, commctrl. h contient les valeurs spécifiques aux éléments suivantes.



| Valeurs des étapes de dessin spécifiques à l’élément | Description                                                                                                                                                                                                                                                                         |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDDS \_ ITEMPREPAINT              | Avant qu’un élément soit dessiné.                                                                                                                                                                                                                                                            |
| CDDS \_ ITEMPOSTPAINT             | Après qu’un élément a été dessiné.                                                                                                                                                                                                                                                       |
| CDDS \_ ITEMPREERASE              | Avant qu’un élément soit effacé.                                                                                                                                                                                                                                                           |
| CDDS \_ ITEMPOSTERASE             | Une fois qu’un élément a été effacé.                                                                                                                                                                                                                                                      |
| sous- \_ élément CDDS                   | [Versions de contrôle communes](common-control-versions.md) 4,71. Indicateur combiné à CDDS \_ ITEMPREPAINT ou CDDS \_ ITEMPOSTPAINT si un sous-élément est en train d’être dessiné. Cette valeur est définie uniquement si [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) est retourné à partir de CDDS \_ prépaint. |



 

Votre application doit traiter le code de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) , puis retourner une valeur spécifique qui informe le contrôle de ce qu’il doit faire. Consultez les sections suivantes pour plus d’informations sur ces valeurs de retour.

## <a name="taking-advantage-of-custom-draw-services"></a>Tirer parti des services de dessin personnalisés

La clé de l’exploitation de la fonctionnalité de dessin personnalisé est de répondre aux codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) qu’un contrôle envoie. Les valeurs de retour que votre application envoie en réponse à ces notifications déterminent le comportement du contrôle pour ce cycle de peinture.

Cette section contient des informations sur la façon dont votre application peut utiliser les valeurs de retour de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) pour déterminer le comportement du contrôle.

Les détails sont répartis dans les rubriques suivantes :

-   [Réponse à la notification de prépaint](#responding-to-the-prepaint-notification)
-   [Demande de notifications spécifiques à un élément](#requesting-item-specific-notifications)
-   [Dessin de l’élément vous-même](#drawing-the-item-yourself)
-   [Modification des polices et des couleurs](#changing-fonts-and-colors)

### <a name="responding-to-the-prepaint-notification"></a>Réponse à la notification de prépaint

Au début de chaque cycle de peinture, le contrôle envoie le code de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) , en spécifiant la \_ valeur de prépaint CDDS dans le membre **DWDRAWSTAGE** de la \_ structure CUSTOMDRAW nm associée. La valeur renvoyée par votre application à cette première notification détermine le mode et le moment où le contrôle envoie les notifications de dessin personnalisées suivantes pour le reste du cycle de peinture. Votre application peut retourner une combinaison des indicateurs suivants en réponse à la première notification.



| Valeur de retour            | Résultat                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CDRF \_ par défaut         | Le contrôle se dessine lui-même. Il n’enverra pas de notifications [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture. Cet indicateur ne peut pas être utilisé avec un autre indicateur.                                                                                                                                                                                                                                                                               |
| CDRF, \_ INerase           | Le contrôle dessinera uniquement l’arrière-plan.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CDRF \_ NEWFONT           | Votre application a spécifié une nouvelle police pour l’élément. le contrôle utilise la nouvelle police. Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](#changing-fonts-and-colors). Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                       |
| CDRF \_ NOTIFYITEMDRAW    | Le contrôle notifie le parent de toutes les opérations de dessin spécifiques à l’élément. Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après le dessin des éléments. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.                                                                                                                                                                                                                       |
| CDRF \_ NOTIFYPOSTERASE   | Le contrôle notifie le parent après l’effacement d’un élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.                                                                                                                                                                                                                                                                                                                                             |
| CDRF \_ NOTIFYPOSTPAINT   | Le contrôle enverra une notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) lorsque le cycle de peinture pour l’ensemble du contrôle est terminé. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.                                                                                                                                                                                                                                                                 |
| CDRF \_ NOTIFYSUBITEMDRAW | [Version 4,71](common-control-versions.md). Votre application recevra une [notification \_ CUSTOMDRAW nm](nm-customdraw.md) avec **dwDrawStage** défini sur CDDS \_ ITEMPREPAINT \| CDDS sous- \_ élément avant que chaque sous-élément de vue liste soit dessiné. Vous pouvez ensuite spécifier la police et la couleur de chaque sous-élément séparément ou retourner [**CDRF \_ par défaut**](cdrf-constants.md) pour le traitement par défaut. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT. |
| CDRF \_ SKIPDEFAULT       | Votre application a dessiné l’élément manuellement. Le contrôle ne dessine pas l’élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.                                                                                                                                                                                                                                                                                                                      |
| CDRF \_ SKIPPOSTPAINT     | Le contrôle ne dessine pas le rectangle de focus autour d’un élément.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

### <a name="requesting-item-specific-notifications"></a>Demande de notifications spécifiques à un élément

Si votre application renvoie [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) à la notification de dessin personnalisée de prépaint initiale, le contrôle enverra des notifications pour chaque élément qu’il dessine pendant ce cycle de peinture. Ces notifications spécifiques à l’élément comporteront la \_ valeur CDDS ITEMPREPAINT dans le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée. Vous pouvez demander que le contrôle envoie une autre notification quand il a terminé de dessiner l’élément en retournant [**CDRF \_ NOTIFYPOSTPAINT**](cdrf-constants.md) à ces notifications spécifiques à l’élément. Sinon, retournez [**CDRF \_ par défaut**](cdrf-constants.md) et le contrôle n’avertira pas la fenêtre parente jusqu’à ce qu’il commence à dessiner l’élément suivant.

### <a name="drawing-the-item-yourself"></a>Dessin de l’élément vous-même

Si votre application dessine la totalité de l’élément, retournez [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md). Cela permet au contrôle d’ignorer les éléments qu’il n’a pas besoin de dessiner, ce qui réduit la surcharge du système. N’oubliez pas que le retour de cette valeur signifie que le contrôle ne dessinera aucune partie de l’élément.

### <a name="changing-fonts-and-colors"></a>Modification des polices et des couleurs

Votre application peut utiliser un dessin personnalisé pour modifier la police d’un élément. Sélectionnez simplement le HFONT souhaité dans le contexte de périphérique spécifié par le membre **HDC** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée à la notification de dessin personnalisée. Étant donné que la police que vous sélectionnez peut avoir des métriques différentes de la police par défaut, veillez à inclure le bit [**CDRF \_ NEWFONT**](cdrf-constants.md) dans la valeur de retour du message de notification. Pour plus d’informations sur l’utilisation de cette fonctionnalité, consultez l’exemple de code dans utilisation d’un [dessin personnalisé](using-custom-draw.md). La police que votre application spécifie est utilisée pour afficher cet élément lorsqu’il n’est pas sélectionné. L’option dessin personnalisé ne vous permet pas de modifier les attributs de police des éléments sélectionnés.

Pour modifier les couleurs de texte pour tous les contrôles qui prennent en charge le dessin personnalisé, à l’exception de la vue liste et de l’arborescence, définissez simplement le texte et les couleurs d’arrière-plan souhaités dans le contexte de périphérique fourni dans la structure de notification de dessin personnalisée avec les fonctions [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) et [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) . Pour modifier les couleurs de texte dans l’affichage de liste ou l’arborescence, vous devez placer les valeurs de couleur souhaitées dans les membres **clrText** et **clrTextBk** de la structure [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) ou [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) .

> [!Note]  
> Avant la [Version 6,0](common-control-versions.md) des contrôles communs, les barres d’outils ignorent l’indicateur [**CDRF \_ NEWFONT**](cdrf-constants.md) . La version 6,0 prend en charge l’indicateur **CDRF \_ NEWFONT** , et vous pouvez l’utiliser pour sélectionner une police différente pour la barre d’outils. Toutefois, vous ne pouvez pas modifier la couleur d’une barre d’outils quand un style visuel est actif. Pour modifier la couleur d’une barre d’outils dans la version 6,0, vous devez d’abord désactiver les styles visuels en appelant [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) et en ne spécifiant aucun style visuel :

 


```
SetWindowTheme (hwnd, "", "");
```



## <a name="custom-draw-with-list-view-and-tree-view-controls"></a>Dessin personnalisé avec les contrôles List-View et Tree-View

La plupart des contrôles courants peuvent être gérés de la même façon. Toutefois, les contrôles d’affichage de liste et d’arborescence disposent de certaines fonctionnalités qui nécessitent une approche quelque peu différente du dessin personnalisé.

Pour la [Version 5,0](common-control-versions.md), ces deux contrôles peuvent afficher du texte tronqué si vous modifiez la police en retournant [**CDRF \_ NEWFONT**](cdrf-constants.md). Ce comportement est nécessaire pour la compatibilité descendante avec les versions antérieures des contrôles communs. Si vous souhaitez modifier la police d’un contrôle d’affichage de liste ou d’arborescence, vous obtiendrez de meilleurs résultats si vous envoyez un message [**CCM \_ SETVERSION**](ccm-setversion.md) avec la valeur *wParam* définie sur 5 avant d’ajouter des éléments au contrôle. Pour obtenir un exemple de contrôle d’arborescence qui utilise un dessin personnalisé, consultez l’exemple d’article de la base de connaissances [: CustDTv illustre un dessin personnalisé dans un contrôle TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496).

### <a name="custom-draw-with-list-view-controls"></a>Dessin personnalisé avec des contrôles de List-View

Étant donné que les contrôles List-View possèdent des sous-éléments et plusieurs modes d’affichage, vous devez gérer la notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) différemment de celle des autres contrôles communs.

Pour le mode rapport, utilisez la procédure suivante.

1.  La première [notification \_ CUSTOMDRAW nm](nm-customdraw.md) aura le membre **DwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée définie sur CDDS \_ PrePaint. Retourne [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Vous recevrez ensuite une [notification \_ CUSTOMDRAW nm](nm-customdraw.md) avec **dwDrawStage** défini sur CDDS \_ ITEMPREPAINT. Si vous spécifiez de nouvelles polices ou couleurs et que vous renvoyez [**CDRF \_ NEWFONT**](cdrf-constants.md), tous les sous-éléments de l’élément seront modifiés. Si vous souhaitez plutôt gérer chaque sous-élément séparément, retournez [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md).
3.  Si vous avez retourné [**CDRF \_ NOTIFYSUBITEMDRAW**](cdrf-constants.md) à l’étape précédente, vous recevrez une [notification \_ CUSTOMDRAW nm](nm-customdraw.md) pour chaque sous-élément avec **dwDrawStage** défini sur CDDS sous-élément CDDS ITEMPREPAINT \_ \| \_ . Pour modifier la police ou la couleur de ce sous-élément, spécifiez une nouvelle police ou couleur et retournez [**CDRF \_ NEWFONT**](cdrf-constants.md).

Pour les grandes icônes, les petites icônes et les modes de liste, utilisez la procédure suivante.

1.  La première [notification \_ CUSTOMDRAW nm](nm-customdraw.md) aura le membre **DwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée définie sur CDDS \_ PrePaint. Retourne [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md).
2.  Vous recevrez ensuite une [notification \_ CUSTOMDRAW nm](nm-customdraw.md) avec **dwDrawStage** défini sur CDDS \_ ITEMPREPAINT. Vous pouvez modifier les polices ou les couleurs d’un élément en spécifiant de nouvelles polices et couleurs et en retournant [**CDRF \_ NEWFONT**](cdrf-constants.md). Comme ces modes n’ont pas de sous-éléments, vous ne recevrez pas de \_ notifications CUSTOMDRAW nm supplémentaires.

Pour obtenir un exemple de gestionnaire de notification [ \_ CUSTOMDRAW](nm-customdraw.md) en mode liste, consultez [utilisation d’un dessin personnalisé](using-custom-draw.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Utilisation d’un dessin personnalisé](using-custom-draw.md)
</dt> <dt>

[Référence de dessin personnalisée](custom-draw-reference.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[EXEMPLE : CustDTv illustre un dessin personnalisé dans un contrôle TreeView (Q248496)]( https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 