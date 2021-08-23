---
title: Unités de texte UI Automation
description: Cette rubrique décrit les unités de texte prises en charge par Microsoft UI Automation \ 32 ; Modèle de contrôle TextRange. Les fournisseurs UI Automation et les clients utilisent des unités de texte pour spécifier la quantité de déplacement ou de modification de la taille d’une plage de texte.
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- UI Automation, unités de texte
- unités de texte, à propos de
- UI Automation, liste d’unités de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5c40604f3c524c1e9f3bcdb36458e099563eb7279fa61133dcfa7ea3fde90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118824162"
---
# <a name="ui-automation-text-units"></a>Unités de texte UI Automation

Cette rubrique décrit les unités de texte prises en charge par le modèle de contrôle [TextRange](uiauto-implementingtextandtextrange.md) de Microsoft UI Automation. Les fournisseurs UI Automation et les clients utilisent des unités de texte pour spécifier la quantité de déplacement ou de modification de la taille d’une plage de texte.

-   [Éléments de l’API d’unité de texte](#text-unit-api-elements)
-   [Descriptions des unités de texte](#text-unit-descriptions)
    -   [Caractère](#character)
    -   [Format](#format)
    -   [Word](#word)
    -   [Ligne](#line)
    -   [Paragraph](#paragraph)
    -   [Page](#page)
    -   [Document](#document)
-   [Autres plages potentielles](#other-potential-ranges)
-   [Rubriques connexes](#related-topics)

## <a name="text-unit-api-elements"></a>Éléments de l’API d’unité de texte

L’API UI Automation comprend les méthodes suivantes qui nécessitent la spécification d’une unité de texte :

-   [**ITextRangeProvider :: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**ITextRangeProvider :: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**IUIAutomationTextRange :: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**IUIAutomationTextRange :: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

L’énumération [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) définit les unités de texte prises en charge par les plages de texte UI Automation. Pour spécifier l’unité de texte, un membre de l’énumération [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) est spécifié dans un appel à une méthode [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) ou [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) . Les unités de texte, du plus petit au plus grand, sont les suivantes :

-   [**\_Caractère TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Format TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Mot TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Ligne TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ paragraphe**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Page TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Document TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Si un contrôle textuel particulier ne prend pas en charge l’unité de texte spécifiée, le fournisseur doit répondre en remplaçant la plus grande unité de texte prise en charge par le contrôle. Par exemple, si [**le \_ paragraphe TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) est spécifié mais pas pris en charge, la méthode peut remplacer [**TextUnit \_ page**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ou [**TextUnit \_ document**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit).

Les caractéristiques linguistiques du texte source peuvent compliquer la tâche d’un fournisseur pour déterminer les limites de texte en fonction de l’unité de texte spécifiée. Pour vous aider à déterminer les limites de texte, un fournisseur peut utiliser des fonctions d’API Uniscribe telles que [**ScriptBreak**](/windows/desktop/api/usp10/nf-usp10-scriptbreak). Pour plus d’informations, consultez [Uniscribe](/windows/desktop/Intl/uniscribe) sur le site Web MSDN.

## <a name="endpoint-inclusivity"></a>Exversion de point de terminaison

Un point de terminaison d’unité de texte peut servir à la fois de point de terminaison de [démarrage](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) et de point de terminaison de [fin](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) pour les plages de texte adjacentes du même type. Si la fin d’une unité de texte est également le début d’une autre unité de texte, la plage contenant le point de terminaison de [fin](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) ne partage aucun attribut ou objet de la plage adjacente contenant le point de terminaison de [début](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) .

Par exemple, un flux de texte, « Hello **World**», contient deux unités Word avec différents attributs d’épaisseur de police (normal et gras). Dans ce cas, le [point de](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) terminaison de l’unité de mot « Hello » et le point de terminaison de [début](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) du mot «**World**» de l’unité sont les mêmes, ce qui se traduit par les éléments suivants :

- La plage de « Hello » ne partage pas l’attribut Bold du mot « World » et ne retourne pas la valeur de l’attribut mixed pour l’attribut de texte de l’épaisseur de la police.
- La plage «**World**» a une seule épaisseur de police (gras) et ne partage pas l’épaisseur de police de l’unité de mot précédente « Hello ».

Voici un autre exemple où un flux de texte contient deux unités Word, dont l’une est un lien : `[Foo]() Bar` . Dans ce cas, le point de terminaison de [fin](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) de l’unité de mot `[Foo]()` et le point de terminaison de [début](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) de la « barre » d’unité de mot sont les mêmes, ce qui se traduit par les éléments suivants :

- Le lien appartient à la plage de texte contenant « foo ».
- Le lien est un enfant de la plage de texte « foo » et est entouré par [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).
- La plage de texte « bar » n’a pas d’enfants et est placée entre les [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).

**Remarques supplémentaires :**

> Une plage dégénérée (vide) à une limite d’unité de texte avec une plage de texte du même type assume les propriétés de l’unité de texte immédiatement adjacente.
>
> L’appel de [IUIAutomationTextRange :: ExpandToEnclosingUnit](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) sur une plage dégénérée au niveau d’une limite d’unité de texte avec une plage de texte du même type, développe la plage dégénérée jusqu’à l’unité de texte suivante.

## <a name="text-unit-descriptions"></a>Descriptions des unités de texte

Cette section décrit chacune des unités de texte prises en charge par UI Automation.

### <a name="character"></a>Caractère

[**TextUnit \_ Le caractère**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) est une unité linguistique de texte qui représente un caractère unique. La définition linguistique d’un caractère varie en fonction de la langue. Pour l’anglais des États-Unis, un caractère est généralement encadré d’un espace ou d’un autre caractère, tel qu’un signe de ponctuation, un chiffre ou une lettre.

Les caractères de contrôle tels que les retours chariot et la marque Unicode de gauche à droite (LTM) ne doivent pas être considérés comme des caractères, mais ils peuvent être inclus dans une plage de texte normalisée en fonction de l’unité de texte de caractères.

Les signes de ponctuation et les caractères de saut de mot tels que les espaces doivent être considérés comme des caractères.

### <a name="format"></a>Format

[**TextUnit \_ Le format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) est utilisé pour positionner la limite d’une plage de texte en fonction des attributs de mise en forme du texte. Par exemple, si une plage de texte est actuellement positionnée sur un caractère unique d’un mot, la spécification du **\_ format TextUnit** dans un appel à [**IUIAutomationTextRange :: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) développe la plage de texte pour inclure tout le texte partageant les mêmes attributs que le caractère unique. La plage de texte résultante peut inclure ou non le mot entier. En outre, l’utilisation de l’unité format texte ne permet pas de développer une plage de texte sur les limites d’un objet incorporé, tel qu’une image ou un lien hypertexte.

Contrairement aux autres unités de texte, notamment les unités de texte qui sont plus petites, [**le \_ format TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) peut être plus petit ou plus grand que les autres unités. Par exemple, si un document entier partage les mêmes attributs de texte et ne contient pas d’objets incorporés, le développement d’une plage de texte par le **\_ format TextUnit** crée une nouvelle plage qui englobe le document entier, tandis que le développement de la plage de texte par [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) crée une plage plus petite.

### <a name="word"></a>Word

[**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) est une unité linguistique de texte qui représente un mot unique et entier. La définition linguistique d’un mot varie selon la langue. Pour l’anglais des États-Unis, les mots sont généralement encadrés par des espaces ou des signes de ponctuation.

Quand [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) est utilisé pour définir la limite d’une plage de texte, la plage de texte résultante doit inclure tous les caractères de saut de mot présents à la fin du mot, mais avant le début du mot suivant.

### <a name="line"></a>Ligne

[**TextUnit \_ Line**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) est une unité de texte qui représente une seule ligne de texte telle qu’elle est présentée dans la fenêtre d’affichage du contrôle. Quand vous utilisez la **\_ ligne TextUnit** pour définir la limite d’une plage de texte, un fournisseur doit définir la limite immédiatement après le point où un caractère de contrôle brise la ligne, ou lorsque la fenêtre d’affichage du contrôle encapsule le texte sur une nouvelle ligne. La limite doit être définie au début d’une nouvelle ligne.

### <a name="paragraph"></a>Paragraph

[**TextUnit \_ Le paragraphe**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) est une unité linguistique de texte qui représente un paragraphe complet. Un paragraphe doit commencer juste avant le premier caractère d’un paragraphe et doit généralement se terminer juste après le dernier caractère. Toutes les lignes vides qui suivent un paragraphe doivent être fusionnées dans le paragraphe, sauf si un contenu de la source de texte indique une autre valeur. En règle générale, la limite de fin d’un paragraphe marque également la limite de fin d’une unité de texte de [**\_ ligne TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) .

### <a name="page"></a>Page

[**TextUnit \_ La page**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) représente une page de texte complète d’un document. Les limites d’une page doivent être définies aux points immédiats où une page démarre et se termine.

### <a name="document"></a>Document

[**TextUnit \_ Le document**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) représente tout le contenu d’un document tel qu’il est pris en charge par le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) . Aucun texte ne doit exister en dehors d’une plage de texte qui contient un document. Tous les objets insérés dans un document, tels que les notes d’annotation qui franchissent les limites d’une page, doivent être traités comme des objets incorporés du document et ne font pas partie du contenu texte du document.

## <a name="other-potential-ranges"></a>Autres plages potentielles

La spécification du modèle de contrôle [TextRange](uiauto-implementingtextandtextrange.md) actuel n’autorise pas l’ajout de nouvelles valeurs d’unité de texte à l’énumération [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , pas plus qu’elle n’autorise la redéfinition des valeurs d’unité de texte existantes. Pour exposer d’autres plages potentielles, telles que des en-têtes et des annotations, un fournisseur doit exposer ces plages en tant qu’objets incorporés avec une plage de texte associée. De cette façon, vous pouvez également ajouter la prise en charge des modèles de contrôle appropriés. Cette solution est plus flexible et extensible que de définir de nouvelles unités de texte.

## <a name="related-topics"></a>Rubriques connexes

### <a name="reference"></a>Informations de référence

[TextPatternRangeEndpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[ITextRangeProvider :: GetChildren](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>Conceptuel

[Prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md)

[Utilisation de contrôles textuels](uiauto-workingwithtextbasedcontrols.md)