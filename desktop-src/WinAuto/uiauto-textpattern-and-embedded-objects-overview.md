---
title: Comment UI Automation expose des objets incorporés
description: Cette rubrique décrit comment Microsoft UI Automation expose des objets incorporés ou des éléments enfants dans un document texte ou un conteneur.
ms.assetid: 5ecf5e94-5329-4abb-aedb-4e303688e5f7
keywords:
- UI Automation, vue d’ensemble du modèle de texte
- UI Automation, vue d’ensemble des contrôles de texte
- UI Automation, modèle de contrôle de texte
- UI Automation, vue d’ensemble des objets incorporés
- UI Automation, exposer des objets incorporés
- UI Automation, scénarios pour les objets incorporés
- modèles de texte, à propos de
- contrôles de texte, à propos de
- Text (modèle de contrôle)
- modèles de contrôle, texte
- objets incorporés
- exposer des objets incorporés
ms.topic: article
ms.date: 08/31/2019
ms.openlocfilehash: 8e9e0a8b9f70677778238908f8faf04e21ed9619
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443320"
---
# <a name="how-ui-automation-exposes-embedded-objects"></a>Comment UI Automation expose des objets incorporés

Cette rubrique décrit comment Microsoft UI Automation utilise les modèles de contrôle Text et TextRange pour exposer des objets incorporés (éléments enfants/descendants) dans un document texte ou un conteneur.

Pour UI Automation, un objet incorporé est un élément qui a des limites non textuelles telles qu’une image, un lien hypertexte, un tableau ou un type de document (feuille de calcul Microsoft Excel, fichier Microsoft Windows Media, etc.).

> [!NOTE]
> Cela diffère de la définition OLE COM (Component Object Model) (voir [objets incorporés](../com/embedded-objects.md)), où un élément est créé dans une application et incorporé ou lié dans une autre application. Le fait que l’objet puisse être modifié dans son application d’origine est sans importance dans le contexte de l’Automation d’interface utilisateur.

## <a name="embedded-objects-and-the-ui-automation-tree"></a>Objets incorporés et arborescence UI Automation

Les objets incorporés sont traités comme des éléments individuels dans l’affichage de contrôle de l’arborescence UI Automation. Ils sont exposés en tant qu’enfants du conteneur de texte pour être accessibles via le même modèle objet que d’autres contrôles dans UI Automation.

Le tableau suivant répertorie des exemples d’éléments conteneur et non-conteneur.

:::row:::
   :::column span="2":::

      **Éléments conteneurs**

   :::column-end:::
   :::column span="":::

      **Éléments non-conteneurs**

   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::

- Calendrier
- Combobox
- DataGrid
- Document
- Modifier
- Groupe
- En-tête
- HeaderItem
- List
- Menu

   :::column-end:::
   :::column span="":::

- MenuBar
- Volet
- SplitButton
- Onglet
- Table de charge de travail
- Barre d’outils
- Arborescence
- TreeItem
- Fenêtre

   :::column-end:::
   :::column span="":::

- Lien
- Cases à cocher
- Bouton

  :::column-end:::
:::row-end:::

L’illustration suivante montre un conteneur de texte (document) avec une table et une image incorporées.

![Illustration montrant un document avec une image et une table incorporées](images/embeddedtable.jpg)

L’affichage de contenu UI Automation du document précédent est illustré dans le diagramme suivant.

![diagramme de l’affichage de contenu UI Automation d’un document avec des objets incorporés](images/contenttree.jpg)

### <a name="compatible-and-non-compatible-embedded-objects"></a>Objets incorporés « compatibles » et « non compatibles »

Certains fournisseurs UI Automation utilisent le même magasin de texte pour chaque objet TextPattern qu’ils contiennent.  Les objets qui sont sauvegardés par le même magasin de texte que leur conteneur sont appelés objets incorporés « compatibles ». Ces objets peuvent être des objets TextPattern eux-mêmes et, dans ce cas, leurs plages de texte sont comparables aux plages de texte obtenues à partir de leur conteneur. Cela permet aux fournisseurs d’exposer des informations client relatives aux objets TextPattern individuels comme s’il s’agissait d’un fournisseur de texte volumineux.

