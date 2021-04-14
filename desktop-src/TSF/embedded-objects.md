---
title: Objets incorporés (Text Services Framework)
description: Text Services Framework permet à un service de texte d’incorporer des objets dans un flux de texte d’application.
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- Text Services Framework (TSF), objets incorporés
- TSF (Text Services Framework), objets incorporés
- Applications compatibles TSF, objets incorporés
- objets incorporés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e4f819e6f42cc4e8d2ed81e47c79efe5ff7407
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104564381"
---
# <a name="embedded-objects-text-services-framework"></a>Objets incorporés (Text Services Framework)

Text Services Framework permet à un service de texte d’incorporer des objets dans un flux de texte d’application. Les objets incorporés sont insérés dans le flux de texte à l’aide de la valeur [TS \_ char \_ Embedded](ts-char--constants.md). Cette valeur correspond au caractère de remplacement d’objet Unicode U + FFFC, à l’aide de la notation hexadécimale. Par exemple, l’illustration suivante montre le rendu d’un objet incorporé qui représente le IDÉOGRAMME *Hi* japonais, en association avec la séquence de caractères Unicode qui représente la traduction en anglais de « Sun ».

![encodage de caractères d’un objet incorporé](images/emb-obj.gif)

La ligne supérieure de la figure contient le texte traduit, composé du mot « Sun » suivi du caractère japonais pour Sun, *Hi*. La ligne centrale de l’illustration montre le caractère Unicode. Dans le cas de U + FFFC, il s’agit du caractère de remplacement de l’objet. La ligne inférieure de la figure montre la valeur hexadécimale de chaque caractère.

## <a name="supporting-embedded-objects-in-an-application"></a>Prise en charge des objets incorporés dans une application

Le gestionnaire TSF insère un objet incorporé dans le flux de texte en appelant [ITextStoreACP :: InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) pour une application ACP, ou [ITextStoreAnchor :: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) pour une application basée sur un point d’ancrage. Lorsqu’un objet incorporé est inséré, l’application doit placer la valeur du caractère **\_ \_ incorporé TS** au niveau de la position du caractère (ou de l’emplacement d’ancrage) où l’objet est incorporé et stocker l’IDataObject associé à l’objet incorporé. Quand [ITextStoreACP :: gettext](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) ou [ITextStoreAnchor :: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) est appelé et qu’un objet incorporé est contenu dans le texte obtenu, la valeur **\_ \_ Embedded char TS** indique la présence et l’emplacement de l’objet incorporé. Pour obtenir l’objet incorporé, appelez [ITextStoreACP :: GetEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) avec la position de caractère de l’objet incorporé ou [ITextStoreAnchor :: GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) avec l’emplacement d’ancrage de l’objet incorporé.

L’application ne reconnaît pas normalement le contenu de l’objet incorporé. L’application peut tenter d’obtenir des informations d’affichage à partir de l’objet lui-même. Si l’objet incorporé peut fournir des données dans un format reconnu par l’application, tel que CF \_ UNICODETEXT ou CF \_ bitmap, l’application peut afficher des informations graphiques fournies par l’objet.

## <a name="inserting-embedded-objects"></a>Insertion d’objets incorporés

Un service de texte insère un objet incorporé dans un contexte en appelant [ITfRange :: InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) ou [ITfInsertAtSelection :: InsertEmbeddedAtSelection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection). Le service de texte doit fournir l’IDataObject incorporé.

 

 
