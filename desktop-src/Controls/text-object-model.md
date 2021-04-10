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
# <a name="text-object-model"></a><span data-ttu-id="dc9f7-103">Modèle d’objet de texte</span><span class="sxs-lookup"><span data-stu-id="dc9f7-103">Text Object Model</span></span>

<span data-ttu-id="dc9f7-104">Cette section contient des informations sur les éléments de programmation utilisés avec le modèle d’objet de texte (TOM).</span><span class="sxs-lookup"><span data-stu-id="dc9f7-104">This section contains information about the programming elements used with the Text Object Model (TOM).</span></span>

<span data-ttu-id="dc9f7-105">TOM définit un ensemble important d’interfaces de manipulation de texte.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-105">The TOM defines a substantial set of text manipulation interfaces.</span></span> <span data-ttu-id="dc9f7-106">Les solutions de texte telles que Microsoft Word et les contrôles RichEdit prennent en charge l’ensemble de fonctionnalités TOM.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-106">Text solutions such as Microsoft Word and rich edit controls support the TOM feature set.</span></span> <span data-ttu-id="dc9f7-107">TOM a été radicalement influencé par WordBasic (le langage de programmation utilisé pour Word) et il est facile à utiliser à partir de Microsoft Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="dc9f7-107">TOM was greatly influenced by WordBasic (the programming language used for Word) and it is easy to use from Microsoft Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="dc9f7-108">Cette compatibilité présente plusieurs avantages :</span><span class="sxs-lookup"><span data-stu-id="dc9f7-108">This compatibility has several advantages:</span></span>

-   <span data-ttu-id="dc9f7-109">Le code peut migrer assez facilement d’une solution à l’autre.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-109">Code can migrate fairly easily from one solution to another.</span></span>
-   <span data-ttu-id="dc9f7-110">Une langue peut être utilisée pour partager des informations de texte entre différents moteurs de texte.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-110">One language can be used to share text information between different text engines.</span></span>
-   <span data-ttu-id="dc9f7-111">Cela réduit le besoin de documentation et de code par rapport aux interfaces COM (Component Object Model) de bas niveau et aux interfaces VBA.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-111">It reduces the need for documentation and code compared to the separate low-level Component Object Model (COM) and VBA interfaces.</span></span>

<span data-ttu-id="dc9f7-112">Toutefois, elle peut être moins efficace pour les besoins C/C++ que l’utilisation d’interfaces COM plus générales de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-112">However, it can be less efficient for C/C++ purposes than the use of more general lower level COM interfaces.</span></span>

<span data-ttu-id="dc9f7-113">TOM est un ensemble d’interfaces simple à implémenter pour ses solutions de texte principal, les contrôles de mot et RichEdit.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-113">TOM is a straightforward set of interfaces to implement for its primary text solutions, Word and rich edit controls.</span></span> <span data-ttu-id="dc9f7-114">Toutefois, pour les applications qui placent une importance mineure sur le texte, il est préférable de fournir TOM interfaces en transférant le texte vers un contrôle d’édition qui prend en charge TOM.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-114">However, for applications that place minor emphasis on text, it is better to provide TOM interfaces by transferring the text to an edit control that supports TOM.</span></span> <span data-ttu-id="dc9f7-115">Étant donné que les contrôles RichEdit sont livrés avec les systèmes d’exploitation Microsoft, ils constituent le moyen standard d’obtenir des fonctionnalités TOM.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-115">Since rich edit controls ship with Microsoft operating systems, they are the standard means of obtaining TOM functionality.</span></span>

### <a name="overviews"></a><span data-ttu-id="dc9f7-116">Vues d'ensemble</span><span class="sxs-lookup"><span data-stu-id="dc9f7-116">Overviews</span></span>



| <span data-ttu-id="dc9f7-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="dc9f7-117">Topic</span></span>                                                          | <span data-ttu-id="dc9f7-118">Contenu</span><span class="sxs-lookup"><span data-stu-id="dc9f7-118">Contents</span></span>                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc9f7-119">À propos du modèle d’objet de texte</span><span class="sxs-lookup"><span data-stu-id="dc9f7-119">About Text Object Model</span></span>](about-text-object-model.md)         | <span data-ttu-id="dc9f7-120">L’objet de modèle d’objet de texte de niveau supérieur (TOM) est défini par l’interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) , qui a des méthodes pour créer et récupérer des objets inférieurs dans la hiérarchie d’objets.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-120">The top-level Text Object Model (TOM) object is defined by the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface, which has methods for creating and retrieving objects lower in the object hierarchy.</span></span><br/> |
| [<span data-ttu-id="dc9f7-121">Utilisation du modèle d’objet de texte</span><span class="sxs-lookup"><span data-stu-id="dc9f7-121">Using The Text Object Model</span></span>](using-the-text-object-model.md) | <span data-ttu-id="dc9f7-122">Les exemples de code présentés dans ce document illustrent divers aspects de l’utilisation du modèle d’objet de texte (TOM).</span><span class="sxs-lookup"><span data-stu-id="dc9f7-122">The code samples in this document show various aspects of using the Text Object Model (TOM).</span></span><br/>                                                                                                          |



 

