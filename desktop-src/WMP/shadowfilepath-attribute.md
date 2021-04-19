---
title: Attribut ShadowFilePath
description: L’attribut ShadowFilePath est le chemin d’accès complet à un fichier caché.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Attribut ShadowFilePath lecteur Windows Media
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537474"
---
# <a name="shadowfilepath-attribute"></a>Attribut ShadowFilePath

L’attribut **ShadowFilePath** est le chemin d’accès complet à un fichier caché.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)

## <a name="remarks"></a>Notes

Un *fichier caché* est créé dans le cadre d’une conversion de format de fichier. Il s’agit de la copie d’un fichier que le lecteur utilise lorsque l’utilisateur synchronise le contenu de l’ordinateur sur un appareil qui requiert que le contenu soit au format de fichier d’origine. Cet attribut est défini pour que le fichier converti pointe vers l’emplacement du fichier caché.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**À propos du processus de conversion**](about-the-conversion-process.md)
</dt> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