Toutefois, les fournisseurs peuvent utiliser différents magasins de texte pour différents objets TextPattern incorporés dans un conteneur TextPattern. Les objets qui ne sont pas sauvegardés par le magasin de texte du conteneur sont appelés objets incorporés « non compatibles ». Ces types d’objets incorporés peuvent être ou ne pas être des objets basés sur TextPattern.  

Le tableau suivant répertorie quelques exemples d’objets incorporés compatibles et non compatibles.

| Objets  | Objets incorporés compatibles | Objets incorporés non compatibles |
| --- | --- | --- |
| Objets incorporés non-TextPattern | Bouton dans Microsoft Edge<br>Table de données dans Microsoft Edge | Dans RichTextBlock dans l’infrastructure XAML de Microsoft<br>Images avec texte alt dans Microsoft Edge<br>ListView avec ListItems dans RichTextBlock dans l’infrastructure XAML de Microsoft |
| Objets incorporés TextPattern | Contrôle d’entrée de type « text » dans Microsoft Edge<br>Tableau dans un document Word | Élément TextBox dans un document Microsoft Word |

## <a name="exposing-embedded-objects"></a>Exposer des objets incorporés

Les modèles de contrôle [Text et TextRange](uiauto-implementingtextandtextrange.md) exposent des propriétés et des méthodes qui facilitent la navigation et l’interrogation des objets incorporés.

Le contenu textuel (ou texte interne) d’un conteneur de texte et d’un objet incorporé, tel qu’un lien hypertexte ou une cellule de tableau, est exposé en tant que flux de texte unique et continu dans l’affichage de contrôle et l’affichage de contenu de l’arborescence UI Automation. les limites de l’objet sont ignorées. Si un client UI Automation récupère le texte à des fins de récit, d’interprétation ou d’analyse de quelque manière que ce soit, la plage de texte doit être vérifiée à la recherche de cas spéciaux, tels qu’une table avec du contenu textuel ou d’autres objets incorporés. Appelez [**IUIAutomationTextRange :: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) pour obtenir une interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour chaque objet incorporé, puis appelez [**IUIAutomationTextPattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) pour obtenir une plage de texte pour chaque élément. Cette action se répète jusqu'à ce que tout le contenu textuel ait été récupéré.

> [!NOTE]
> Une plage dégénérée (ou réduite) est l’emplacement où le point de terminaison de démarrage et le point de terminaison de fin sont identiques. Les plages dégénérées sont souvent utilisées pour indiquer la position du curseur de texte via les méthodes [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) [GetSelection](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection) et [GetCaretRange](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange) .

Le diagramme suivant montre un flux de texte avec des objets incorporés et leurs étendues de plage.

![Diagramme montrant un flux de texte avec des objets incorporés et leurs étendues de plage](images/rangespans.jpg)

## <a name="embedded-objects-and-textunit"></a>Objets incorporés et TextUnit

Un objet [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) peut être parcouru et par un [TextUnit](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit)spécifié. Les fournisseurs qui contiennent des objets incorporés peuvent être parcourus à peu près de la même façon, mais les objets incorporés affectent le parcours. Voici quelques éléments à connaître :

- Tout objet incorporé non compatible est représenté par le caractère de remplacement U + FFFC dans le magasin de texte du TextPattern de l’élément conteneur. Il est également considéré à la fois comme une unité de caractères et comme une unité de mot.
- Les objets incorporés compatibles peuvent être constitués de plusieurs caractères et mots.
- L’élément englobant est l’élément le plus bas qui couvre l’ensemble de la plage de texte.
- Les éléments enfants d’une plage sont également des éléments enfants d’un élément conteneur qui est partiellement ou complètement inclus dans la plage.
- Dans l’idéal (surtout dans le cas d’éléments de conteneur comme table), une limite de mot n’excède pas la limite de l’objet. Dans l’exemple suivant, le mot « bar » ne contient pas de position de texte en dehors de la `</td>` balise (ne `<br \>` fait pas partie du mot « bar »).

```Xaml
<table style="width:100%">
  <tr>
    <th>Name</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>Eve Jackson</td>
    <td>Foo Bar</td>
  </tr>
</table>
<br/>
```

