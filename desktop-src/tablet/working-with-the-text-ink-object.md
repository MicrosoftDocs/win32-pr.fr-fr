---
description: Pour faciliter la prise en charge de l’entrée manuscrite dans les applications, il existe deux objets, qui peuvent être incorporés et pris en charge par n’importe quel conteneur OLE, l’objet d’encre de texte (tInk) et l’objet d’encre d’esquisse (sInk).
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: Utilisation de l’objet Ink Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082323f7e67e76f7ae39c6b592a86f2be0945a86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516289"
---
# <a name="working-with-the-text-ink-object"></a>Utilisation de l’objet Ink Text

Pour faciliter la prise en charge de l’entrée manuscrite dans les applications, il existe deux objets, qui peuvent être incorporés et pris en charge par n’importe quel conteneur OLE, l’objet d’encre de texte (tInk) et l’objet d’encre d’esquisse (sInk).

L’objet Ink Text est un objet OLE représentant l’encre supposée former des mots. Un objet d’encre de texte permet de convertir l’encre manuscrite en texte en le sélectionnant dans une liste de remplacements. La couleur et la taille de l’objet Ink Text peuvent être définies par programme et peuvent être basées sur les attributs du texte autour de l’objet. L’objet texte manuscrit est destiné à contenir un mot unique.

L’objet Ink Text prend en charge l’ensemble standard d’interfaces OLE nécessaires à l’incorporation et à la prise en charge du presse-papiers. L’interface [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) lit et écrit dans un flux au format ISF (Ink Serialized Format). L’objet Ink text fournit l’interface [**IInkLineInfo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) pour accéder à ses propriétés d’affichage et à la liste des résultats de la reconnaissance.

L’objet Ink Text peut être utilisé pour l’interopérabilité entre les applications, soit en le plaçant dans l’emplacement de l’objet OLE dans le presse-papiers, en l’incorporant au format RTF, soit en le rendant persistant dans un flux ISF.

Un objet Ink Text peut être généré des manières suivantes.

-   Le contrôle [InkEdit](inkedit-control-reference.md) utilise l’objet Ink Text. La fonctionnalité du contrôle InkEdit est un super-ensemble de la fonctionnalité de contrôle RichEdit standard. L’entrée manuscrite est insérée dans le flux RTF du contrôle InkEdit sous la forme d’un objet d’encre de texte.
-   Quand une application copie un [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ou un objet [InkEdit](inkedit-control-reference.md) dans le presse-papiers et que le format d' [**énumération InkClipboardFormats**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) est défini, l’emplacement du presse-papiers de l’objet OLE contient un objet OLE d’encre textuelle.
-   Le panneau de saisie Tablet PC peut générer des objets Ink Text.

Par exemple, votre application peut reconnaître l’écriture manuscrite et ajouter le résultat de la reconnaissance aux traits. Ensuite, si vous copiez et collez les traits dans Microsoft Word sous la forme d’un objet d’encre texte, d’autres mots sont disponibles dans Word 2003 et versions ultérieures.

Pour pouvoir contenir des objets d’encre de texte, une application doit implémenter la prise en charge des conteneurs OLE pour les objets incorporés. Ensuite, pour que le conteneur prenne entièrement en charge l’encre de texte, vous devez mettre en place :

-   Modifications apportées à l’application pour la recherche et le remplacement. Au lieu d’ignorer les objets incorporés dans la recherche, ces objets doivent être interrogés pour le type. S’il s’agit d’un objet d’encre texte, ils doivent être instanciés et interrogés pour le texte correspondant.
-   Modifications du comportement de la sélection. La sélection d’objets d’encre de texte ne doit jamais apparaître avec des poignées de redimensionnement. Elles doivent être sélectionnées de la même façon que le texte est sélectionné dans le document. Le code de sélection des objets doit détecter si le type est l’encre du texte et afficher la sélection de manière appropriée.
-   Utilisation des propriétés ambiantes. Les propriétés ambiantes telles que la taille de la police, la couleur et la mise en forme en gras doivent être transmises à l’objet texte Ink. L’application de ces propriétés modifie la largeur de l’encre manuscrite. une mise à jour de la taille est donc requise en appelant la méthode [**IInkLineInfo :: GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) ou [**IOleObject :: GetExtent**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) .

## <a name="in-this-section"></a>Dans cette section

-   [Conversion d’un objet Ink Text en Ink](converting-a-text-ink-object-to-ink.md)
-   [API Text Ink](text-ink-apis.md)
-   [Objets sInk et tInk](sink-and-tink-objects.md)

 

 
