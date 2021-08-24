---
title: Attribut ShadowFilePath
description: L’attribut ShadowFilePath est le chemin d’accès complet à un fichier caché.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Lecteur Windows Media de l’attribut ShadowFilePath
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf1e8f2eb5cb810004ea219aac62973377111902071beb78eca051df19877f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002149"
---
# <a name="shadowfilepath-attribute"></a>Attribut ShadowFilePath

L’attribut **ShadowFilePath** est le chemin d’accès complet à un fichier caché.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)

## <a name="remarks"></a>Remarques

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

 

 