- En général, `<br \>` est traité comme un mot individuel, de sorte qu’il ne dépasse pas les limites d’une ligne.
- Une exception à la règle précédente est l’emplacement où une unité de texte Word contient des objets complets au sein de celle-ci. Par exemple, `<p>Hello <a href="#">link</a> here.</p>` , qui inclut des conteneurs insérés, contient les mots « Hello », « Link » et « here ». Où « Link » a un objet TextPattern en tant qu’élément englobant et un objet de lien comme enfant.
- Dans le cas d’unités de caractères, l’objet est l’élément englobant (les unités de texte comme celui-ci ne doivent pas avoir d’enfants).
- Les objets d’annotation ne doivent pas être représentés en tant qu’objet incorporé. Par exemple, la présence d’autres spécificateurs Author dans un document co-créé.
- Les objets incorporés occupent au moins une position de curseur, les annotations sont simplement des métadonnées.
- Chaque limite d’objet (de début et de fin) est représentée par un saut de mise en forme dans la plage de documents TextPattern.
- Pour le format HTML, chaque balise HTML ne produit pas nécessairement un objet UI Automation. Par exemple, le contenu des <em></em> balises d’accentuation n’a pas besoin d’être représenté comme élément, mais plutôt comme un flux de texte où UIA_IsItalicAttributeId retourne la valeur true.
- Le point de terminaison de démarrage est inclus et est le point de terminaison préféré alors que le point de terminaison de fin est exclusif. Cela est utile lorsque la plage est dégénérée et que les points de terminaison de début et de fin appartiennent à la même position pour cette plage.

## <a name="comparing-embedded-objects"></a>Comparaison d’objets incorporés

Les objets TextPattern imbriqués qui se trouvent dans une relation enfant similaire et partagent le même magasin de texte de sauvegarde sont appelés comparables. Dans ce cas, les plages de l’un des objets TextPattern peuvent être comparées à l’aide de [ITextRangeProvider :: compare](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare) et [ITextRangeProvider :: CompareEndpoints](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints). Les deux produisent une valeur numérique valide spécifiant leur position relative.

Un objet non TextPattern incorporé dans un objet TextPattern est comparable au TextPattern si l’objet a une plage valide dans TextPattern ([ITextProvider :: RangeFromChild](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild)) et que le contenu situé derrière la plage de texte n’est pas vide et qu’il ne s’agit pas d’un caractère de remplacement.

## <a name="embedded-textpattern-objects-and-the-document-textunit"></a>Objets TextPattern incorporés et le document TextUnit

Pour les objets TextPattern incorporés, l’unité de [document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) reconnaît uniquement le contenu contenu dans cet élément.

### <a name="word-textpattern-element-hierarchy"></a>Hiérarchie d’éléments de Word TextPattern

- L’élément document implémente TextPattern et [document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) retourne l’intégralité de la plage de documents Word.
- Les pages individuelles du document implémentent TextPattern et [document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) renvoie le contenu de ces pages individuelles (même si les pages partagent le même magasin de texte avec l’ensemble du document TextPattern).

### <a name="webpage-and-text-input-controls-in-edge"></a>Contrôles de saisie de texte et de page Web dans Edge

- L’élément principal du volet de page Web implémente TextPattern et expose la totalité du contenu de la page Web.
- Les contrôles d’entrée de texte individuels prennent en charge TextPattern, où une plage de documents représente le texte contenu dans chaque champ d’entrée (même s’ils partagent le même magasin de texte avec l’ensemble de la page Web).

## <a name="common-scenarios"></a>Scénarios courants

Cette section présente des exemples de scénarios courants qui impliquent des objets incorporés : liens hypertexte, images et tables. Dans les exemples suivants, l’accolade ouvrante ({) représente le point de terminaison de début de la plage de texte, et l’accolade fermante (}) représente le point de terminaison de fin.

### <a name="hyperlink-example-1-a-text-range-that-contains-an-embedded-text-hyperlink"></a>HYPERLINK Example 1 : plage de texte qui contient un lien hypertexte textuel incorporé

