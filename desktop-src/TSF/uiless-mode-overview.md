---
title: Vue d’ensemble du mode UILess
description: Vue d’ensemble du mode UILess
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- Text Services Framework (TSF), UILessMode
- TSF (Text Services Framework), UILessMode
- Applications compatibles TSF, UILessMode
- UILessMode
- Text Services Framework (TSF), liste de candidats UIElement
- TSF (Text Services Framework), liste de candidats UIElement
- Applications compatibles TSF, liste de candidats UIElement
- UIElement liste de candidats
- Text Services Framework (TSF), info-bulle UIElement
- TSF (Text Services Framework), info-bulle UIElement
- Applications compatibles TSF, info-bulle UIElement
- Info-bulle UIElement
- Text Services Framework (TSF), éléments d’interface utilisateur prédéfinis
- TSF (Text Services Framework), éléments d’interface utilisateur prédéfinis
- Applications compatibles TSF, éléments d’interface utilisateur prédéfinis
- éléments d’interface utilisateur prédéfinis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7354a88fb28fd0d6bf5f4180ac23359a2117fe7
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104553457"
---
# <a name="uiless-mode-overview"></a>Vue d’ensemble du mode UILess

## <a name="how-to-create-uilessmode"></a>Création de UILessMode

**Création d’un thread sans interface utilisateur :** L’application peut rendre une interface utilisateur moins thread par [**ITfThreadMgrEx :: ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) avec ITF \_ AE \_ UIELEMENTENABLEDONLY. Quand ThreadMgr est activé avec cet indicateur, seules les astuces qui peuvent contrôler son élément d’interface utilisateur sont activées sur le thread. L’application doit implémenter l’interface [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) et informer l’interface dans le gestionnaire de threads. [**ITfUIElementSink :: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) est appelé quand le TIP affiche son interface utilisateur. L’application peut retourner **true** dans pbShow param pour permettre à Tip d’afficher l’interface utilisateur d’origine de l’info-bulle lorsque l’application ne souhaite pas dessiner. Si l’application n’autorise pas l’interface utilisateur du TIP, elle peut retourner la **valeur false** dans pbShow (consultez les diagrammes ci-dessous). L’application peut dessiner l’interface utilisateur en lui-même en obtenant des informations à partir du paramètre d' *Empelement* . Il peut s’agir de la liste candidate, de l’élément de la barre de langue ou de l’interface utilisateur personnalisée du Conseil. L’application peut connaître le type d’interface utilisateur par l’interface QIing [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) . Lorsque l’interface utilisateur est modifiée, [**ITfUIElementSink :: UpdateUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) est appelée. L’application peut comparer le GUID de l’enpelement->GetGUID () pour savoir si l’élément est actuellement dessiné par l’application.

**Astuce pour la prise en charge de l’interface utilisateur :** Le Conseil doit prendre en charge le mode sans interface utilisateur s’il souhaite s’exécuter sous l’application qui ne souhaite pas autoriser l’interface utilisateur du TIP, comme l’application de jeu ou les applications plein écran. Pour être moins conscient de l’interface utilisateur, TIP doit implémenter l’interface [**ITfTextInputProcessorEx**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) . Si cette interface n’est pas implémentée, TIP ne sera pas activé sous le thread en mode sans interface utilisateur. En outre, TIP doit appeler [**ITFUIElementMgr :: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) avant d’afficher une interface utilisateur visible à l’écran. Cette méthode effectue un appel à [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) pour notifier l’application. Et l’application décidera si elle peut être affichée ou non. Quand TIP appelle BeginUIElement (), TIP doit avoir l’interface [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) pour l’interface utilisateur correspondante. L’application effectue un QI en QI pour obtenir une autre interface spécifique à l’interface utilisateur afin de récupérer plus d’informations pour dessiner l’interface utilisateur. Le système prédéfinit [**ITfCandidateListUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) et [**ITfReadingInformationUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) pour Tip. Quand le TIP souhaite afficher la liste des candidats en mode thread sans interface utilisateur, TIP doit créer une instance de l’interface **ITfCandidateListUIElement** et appeler **ITFUIElementMgr :: BeginUIElement**. Quand [**ITfTextInputProcessorEx :: ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) est appelé, Conseil sait déjà que le thread est moins d’interface utilisateur, ce qui permet d’éliminer l’interface utilisateur personnalisée supplémentaire. Toutefois, bien entendu, il peut implémenter sa propre interface qui peut être QIed et essayer d’effectuer une notification. Ainsi, le TIP et l’applicateur **ITfUIElement** cationique peuvent avoir une négociation pour l’interface utilisateur personnalisée Tip.

