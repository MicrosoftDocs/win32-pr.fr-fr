---
title: Modèle d’objet de texte
description: Cette section contient des informations sur les éléments de programmation utilisés avec le modèle d’objet de texte (TOM).
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7625ca7772da7f4e10aa7d64159971ee0e259d2a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103842833"
---
# <a name="text-object-model"></a>Modèle d’objet de texte

Cette section contient des informations sur les éléments de programmation utilisés avec le modèle d’objet de texte (TOM).

TOM définit un ensemble important d’interfaces de manipulation de texte. Les solutions de texte telles que Microsoft Word et les contrôles RichEdit prennent en charge l’ensemble de fonctionnalités TOM. TOM a été radicalement influencé par WordBasic (le langage de programmation utilisé pour Word) et il est facile à utiliser à partir de Microsoft Visual Basic pour Applications (VBA). Cette compatibilité présente plusieurs avantages :

-   Le code peut migrer assez facilement d’une solution à l’autre.
-   Une langue peut être utilisée pour partager des informations de texte entre différents moteurs de texte.
-   Cela réduit le besoin de documentation et de code par rapport aux interfaces COM (Component Object Model) de bas niveau et aux interfaces VBA.

Toutefois, elle peut être moins efficace pour les besoins C/C++ que l’utilisation d’interfaces COM plus générales de niveau inférieur.

TOM est un ensemble d’interfaces simple à implémenter pour ses solutions de texte principal, les contrôles de mot et RichEdit. Toutefois, pour les applications qui placent une importance mineure sur le texte, il est préférable de fournir TOM interfaces en transférant le texte vers un contrôle d’édition qui prend en charge TOM. Étant donné que les contrôles RichEdit sont livrés avec les systèmes d’exploitation Microsoft, ils constituent le moyen standard d’obtenir des fonctionnalités TOM.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                                          | Contenu                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos du modèle d’objet de texte](about-text-object-model.md)         | L’objet de modèle d’objet de texte de niveau supérieur (TOM) est défini par l’interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) , qui a des méthodes pour créer et récupérer des objets inférieurs dans la hiérarchie d’objets.<br/> |
| [Utilisation du modèle d’objet de texte](using-the-text-object-model.md) | Les exemples de code présentés dans ce document illustrent divers aspects de l’utilisation du modèle d’objet de texte (TOM).<br/>                                                                                                          |



 

### <a name="interfaces"></a>Interfaces



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Contenu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></td>
<td>L’interface <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> est l’interface de niveau supérieur Tom, qui récupère les objets Active Selection et Range pour tout récit du document, qu’il soit actif ou non. Elle permet à l’application d’effectuer les opérations suivantes :
<ul>
<li>Ouvrir et enregistrer des documents.</li>
<li>Contrôler le comportement d’annulation et la mise à jour de l’écran.</li>
<li>Rechercher une plage à partir de la position d’un écran.</li>
<li>Obtient un énumérateur <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> Story.</li>
</ul>
<br/> <strong>Quand implémenter</strong><br/> En général, les applications n’implémentent pas l’interface <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> . Les solutions de texte Microsoft, telles que les contrôles RichEdit, implémentent <strong>ITextDocument</strong> dans le cadre de leur implémentation Tom. <br/> <strong>Quand l’utiliser</strong><br/> Les applications peuvent récupérer un pointeur <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> à partir d’un contrôle RichEdit. Pour ce faire, envoyez un message <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> pour récupérer un objet <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> à partir d’un contrôle Rich Edit. Ensuite, appelez la méthode <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown :: QueryInterface</strong></a> de l’objet pour récupérer un pointeur <strong>ITextDocument</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></td>
<td>Les attributs de plage de texte enrichi TOM sont accessibles par le biais d’une paire d’interfaces doubles, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> et <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></td>
<td>Les attributs de plage de texte enrichi TOM sont accessibles par le biais d’une paire d’interfaces doubles, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> et <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></td>
<td>Les objets <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> sont des outils de modification et de liaison de données puissants qui permettent à un programme de sélectionner du texte dans un récit, puis d’examiner ou de modifier ce texte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></td>
<td>Une sélection de texte est une plage de texte avec mise en surbrillance de sélection.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></td>
<td>L’objectif de l’interface <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> est d’énumérer les récits dans un <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

