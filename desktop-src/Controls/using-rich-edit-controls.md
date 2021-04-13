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
# <a name="using-rich-edit-controls"></a>Utilisation de contrôles RichEdit

Cette section contient des rubriques qui montrent comment créer et utiliser des contrôles RichEdit.

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="create-rich-edit-controls.md">Comment créer des contrôles RichEdit</a><br/></td>
<td>Pour créer un contrôle Rich Edit, appelez la fonction <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> , en spécifiant la classe Rich Edit Window. Pour Microsoft Rich Edit 4,1 (Msftedit.dll), spécifiez MSFTEDIT_CLASS en tant que classe de fenêtre. Pour toutes les versions précédentes, spécifiez RICHEDIT_CLASS. Pour plus d’informations, consultez <a href="about-rich-edit-controls.md">versions de Rich Edit</a>. <br/> Les contrôles RichEdit prennent en charge la plupart des styles de fenêtre utilisés avec les contrôles d’édition, ainsi que des styles supplémentaires. Vous devez spécifier le style de fenêtre <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> si vous souhaitez autoriser plus d’une ligne de texte dans le contrôle. Pour plus d’informations, consultez <a href="rich-edit-control-styles.md">styles de contrôle RichEdit</a>. <br/></td>
</tr>
<tr class="even">
<td><a href="format-text-in-rich-edit-controls.md">Comment mettre en forme du texte dans les contrôles RichEdit</a><br/></td>
<td>Une application peut envoyer des messages à un contrôle Rich Edit afin de mettre en forme des caractères et des paragraphes et de récupérer des informations de mise en forme. Les attributs de mise en forme des paragraphes incluent l’alignement, les tabulations, les retraits, la numérotation et les tables simples. Pour les caractères, vous pouvez spécifier le nom de la police, la taille, la couleur et les effets tels que gras, italique et protégé. <br/></td>
</tr>
<tr class="odd">
<td><a href="interact-with-the-current-selection.md">Comment interagir avec la sélection actuelle</a><br/></td>
<td>L’utilisateur peut sélectionner du texte dans un contrôle RichEdit à l’aide de la souris ou du clavier. La <em>sélection actuelle</em> correspond à la plage de caractères sélectionnés ou à la position du point d’insertion si aucun caractère n’est sélectionné. Une application peut obtenir des informations sur la sélection actuelle, la définir, déterminer quand elle change et afficher ou masquer la mise en surbrillance de la sélection. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-text-operations.md">Utilisation des opérations de modification de texte enrichi</a><br/></td>
<td>Une application peut envoyer des messages pour récupérer ou Rechercher du texte dans un contrôle RichEdit. Vous pouvez récupérer le texte sélectionné ou une plage de texte spécifiée. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-word-and-line-break-information.md">Utilisation des informations sur les mots et les sauts de ligne</a><br/></td>
<td>Un contrôle Rich Edit appelle une fonction appelée procédure d’interruption de mot pour rechercher des sauts entre les mots et pour déterminer où elle peut couper les lignes. Le contrôle utilise ces informations lors de l’exécution d’opérations de retour automatique à la ligne et lors du traitement des combinaisons de touches CTRL + Flèche gauche et CTRL + Flèche droite. Une application peut envoyer des messages à un contrôle Rich Edit pour remplacer la procédure de césure par défaut, pour récupérer des informations de césure de mots et pour déterminer la ligne sur laquelle se trouve un caractère donné. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-clipboard-operations.md">Comment utiliser les opérations du presse-papiers RichEdit</a><br/></td>
<td>Une application peut coller le contenu du presse-papiers dans un contrôle RichEdit en utilisant le format de presse-papiers le mieux disponible ou un format de presse-papiers spécifique. Vous pouvez également déterminer si un contrôle RichEdit peut coller un format de presse-papiers. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-streams.md">Utilisation des flux</a><br/></td>
<td>Vous pouvez utiliser des flux pour transférer des données vers ou à partir d’un contrôle RichEdit. Un flux est défini par une structure <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> , qui spécifie une mémoire tampon et une fonction de rappel définie par l’application. <br/></td>
</tr>
<tr class="even">
<td><a href="automatically-resize-rich-edit-controls.md">Comment redimensionner automatiquement les contrôles RichEdit</a><br/></td>
<td>Une application peut redimensionner un contrôle RichEdit en fonction des besoins afin qu’elle ait toujours la même taille que son contenu. Un contrôle Rich Edit prend en charge cette fonctionnalité dite « sans <em>bas</em> » en envoyant à sa fenêtre parente une <a href="en-requestresize.md">EN_REQUESTRESIZE</a> code de notification chaque fois que la taille du contenu du contrôle change. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-rich-edit-control-notification-codes.md">Comment utiliser les codes de notification de contrôle RichEdit</a><br/></td>
<td>La fenêtre parente d’un contrôle RichEdit peut traiter les codes de notification pour surveiller les événements qui affectent le contrôle. Les contrôles RichEdit prennent en charge tous les codes de notification utilisés avec les contrôles d’édition, ainsi que plusieurs autres. <br/></td>
</tr>
<tr class="even">
<td><a href="use-font-binding-in-rich-edit-controls.md">Comment utiliser la liaison de police dans les contrôles RichEdit</a><br/></td>
<td>Microsoft Rich Edit 3,0 affecte un jeu de caractères aux caractères de texte brut en fonction de leur contexte. Quelques exemples : <br/>
<ul>
<li>Les caractères grecs sont affectés <strong>GREEK_CHARSET</strong>.</li>
<li>Les symboles Hangul sont affectés <strong>HANGUL_CHARSET</strong>.</li>
<li>Les caractères chinois sont affectés <strong>SHIFTJIS_CHARSET</strong> si des caractères Kana sont trouvés à proximité ou <strong>GB2312_CHARSET</strong> si aucun Kana n’est trouvé à proximité.</li>
<li>Les caractères ANSI non neutres sont assignés <strong>ANSI_CHARSET</strong> dans n’importe quel événement.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="using-rich-edit-com.md">Utilisation d’OLE dans des contrôles RichEdit</a><br/></td>
<td>Cette section contient des informations sur l’utilisation de la liaison et de l’incorporation d’objets (OLE) dans les contrôles RichEdit. <br/></td>
</tr>
<tr class="even">
<td><a href="printing-rich-edit-controls.md">Comment imprimer le contenu de contrôles RichEdit</a><br/></td>
<td>Cette section contient des informations sur l’impression du contenu des contrôles RichEdit. <br/></td>
</tr>
</tbody>
</table>



 

 

