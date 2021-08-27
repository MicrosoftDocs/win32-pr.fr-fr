---
description: Le type d’application que vous créez détermine le format de persistance d’encre à prendre en charge.
ms.assetid: bd0a4382-f014-4f03-990d-d2f96aa76ab8
title: Choix des formats à prendre en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b8b2197c37db603388a4191e08114800aaba37ee8e89803c7ddfb08be18d3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110999"
---
# <a name="choosing-which-formats-to-support"></a>Choix des formats à prendre en charge

Le type d’application que vous créez détermine le format de persistance d’encre à prendre en charge.

## <a name="single-ink-object-applications"></a>Applications à objet d’encre unique

Les applications dont les documents contiennent uniquement de l’encre doivent utiliser le format ISF (Ink Serialized Format). Ils doivent pouvoir copier et coller Ink Serialized Format (ISF). C’est le cas, par exemple, d’une application de dessin ou d’annotation. Ces applications peuvent utiliser les méthodes [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)et [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste) .

## <a name="complex-applications"></a>Applications complexes

Les applications dont les documents contiennent d’autres contenus, tels que du texte, doivent copier du code HTML avec des fichiers GIF (Graphics Interchange Format) enrichis, en plus de ISF. Le HTML lui-même doit être généré par l’application, bien que les interfaces de programmation d’applications (API) du Tablet PC génèrent des fichiers GIF. Ces applications doivent également être en mesure de copier et coller des applications ISF pour l’interopérabilité avec les applications décrites ci-dessus.

## <a name="rtf"></a>RTF

une application doit pouvoir produire un format rtf (rich Text Format) si l’interopérabilité avec Microsoft Word 2002 ou d’autres applications héritées est requise.

## <a name="mime-support"></a>Prise en charge MIME

Le tableau suivant répertorie les en-têtes MIME (Multipurpose Internet Mail Extensions) et les extensions de fichier suggérés pour l’encre qui est conservée dans les fichiers à l’aide du format ISF ou GIF. Ces valeurs se trouvent dans l’énumération [**PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat) .



| Format de persistance            | En-tête MIME                                                                                    | Extension de fichier            |
|-------------------------------|------------------------------------------------------------------------------------------------|---------------------------|
| **Base64Gif**                 | Content-type : application/x-ms-Ink Content-Transfer-Encoding : base64<br/>                | Non applicable<br/> |
| **Base64InkSerializedFormat** | Content-type : content-type : image/GIF ; format = Ink Content-Transfer-Encoding : base64<br/> | Non applicable<br/> |
| **Formats**                       | Type de contenu : application/x-ms-Ink<br/>                                                  | .gif<br/>           |
| **InkSerializedFormat**       | Content-type : content-type : image/GIF ; format = Ink<br/>                                   | . ISF<br/>           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Énumération PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)
</dt> </dl>

 

 




