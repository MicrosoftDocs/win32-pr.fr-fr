---
description: Pour faciliter la prise en charge de l’encre dans les applications, il existe deux objets, qui peuvent être incorporés et pris en charge par n’importe quel conteneur OLE.
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: Objets sInk et tInk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e25e1f258ac789382475666878c986f5053323a1b19bf8f4b6110c096f2fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091298"
---
# <a name="sink-and-tink-objects"></a>Objets sInk et tInk

Pour faciliter la prise en charge de l’encre dans les applications, il existe deux objets, qui peuvent être incorporés et pris en charge par n’importe quel conteneur OLE. Ils sont générés en appelant la **méthode Ink. ClipboardCopy (Rectangle, InkClipboardFormats, InkClipboardModes)** ou la méthode **Ink. ClipboardCopy, méthode (Strokes, InkClipboardFormats, InkClipboardModes)** et sont les suivantes :

-   Objet texte Ink (tInk). Il s’agit d’un objet OLE représentant l’encre supposée former des mots. Un objet tInk permet de convertir l’encre manuscrite en texte, soit en tant que texte retourné par un module de reconnaissance, soit en choisissant un choix dans une liste de substituts de reconnaissance. La couleur et la taille de l’encre peuvent être définies par programme et peuvent être basées sur les attributs du texte autour de l’objet. L’objet tInk est destiné à contenir un mot unique. L’objet tInk est un petit objet léger qui peut effectuer des opérations simples telles que le rendu (à partir d’un handle vers un contexte de périphérique (HDC) et un RECT) et le rendre persistant (à partir d’un flux). L’utilisation d’un objet tInk permet une expérience utilisateur transparente quand vous travaillez dans une application qui utilise l’entrée de l’écriture manuscrite et du texte.
-   Esquissez un objet d’encre (récepteur). Il s’agit d’un objet OLE représentant une entrée qui n’est pas censée former des mots. Un objet récepteur est interprété comme un dessin. Un objet récepteur est également utile pour représenter plusieurs mots.

Ces objets peuvent être utilisés pour l’interopérabilité entre les applications, soit en les plaçant à l’emplacement de l’objet OLE dans le presse-papiers, soit en les incorporant au format RTF (Rich Text Format).

Vous pouvez utiliser les objets tInk et sInk des manières suivantes :

-   les objets tInk et sInk sont pris en charge dans Microsoft Word 2002. Les utilisateurs peuvent insérer de l’encre dans un document Word à l’aide des panneaux de saisie de texte d’écriture et de dessin fournis dans Word 2002. Cette encre est incorporée dans le fichier Word en tant qu’objet OLE avec le CLSID de l’objet récepteur ou tInk.
-   Le contrôle de Tablet PC [InkEdit](/previous-versions/ms552265(v=vs.100)) utilise l’objet Tink. Le contrôle InkEdit est une sous-classe du contrôle [RichTextBox](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) standard. L’entrée manuscrite est insérée dans le flux RTF du contrôle InkEdit en tant qu’objet tInk.
-   Lorsqu’une application déplace un objet [Ink](/previous-versions/aa515768(v=msdn.10)) sélectionné dans le presse-papiers, l’emplacement OLE Object Clipboard contient un objet OLE TInk ou sInk.

Par exemple, votre application peut reconnaître l’écriture manuscrite et marquer tout objet [Ink](/previous-versions/aa515768(v=msdn.10)) comme objet Tink. Ensuite, si vous sélectionnez un mot dans l’encre, puis le copiez et collez-le dans Word, des variantes de ce mot s’affichent dans Word 2002.

> [!Note]  
> La prise en charge du presse-papiers de la plateforme Tablet PC sélectionne automatiquement l’indicateur EMF (Enhanced Metafile) quand vous placez un objet récepteur ou tInk dans le presse-papiers en tant qu’objet OLE. L’objet lui-même est stocké dans le presse-papiers dans les emplacements incorporer la source et le descripteur d’objet.

 

Autre exemple, en utilisant l’objet récepteur, vous pouvez dessiner une esquisse manuscrite dans une application, copier et coller l’esquisse dans Word 2002, puis modifier le dessin à l’aide du panneau de saisie Tablet PC dans Word.

Pour pouvoir contenir des objets tInk, une application doit implémenter la prise en charge des conteneurs OLE pour les objets incorporés. Ensuite, pour que le conteneur prenne entièrement en charge tInk, vous devez ester :

-   Modifications apportées au code pour rechercher et remplacer. Au lieu d’ignorer les objets incorporés dans la recherche, ces objets doivent être interrogés pour le type. S’il s’agit d’un objet tInk, ils doivent être instanciés et interrogés pour le texte correspondant.
-   Modifications du comportement de la sélection. La sélection d’objets tInk ne doit jamais apparaître avec des poignées de redimensionnement. Elles doivent être sélectionnées de la même façon que le texte est sélectionné dans le document. Le code de sélection des objets doit détecter si le type est tInk et afficher la sélection de manière appropriée.
-   Utilisation des propriétés ambiantes. Les propriétés ambiantes telles que la taille de la police, la couleur et la mise en forme en gras doivent être transmises à l’objet tInk. L’application de ces propriétés modifie la largeur de l’encre manuscrite. une mise à jour de la taille est donc requise en appelant la méthode [**GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) ou [IOleObject :: GetExtent](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) .
-   Remplacez le traitement par défaut de la méthode [IOleObject ::D overb](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) . Cela permet la conversion en texte pour transmettre un lot d’objets tInk au module de reconnaissance, qui peut ensuite décomposer les mots en segments de reconnaissance.

Pour plus d’informations sur la césure des mots dans des segments de reconnaissance, consultez [segments de reconnaissance](recognition-segments.md).

 

 