La plage de texte suivante contient un lien hypertexte textuel incorporé.

  {L’URL https://www.microsoft.com est incorporée dans le texte}.

L’appel des méthodes [**IUIAutomationTextRange :: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)et [**IUIAutomationTextPattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) entraîne les comportements décrits dans le tableau suivant.

| Méthode appelée                                                                                                                                                                                                                                                     | Résultats                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange :: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                  | Retourne la chaîne « l’URL https://www.microsoft.com est incorporée dans le texte ».                                                                               |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                          | Retourne l’élément UI Automation le plus profond qui englobe la plage de texte, dans ce cas, l’élément Automation qui représente le fournisseur de texte lui-même. |
| [**IUIAutomationTextRange :: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                          | Retourne un élément UI Automation qui représente le contrôle de lien hypertexte.                                                                                      |
| [**IUIAutomationTextPattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild), où l’élément UI Automation a été retourné par la méthode [**IUIAutomationTextRange :: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) précédente. | Retourne la plage qui représente « https://www.microsoft.com ».                                                                                            |
### <a name="hyperlink-example-2-a-text-range-that-partially-spans-an-embedded-text-hyperlink"></a>Exemple de lien hypertexte 2 : plage de texte couvrant partiellement un lien hypertexte textuel incorporé

La plage de texte suivante s’étend partiellement à un lien hypertexte de texte incorporé.

  L’URL https://{www} est incorporée dans le texte.

L’appel des méthodes [**IUIAutomationTextRange :: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)et [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) entraîne les comportements décrits dans le tableau suivant.

| Méthode appelée                                                                                            | Résultats                                                                                                         |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange :: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Retourne la chaîne « www ».                                                                                      |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Retourne l’élément UI Automation le plus profond qui englobe la plage de texte ; dans ce cas, le contrôle de lien hypertexte. |
| [**IUIAutomationTextRange :: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                 | Retourne la **valeur null** , car la plage de texte ne couvre pas l’intégralité de la chaîne d’URL.                                   |

### <a name="hyperlink-example-3-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Exemple de lien hypertexte 3 : plage de texte couvrant partiellement le contenu d’un conteneur de texte

La plage de texte suivante s’étend partiellement au contenu d’un conteneur de texte. Le conteneur de texte a un lien hypertexte textuel incorporé qui ne fait pas partie de la plage de texte.

  {URL} https://www.microsoft.com est incorporé dans le texte.

L’appel des méthodes [**IUIAutomationTextRange :: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)et [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) entraîne les comportements décrits dans le tableau suivant.

| Méthode appelée                                                                                            | Résultats                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange :: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Retourne la chaîne « L'URL ».                                                                                                                                                                                                     |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Retourne l’élément UI Automation le plus profond qui englobe la plage de texte, dans ce cas, l’élément qui représente le fournisseur de texte lui-même.                                                                                     |
| [**IUIAutomationTextRange :: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)                               | Déplace la plage de texte vers « https:// », car le texte du lien hypertexte est composé de mots individuels. Dans ce cas, le lien hypertexte n'est pas traité comme un objet unique.<br/> L’URL {http} est incorporée dans le texte.<br/> |

### <a name="image-example-1-a-text-range-that-contains-an-embedded-image"></a>Image exemple 1 : plage de texte qui contient une image incorporée

La plage de texte suivante contient une image incorporée d’une navette.

 {Image ![illustration d’une navette](images/shuttle.jpg) est incorporé dans le texte}.

L’appel des méthodes [**IUIAutomationTextRange :: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)et [**IUIAutomationTextPattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) entraîne les comportements décrits dans le tableau suivant.

| Méthode appelée                                                                                                                                                                                                                                                    | Résultats                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange :: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                 | Retourne la chaîne « l’image est incorporée dans le texte ». Tout texte de remplacement associé à l’image n’est pas inclus dans le flux de texte.                |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                         | Retourne l’élément UI Automation le plus profond qui englobe la plage de texte, dans ce cas, l’élément qui représente le fournisseur de texte lui-même. |
| [**IUIAutomationTextRange :: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                         | Retourne un élément UI Automation qui représente le contrôle image.                                                                               |
| [**IUIAutomationTextPattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) où l’élément UI Automation a été retourné par la méthode [**IUIAutomationTextRange :: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) précédente. | Retourne la plage dégénérée.                                                                                                                 |

### <a name="image-example-2-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Exemple d’image 2 : plage de texte couvrant partiellement le contenu d’un conteneur de texte

La plage de texte suivante s’étend partiellement au contenu d’un conteneur de texte. Le conteneur de texte comporte une image incorporée qui ne fait pas partie de la plage de texte.

 {Image} ![illustration d’une navette](images/shuttle.jpg) est incorporé dans le texte.

L’appel des méthodes [**IUIAutomationTextRange :: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)et [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) entraîne les comportements décrits dans le tableau suivant.

| Méthode appelée                                                                                                          | Résultats                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange :: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                       | Retourne la chaîne « L'image ».                                                                                                                                                                                                                                                 |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)               | Retourne l’élément UI Automation le plus profond qui englobe la plage de texte, dans ce cas, l’élément qui représente le fournisseur de texte lui-même.                                                                                                                                   |
| [**IUIAutomationTextRange :: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) avec les paramètres de **( \_ mot TextUnit**, 2). | Déplace la plage de texte vers « est ». Étant donné que seuls les objets incorporés basés sur du texte sont considérés comme faisant partie du flux de texte, l’image de cet exemple n’affecte pas [**IUIAutomationTextRange :: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) ou sa valeur de retour, dans ce cas, 2. |

### <a name="table"></a>Table de charge de travail

### <a name="table-example-1-gets-the-text-container-from-the-content-of-a-cell"></a>Exemple de table 1 : obtient le conteneur de texte à partir du contenu d’une cellule

Le tableau suivant obtient le conteneur de texte à partir du contenu d’une cellule.

| Cellule avec l'image                                            | Cellule avec le texte |
|------------------------------------------------------------|----------------|
| ![illustration d’une navette](images/shuttle.jpg)           | X              |
| ![illustration de l’espace et de la téléportée](images/space.jpg) | Y              |
| ![illustration d’un microscope](images/microscope.jpg)     | Z              |

L’appel des méthodes [**IUIAutomationGridPattern :: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem), [**IUIAutomationTextPattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)et [**IUIAutomationTextRange :: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) entraîne les comportements décrits dans le tableau suivant.

| Méthode appelée                                                                                                                                                                                                                       | Résultats                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern :: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) avec les paramètres (0,0).                                                                                                                        | Retourne l’élément UI Automation qui représente le contenu de la cellule de tableau, dans ce cas, l’élément est un contrôle de texte.                                                               |
| [**iuiautomationtextpattern::rangefromchild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)                                                                                                                                  | retourne la plage de l’image ![illustration d’une navette](images/shuttle.jpg).                                                                                                            |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) pour l’objet retourné par la méthode [**IUIAutomationTextPattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) précédente. | Retourne l’élément UI Automation qui représente la cellule de tableau. Dans ce cas, l’élément est un contrôle de texte qui prend en charge le modèle de contrôle [TableItem](uiauto-implementingtableitem.md) . |
| [**IUIAutomationTextRange :: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) pour l’objet retourné par la méthode **GetEnclosingElement** précédente.                                                    | Retourne l’élément UI Automation qui représente la table.                                                                                                                                   |
| [**IUIAutomationTextRange :: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) pour l’objet retourné par la méthode **GetEnclosingElement** précédente.                                                    | Retourne l’élément UI Automation qui représente le fournisseur de texte lui-même.                                                                                                                 |

### <a name="table-example-2-gets-the-text-content-of-a-cell"></a>Exemple de table 2 : obtient le contenu de texte d’une cellule

Le tableau de l’exemple précédent obtient le contenu textuel d’une cellule.

L’appel des méthodes [**IUIAutomationGridPattern :: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) et [**IUIAutomationTextPattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) entraîne les comportements décrits dans le tableau suivant.

| Méthode appelée                                                                                                                                                                                                                                                          | Résultats                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern :: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) avec paramètres (1, 1).                                                                                                                                                            | Retourne l’élément UI Automation qui représente le contenu de la cellule de tableau. Dans ce cas, l’élément est un contrôle de texte. |
| [**IUIAutomationTextPattern :: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) où l’élément UI Automation est l’objet retourné par la méthode [**IUIAutomationGridPattern :: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) précédente. | Retourne « Y ».                                                                                                               |

Lors du déplacement d’un document [**par \_ ligne TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), si la plage de texte entre dans une table incorporée, chaque ligne de texte dans une cellule doit être traitée comme une ligne.

## <a name="related-topics"></a>Rubriques connexes

### <a name="conceptual"></a>Conceptuel

- [À propos des modèles de contrôle Text et TextRange](uiauto-about-text-and-textrange-patterns.md)
- [Attributs de texte UI Automation](uiauto-textattributes.md)
- [Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
- [Prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md)