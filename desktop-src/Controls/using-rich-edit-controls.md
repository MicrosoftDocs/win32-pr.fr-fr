---
title: Utilisation de contrôles RichEdit
description: Cette section contient des rubriques qui montrent comment créer et utiliser des contrôles RichEdit.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0489660bb6849d0de76ae7fc2f4e21ca931662a8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104463846"
---
# <a name="using-rich-edit-controls"></a><span data-ttu-id="62ccb-103">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="62ccb-103">Using Rich Edit Controls</span></span>

<span data-ttu-id="62ccb-104">Cette section contient des rubriques qui montrent comment créer et utiliser des contrôles RichEdit.</span><span class="sxs-lookup"><span data-stu-id="62ccb-104">This section contains topics that demonstrate how to create and use rich edit controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="62ccb-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="62ccb-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62ccb-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="62ccb-106">Topic</span></span></th>
<th><span data-ttu-id="62ccb-107">Description</span><span class="sxs-lookup"><span data-stu-id="62ccb-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62ccb-108"><a href="create-rich-edit-controls.md">Comment créer des contrôles RichEdit</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-108"><a href="create-rich-edit-controls.md">How to Create Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-109">Pour créer un contrôle Rich Edit, appelez la fonction <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> , en spécifiant la classe Rich Edit Window.</span><span class="sxs-lookup"><span data-stu-id="62ccb-109">To create a rich edit control, call the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> function, specifying the rich edit window class.</span></span> <span data-ttu-id="62ccb-110">Pour Microsoft Rich Edit 4,1 (Msftedit.dll), spécifiez MSFTEDIT_CLASS en tant que classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="62ccb-110">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT_CLASS as the window class.</span></span> <span data-ttu-id="62ccb-111">Pour toutes les versions précédentes, spécifiez RICHEDIT_CLASS.</span><span class="sxs-lookup"><span data-stu-id="62ccb-111">For all previous versions, specify RICHEDIT_CLASS.</span></span> <span data-ttu-id="62ccb-112">Pour plus d’informations, consultez <a href="about-rich-edit-controls.md">versions de Rich Edit</a>.</span><span class="sxs-lookup"><span data-stu-id="62ccb-112">For more information, see <a href="about-rich-edit-controls.md">Versions of Rich Edit</a>.</span></span> <br/> <span data-ttu-id="62ccb-113">Les contrôles RichEdit prennent en charge la plupart des styles de fenêtre utilisés avec les contrôles d’édition, ainsi que des styles supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="62ccb-113">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="62ccb-114">Vous devez spécifier le style de fenêtre <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> si vous souhaitez autoriser plus d’une ligne de texte dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="62ccb-114">You should specify the <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="62ccb-115">Pour plus d’informations, consultez <a href="rich-edit-control-styles.md">styles de contrôle RichEdit</a>.</span><span class="sxs-lookup"><span data-stu-id="62ccb-115">For more information, see <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62ccb-116"><a href="format-text-in-rich-edit-controls.md">Comment mettre en forme du texte dans les contrôles RichEdit</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-116"><a href="format-text-in-rich-edit-controls.md">How to Format Text in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-117">Une application peut envoyer des messages à un contrôle Rich Edit afin de mettre en forme des caractères et des paragraphes et de récupérer des informations de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="62ccb-117">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="62ccb-118">Les attributs de mise en forme des paragraphes incluent l’alignement, les tabulations, les retraits, la numérotation et les tables simples.</span><span class="sxs-lookup"><span data-stu-id="62ccb-118">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="62ccb-119">Pour les caractères, vous pouvez spécifier le nom de la police, la taille, la couleur et les effets tels que gras, italique et protégé.</span><span class="sxs-lookup"><span data-stu-id="62ccb-119">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62ccb-120"><a href="interact-with-the-current-selection.md">Comment interagir avec la sélection actuelle</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-120"><a href="interact-with-the-current-selection.md">How to Interact with the Current Selection</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-121">L’utilisateur peut sélectionner du texte dans un contrôle RichEdit à l’aide de la souris ou du clavier.</span><span class="sxs-lookup"><span data-stu-id="62ccb-121">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="62ccb-122">La <em>sélection actuelle</em> correspond à la plage de caractères sélectionnés ou à la position du point d’insertion si aucun caractère n’est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="62ccb-122">The <em>current selection</em> is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="62ccb-123">Une application peut obtenir des informations sur la sélection actuelle, la définir, déterminer quand elle change et afficher ou masquer la mise en surbrillance de la sélection.</span><span class="sxs-lookup"><span data-stu-id="62ccb-123">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62ccb-124"><a href="use-rich-edit-text-operations.md">Utilisation des opérations de modification de texte enrichi</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-124"><a href="use-rich-edit-text-operations.md">How to Use Rich Edit Text Operations</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-125">Une application peut envoyer des messages pour récupérer ou Rechercher du texte dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="62ccb-125">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="62ccb-126">Vous pouvez récupérer le texte sélectionné ou une plage de texte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="62ccb-126">You can retrieve either the selected text or a specified range of text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62ccb-127"><a href="use-word-and-line-break-information.md">Utilisation des informations sur les mots et les sauts de ligne</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-127"><a href="use-word-and-line-break-information.md">How to Use Word and Line Break Information</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-128">Un contrôle Rich Edit appelle une fonction appelée procédure d’interruption de mot pour rechercher des sauts entre les mots et pour déterminer où elle peut couper les lignes.</span><span class="sxs-lookup"><span data-stu-id="62ccb-128">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="62ccb-129">Le contrôle utilise ces informations lors de l’exécution d’opérations de retour automatique à la ligne et lors du traitement des combinaisons de touches CTRL + Flèche gauche et CTRL + Flèche droite.</span><span class="sxs-lookup"><span data-stu-id="62ccb-129">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="62ccb-130">Une application peut envoyer des messages à un contrôle Rich Edit pour remplacer la procédure de césure par défaut, pour récupérer des informations de césure de mots et pour déterminer la ligne sur laquelle se trouve un caractère donné.</span><span class="sxs-lookup"><span data-stu-id="62ccb-130">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62ccb-131"><a href="use-rich-edit-clipboard-operations.md">Comment utiliser les opérations du presse-papiers RichEdit</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-131"><a href="use-rich-edit-clipboard-operations.md">How to Use Rich Edit Clipboard Operations</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-132">Une application peut coller le contenu du presse-papiers dans un contrôle RichEdit en utilisant le format de presse-papiers le mieux disponible ou un format de presse-papiers spécifique.</span><span class="sxs-lookup"><span data-stu-id="62ccb-132">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="62ccb-133">Vous pouvez également déterminer si un contrôle RichEdit peut coller un format de presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="62ccb-133">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62ccb-134"><a href="use-streams.md">Utilisation des flux</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-134"><a href="use-streams.md">How to Use Streams</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-135">Vous pouvez utiliser des flux pour transférer des données vers ou à partir d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="62ccb-135">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="62ccb-136">Un flux est défini par une structure <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> , qui spécifie une mémoire tampon et une fonction de rappel définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="62ccb-136">A stream is defined by an <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> structure, which specifies a buffer and an application-defined callback function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62ccb-137"><a href="automatically-resize-rich-edit-controls.md">Comment redimensionner automatiquement les contrôles RichEdit</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-137"><a href="automatically-resize-rich-edit-controls.md">How to Automatically Resize Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-138">Une application peut redimensionner un contrôle RichEdit en fonction des besoins afin qu’elle ait toujours la même taille que son contenu.</span><span class="sxs-lookup"><span data-stu-id="62ccb-138">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="62ccb-139">Un contrôle Rich Edit prend en charge cette fonctionnalité dite « sans <em>bas</em> » en envoyant à sa fenêtre parente une <a href="en-requestresize.md">EN_REQUESTRESIZE</a> code de notification chaque fois que la taille du contenu du contrôle change.</span><span class="sxs-lookup"><span data-stu-id="62ccb-139">A rich edit control supports this so-called <em>bottomless</em> functionality by sending its parent window an <a href="en-requestresize.md">EN_REQUESTRESIZE</a> notification code whenever the size of the control's content changes.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62ccb-140"><a href="use-rich-edit-control-notification-codes.md">Comment utiliser les codes de notification de contrôle RichEdit</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-140"><a href="use-rich-edit-control-notification-codes.md">How to Use Rich Edit Control Notification Codes</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-141">La fenêtre parente d’un contrôle RichEdit peut traiter les codes de notification pour surveiller les événements qui affectent le contrôle.</span><span class="sxs-lookup"><span data-stu-id="62ccb-141">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="62ccb-142">Les contrôles RichEdit prennent en charge tous les codes de notification utilisés avec les contrôles d’édition, ainsi que plusieurs autres.</span><span class="sxs-lookup"><span data-stu-id="62ccb-142">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62ccb-143"><a href="use-font-binding-in-rich-edit-controls.md">Comment utiliser la liaison de police dans les contrôles RichEdit</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-143"><a href="use-font-binding-in-rich-edit-controls.md">How to Use Font Binding in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-144">Microsoft Rich Edit 3,0 affecte un jeu de caractères aux caractères de texte brut en fonction de leur contexte.</span><span class="sxs-lookup"><span data-stu-id="62ccb-144">Microsoft Rich Edit 3.0 assigns a character set to plain-text characters depending on their context.</span></span> <span data-ttu-id="62ccb-145">Quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="62ccb-145">Some examples are:</span></span> <br/>
<ul>
<li><span data-ttu-id="62ccb-146">Les caractères grecs sont affectés <strong>GREEK_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ccb-146">Greek characters are assigned <strong>GREEK_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="62ccb-147">Les symboles Hangul sont affectés <strong>HANGUL_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="62ccb-147">Hangul symbols are assigned <strong>HANGUL_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="62ccb-148">Les caractères chinois sont affectés <strong>SHIFTJIS_CHARSET</strong> si des caractères Kana sont trouvés à proximité ou <strong>GB2312_CHARSET</strong> si aucun Kana n’est trouvé à proximité.</span><span class="sxs-lookup"><span data-stu-id="62ccb-148">Chinese characters are assigned <strong>SHIFTJIS_CHARSET</strong> if kana characters are found nearby, or <strong>GB2312_CHARSET</strong> if no kana are found nearby.</span></span></li>
<li><span data-ttu-id="62ccb-149">Les caractères ANSI non neutres sont assignés <strong>ANSI_CHARSET</strong> dans n’importe quel événement.</span><span class="sxs-lookup"><span data-stu-id="62ccb-149">Non-neutral ANSI characters are assigned <strong>ANSI_CHARSET</strong> in any event.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62ccb-150"><a href="using-rich-edit-com.md">Utilisation d’OLE dans des contrôles RichEdit</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-150"><a href="using-rich-edit-com.md">How to Use OLE in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-151">Cette section contient des informations sur l’utilisation de la liaison et de l’incorporation d’objets (OLE) dans les contrôles RichEdit.</span><span class="sxs-lookup"><span data-stu-id="62ccb-151">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62ccb-152"><a href="printing-rich-edit-controls.md">Comment imprimer le contenu de contrôles RichEdit</a></span><span class="sxs-lookup"><span data-stu-id="62ccb-152"><a href="printing-rich-edit-controls.md">How to Print the Contents of Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="62ccb-153">Cette section contient des informations sur l’impression du contenu des contrôles RichEdit.</span><span class="sxs-lookup"><span data-stu-id="62ccb-153">This section contains information about how to print the contents of rich edit controls.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