## <a name="uielement-supporting-tip"></a>Info-bulle de support UIElement

Le Conseil qui prend en charge l’UIElement doit être catégorisé par GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED. Le Conseil dans GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED doit utiliser [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) pour afficher une interface utilisateur afin que l’application puisse contrôler la visibilité de l’interface utilisateur.

**Afficher/masquer l’état de l’UIElement :** Afficher/masquer l’état indiqué par la méthode [**ITfUIElement :: Show**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) ou [**ITfUIElement :: IsShown**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) est l’état visible réel. Elle n’est pas liée à la disponibilité d’UIElement. UIElement doit toujours être disponible lorsque l’affichage de l’État existe. L’affichage de l’État est contrôlable à partir de l’application. L’application peut soudainement passer en mode UILess et commencer à dessiner une interface utilisateur seule, en appelant **ITfUIElement :: Show** with **false** pour masquer toute l’interface utilisateur du TIP. Ensuite, TIP peut prendre l’une des options ci-dessous. 1) Conseil peut déplacer l’UIElement vers l’état de masquage et commencer à générer des UpdateUIElement. 2) l’info-bulle peut terminer UIElement, car l’élément d’interface utilisateur ne prend pas en charge Hide Status et Tip appelle EndUIElement () pour le terminer.

## <a name="predefined-ui-elements"></a>Éléments d’interface utilisateur prédéfinis

**Liste des candidats :** La liste candidate est l’un des principaux éléments d’interface utilisateur pour l’entrée EA. Cet élément d’interface utilisateur fournit la liste de candidats et le nombre correspondant de chaînes candidates pour le dessin.

**Fenêtre informations de lecture** La fenêtre informations de lecture est courante pour l’entrée au clavier chinois. Il a l’étape qui ne peut pas être insérée dans le document comme chaîne de composition. Certains processeurs d’entrée en chinois ouvrent une petite fenêtre d’informations de lecture qui affiche les informations de lecture, phonétique ou de saisie.

## <a name="the-flow-chart-of-uilessmode"></a>Organigramme de UILessMode

![Diagramme qui montre le graphique de bord U I LessMode.](images/tsf-uilessmode-ovw1.gif)

Une fois que l’info-bulle a reçu la **valeur true** dans \* pbShown par [**ITfUIElementMgr :: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement), l’astuce n’a pas besoin d’appeler UpdateUIElement pour l’UIElement. Mais TIP doit appeler EndUIElement () afin que le [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) et l’application puissent suivre l’état d’UIElement. TIP doit appeler UpdateUIElement () après que BeginUIElement () a retourné la **valeur false** dans \* pbShow. L’application qui souhaite dessiner l’interface utilisateur ne vérifie pas le contenu dans BeginUIElement (), elle retourne simplement l’État Show sur BeginUIElement () et commence à vérifier le contenu à UpdateUIElement (). Par exemple, l’indicateur de mise à jour de la liste de candidats UIElement a tous les bits au premier UpdateUIElement (). Cela signifie que le contenu d’UIElement n’a pas besoin d’être prêt sur BeginUIElement ().

![Diagramme qui indique quand le T I P appelle’ITUIElementMgr :: BeginUIElement () 'et’BeginUIElement’UIElementSink’de l’application est appelé.](images/tsf-uilessmode-ovw2.gif)![Diagramme qui montre que l’application retourne FALSe dans * pbShow.](images/tsf-uilessmode-ovw3.gif)![Organigramme uilessmode](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>UIElement liste candidate

**À propos de IndexPage :** L’application qui dessine la liste candidate calcule le nombre de chaînes par page lorsque le contenu de la liste est modifié (la \_ chaîne TF CLUIE \_ est définie). Il n’est pas recommandé de modifier l’index de page tant que la liste candidate est disponible pour le mode UILess. Cela signifie que la liste des candidats de TIP doit se comporter avec la pagination au lieu de faire défiler le curseur lorsque la sélection est déplacée vers la page suivante. Si le défilement se produit au déplacement de la sélection, l’index de la page est modifié et l’application doit recalculer l’index de la page. Le résultat peut ne pas être attendu par TIP.

**No Selection :** [**ITfCandidateListUIElement :: GetSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) retourne S \_ false, si la liste candidate n’a pas de sélection. La valeur de retour du premier paramètre n’est pas valide.

 

 




