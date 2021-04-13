---
title: Barre de langue (services de texte)
description: Barre de langue
ms.assetid: 82b92567-fdc1-488c-b395-4cb95257955c
keywords:
- Text Services Framework (TSF), barre de langue
- TSF (Text Services Framework), barre de langue
- services de texte, barre de langue
- barre de langue
- Text Services Framework (TSF), boutons
- TSF (Text Services Framework), boutons
- services de texte, boutons
- Text Services Framework (TSF), menus
- TSF (Text Services Framework), menus
- services de texte, menus
- styles des boutons
- boutons de menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41d64a488406f6eefcff5fef6c11093af00bc5b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383752"
---
# <a name="language-bar-text-services"></a>Barre de langue (services de texte)

## <a name="implementing-the-language-bar-object"></a>Implémentation de l’objet de barre de langue

Pour prendre en charge l’ajout d’un élément à la barre de langage, un service de texte doit implémenter un objet qui prend en charge l’interface [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) et l’un des éléments de contrôle [ITfLangBarItem](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem) . Lorsque l’élément est installé, la barre de langue installe un récepteur [ITfLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink) en appelant l’élément [ITfSource :: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) de l’élément avec IID \_ ITfLangBarItemSink. L’élément utilise l’interface **ITfLangBarItemSink** pour notifier la barre de langue des modifications, par exemple lorsque l’élément est masqué, affiché, activé ou désactivé.

Quatre types d’éléments de la barre de langue peuvent être installés et chacune des interfaces requises est créée à partir de **ITfLangBarItem**. Les éléments suivants sont des éléments de contrôle **ITfLangBarItem** possibles.



|               |                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bouton        | Un bouton de barre de langue fonctionne comme un bouton de commande, un contrôle de basculement ou un menu dans la barre de langue. L’objet doit prendre en charge l’interface ITfLangBarItemButton.                   |
| Forfaitaire       | Une bulle de barre de langue fonctionne comme une notification contextuelle sur la barre de langue. L’objet doit prendre en charge l’interface ITfLangBarItemBalloon.                                       |
| Bitmap        | Une image de la barre de langue fonctionne comme un élément statique sur la barre de langue qui affiche une image bitmap. L’objet doit prendre en charge l’interface ITfLangBarItemBitmap.                       |
| Bouton bitmap | Un bouton bitmap de barre de langue fonctionne comme un élément bouton sur la barre de langue qui affiche du texte et une bitmap. L’objet doit prendre en charge l’interface ITfLangBarItemBitmapButton. |



 

## <a name="button-styles"></a>Styles des boutons

Un élément Button peut fonctionner comme l’un des éléments suivants. La fonction de l’élément de bouton est déterminée par les indicateurs définis dans le membre **dwStyle** de la structure [ \_ LANGBARITEMINFO TF](/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo) dans la méthode [ITfLangBarItem :: GetInfo](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo) .



|               |                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bouton        | Le bouton fonctionne comme un bouton de commande standard. Ce style de bouton est identifié par le \_ \_ style de bouton de style BTN de type IFA \_ \_ . ITfLangBarItemButton :: OnClick est appelé lorsque l’utilisateur clique sur l’élément. ITfLangBarItemButton :: InitMenu et ITfLangBarItemButton :: OnMenuSelect ne sont pas utilisés.                                                                                                   |
| Bouton bascule | Le bouton fonctionne comme un contrôle de basculement qui peut maintenir un état de clic, similaire à une case à cocher. Ce style de bouton est identifié par le style de basculement de style d’un type de bouton à la ligne TF \_ IFA \_ \_ \_ . ITfLangBarItemButton :: OnClick est appelé lorsque l’utilisateur clique sur l’élément. ITfLangBarItemButton :: InitMenu et ITfLangBarItemButton :: OnMenuSelect ne sont pas utilisés.                                                  |
| Menu          | Le bouton fonctionne comme un menu déroulant. Ce style de bouton est identifié par le \_ style de menu d’TF IFA \_ style \_ BTN \_ . ITfLangBarItemButton :: InitMenu est appelé lorsque l’utilisateur clique sur le bouton. Lorsque l’utilisateur sélectionne un élément dans le menu, la barre de langage appelle ITfLangBarItemButton :: OnMenuSelect avec l’identificateur de l’élément de menu sélectionné. ITfLangBarItemButton :: OnClickis non utilisé. |



 

## <a name="implementing-a-menu-button"></a>Implémentation d’un bouton de menu

Quand l’utilisateur clique sur un bouton de menu, la barre de langage appelle [ITfLangBarItemButton :: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu). L’élément ajoute des éléments au menu à l’aide de l’interface [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) transmise à InitMenu.

Pour ajouter un sous-menu au menu, appelez [ITfMenu :: AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) avec le \_ \_ sous-menu TF LBMENUF. Une fois cette opération effectuée, un nouvel objet **ITfMenu** qui représente le sous-menu est retourné dans le paramètre *ppMenu* de AddMenuItem. Ce nouvel objet menu est utilisé pour ajouter des éléments au sous-menu.