### <a name="interfaces"></a><span data-ttu-id="dc9f7-123">Interfaces</span><span class="sxs-lookup"><span data-stu-id="dc9f7-123">Interfaces</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc9f7-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="dc9f7-124">Topic</span></span></th>
<th><span data-ttu-id="dc9f7-125">Contenu</span><span class="sxs-lookup"><span data-stu-id="dc9f7-125">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc9f7-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc9f7-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span></span></td>
<td><span data-ttu-id="dc9f7-127">L’interface <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> est l’interface de niveau supérieur Tom, qui récupère les objets Active Selection et Range pour tout récit du document, qu’il soit actif ou non.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-127">The <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface is the TOM top-level interface, which retrieves the active selection and range objects for any story in the document whether active or not.</span></span> <span data-ttu-id="dc9f7-128">Elle permet à l’application d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dc9f7-128">It enables the application to:</span></span>
<ul>
<li><span data-ttu-id="dc9f7-129">Ouvrir et enregistrer des documents.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-129">Open and save documents.</span></span></li>
<li><span data-ttu-id="dc9f7-130">Contrôler le comportement d’annulation et la mise à jour de l’écran.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-130">Control undo behavior and screen updating.</span></span></li>
<li><span data-ttu-id="dc9f7-131">Rechercher une plage à partir de la position d’un écran.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-131">Find a range from a screen position.</span></span></li>
<li><span data-ttu-id="dc9f7-132">Obtient un énumérateur <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> Story.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-132">Get an <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> story enumerator.</span></span></li>
</ul>
<br/> <span data-ttu-id="dc9f7-133"><strong>Quand implémenter</strong></span><span class="sxs-lookup"><span data-stu-id="dc9f7-133"><strong>When to Implement</strong></span></span><br/> <span data-ttu-id="dc9f7-134">En général, les applications n’implémentent pas l’interface <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="dc9f7-134">Applications typically do not implement the <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface.</span></span> <span data-ttu-id="dc9f7-135">Les solutions de texte Microsoft, telles que les contrôles RichEdit, implémentent <strong>ITextDocument</strong> dans le cadre de leur implémentation Tom.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-135">Microsoft text solutions, such as rich edit controls, implement <strong>ITextDocument</strong> as part of their TOM implementation.</span></span> <br/> <span data-ttu-id="dc9f7-136"><strong>Quand l’utiliser</strong></span><span class="sxs-lookup"><span data-stu-id="dc9f7-136"><strong>When to Use</strong></span></span><br/> <span data-ttu-id="dc9f7-137">Les applications peuvent récupérer un pointeur <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> à partir d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-137">Applications can retrieve an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> pointer from a rich edit control.</span></span> <span data-ttu-id="dc9f7-138">Pour ce faire, envoyez un message <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> pour récupérer un objet <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> à partir d’un contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-138">To do this, send an <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> message to retrieve an <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> object from a rich edit control.</span></span> <span data-ttu-id="dc9f7-139">Ensuite, appelez la méthode <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown :: QueryInterface</strong></a> de l’objet pour récupérer un pointeur <strong>ITextDocument</strong> .</span><span class="sxs-lookup"><span data-stu-id="dc9f7-139">Then, call the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown::QueryInterface</strong></a> method to retrieve an <strong>ITextDocument</strong> pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc9f7-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc9f7-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span></span></td>
<td><span data-ttu-id="dc9f7-141">Les attributs de plage de texte enrichi TOM sont accessibles par le biais d’une paire d’interfaces doubles, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> et <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-141">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc9f7-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc9f7-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span></span></td>
<td><span data-ttu-id="dc9f7-143">Les attributs de plage de texte enrichi TOM sont accessibles par le biais d’une paire d’interfaces doubles, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> et <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-143">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc9f7-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc9f7-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span></span></td>
<td><span data-ttu-id="dc9f7-145">Les objets <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> sont des outils de modification et de liaison de données puissants qui permettent à un programme de sélectionner du texte dans un récit, puis d’examiner ou de modifier ce texte.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-145">The <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc9f7-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc9f7-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span></span></td>
<td><span data-ttu-id="dc9f7-147">Une sélection de texte est une plage de texte avec mise en surbrillance de sélection.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-147">A text selection is a text range with selection highlighting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc9f7-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc9f7-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span></span></td>
<td><span data-ttu-id="dc9f7-149">L’objectif de l’interface <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> est d’énumérer les récits dans un <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc9f7-149">The purpose of the <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> interface is to enumerate the stories in an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