Lorsque l’utilisateur sélectionne un élément dans le menu, la barre de langage appelle [ITfLangBarItemButton :: OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) avec l’identificateur de l’élément de menu sélectionné.

## <a name="adding-items-to-the-language-bar"></a>Ajout d’éléments à la barre de langue

Un service de texte doit ajouter ses éléments à la barre de langue lorsque sa méthode [ITfTextInputProcessor :: Activate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate) est appelée et les supprimer quand son [ITfTextInputProcessor ::D eactivate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate) est appelé.

Pour ajouter un élément à la barre de langue, le service de texte obtient une interface [ITfLangBarItemMgr](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr) en appelant ITfThreadMgr :: QUERYINTERFACE avec IID \_ ITfLangBarItemMgr. Le service de texte appelle ensuite [ITfLangBarItemMgr :: AddItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem) avec le pointeur vers l’objet élément de la barre de langage.

Le service de texte doit supprimer l’élément lorsqu’il est désactivé. Le service de texte utilise la même interface **ITfLangBarItemMgr** que celle utilisée pour ajouter les éléments ou obtenir une autre instance de l’interface. Le service de texte appelle ensuite [ITfLangBarItemMgr :: RemoveItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-removeitem) avec le pointeur d’interface de l’élément à supprimer.

## <a name="extending-system-language-bar-items"></a>Extension des éléments de la barre de langue système

TSF offre la possibilité d’ajouter des éléments de menu à des menus de la barre de langage existants. Cela permet à un service de texte d’ajouter des éléments au menu d’un autre service de texte sans avoir à ajouter un bouton distinct à la barre d’outils. Cela permet également d’organiser les éléments de menu en groupes logiques. Par exemple, un service de texte qui fournit des fonctionnalités supplémentaires au service de texte vocal standard peut ajouter des éléments au menu service de texte vocal au lieu d’ajouter son propre bouton de menu de niveau supérieur.

Un service de texte fournit une extension de menu de barre de langue en implémentant un objet qui prend en charge l’interface [ITfSystemLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink) . Cette interface fonctionne exactement comme l’interface [ITfLangBarItemButton](/windows/desktop/api/Ctfutb/nn-ctfutb-itflangbaritembutton) pour un bouton de menu. Lorsque le menu est affiché, le service de texte qui est étendu appelle [ITfSystemLangBarItemSink :: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu). L’extension ajoute des éléments au menu à l’aide de l’interface [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) transmise à **InitMenu**. Lorsque l’utilisateur sélectionne un élément ajouté par l’extension, le service de texte qui est étendu appelle [ITfSystemLangBarItemSink :: OnMenuSelect](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-onmenuselect) avec l’identificateur de l’élément de menu sélectionné.

Pour installer une extension de menu de barre de langue, le service de texte effectue les étapes suivantes.

1.  Obtenez l’interface **ITfLangBarItem** de l’élément à étendre en appelant [ITfLangBarItemMgr :: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem) avec le **GUID** de l’élément à étendre.
2.  Obtenez l’interface **ITfSource** de l’élément à étendre en appelant ITfLangBarItem :: QUERYINTERFACE avec IID \_ ITfSource.
3.  Appelez [ITfSource :: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) avec IID \_ ITfSystemLangBarItemSink et le pointeur vers l’objet **ITfSystemLangBarItemSink** . Si ITfSource :: AdviseSink échoue, le service de texte ne prend pas en charge les extensions de menu.

[ITfSource :: UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink)**ITfSource :: AdviseSink**

## <a name="supporting-language-bar-menu-extensions"></a>Prise en charge des extensions de menu de barre de langage

Un service de texte peut permettre à d’autres services de texte d’ajouter des éléments à ses menus de barre de langue comme indiqué ci-dessus. Service de texte qui doit publier son GUID afin que l’élément puisse être obtenu en appelant [ITfLangBarItemMgr :: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem).

Pour prendre en charge les extensions de menu, le service de texte doit prendre en charge l’interface [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) . Les étapes suivantes activent la prise en charge d’une ou plusieurs extensions de menu.

1.  Quand [ITfSource :: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) avec IID \_ ITfSystemLangBarItemSink est appelé, le service de texte doit stocker l’interface **ITfSystemLangBarItemSink** et retourner une valeur de cookie qui identifie l’extension.
2.  Quand [ITfLangBarItemButton :: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) est appelé, le service de texte appelle la méthode [ITfSystemLangBarItemSink :: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu) de l’extension. Le service de texte doit implémenter un moyen d’identifier les éléments de menu ajoutés par l’extension, par opposition aux éléments ajoutés par le service de texte lui-même.
3.  Quand [ITfLangBarItemButton :: OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) est appelé avec un identificateur d’élément de menu qui appartient à une extension, le service de texte appelle la méthode **ITfSystemLangBarItemSink :: OnMenuSelect** de l’extension.
4.  Lorsque [ITfSource :: UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink) est appelé avec le cookie approprié, le service de texte supprime l’extension de menu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment configurer Text Services Framework](how-to-set-up-tsf.md)
</dt> <dt>

[Barre de langue (applications)](language-bar-app.md)
</dt> </dl>

 

 
