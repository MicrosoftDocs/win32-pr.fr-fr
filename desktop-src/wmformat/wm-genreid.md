---
title: WM/GenreID
description: L’attribut WM/GenreID contient un identificateur de genre conforme au contenu de la balise TCON dans ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Format Windows Media WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380975"
---
# <a name="wmgenreid"></a>WM/GenreID

L’attribut **WM/GenreID** contient un identificateur de genre conforme au contenu de la balise TCON dans ID3v2. Il doit contenir l’ID de genre entre parenthèses, éventuellement suivi d’un perfectionnement qui décrit plus en détail le genre. Pour plus d’informations, reportez-vous à la spécification ID3v2.

## <a name="global-constant"></a>Constante globale

\_wszWMGenreID g

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

L’attribut préféré pour la spécification d’un genre est [**WM/genre**](wm-genre.md). Utilisez-le à la préférence pour cet attribut.

Si vous modifiez **WM/genre** ou **WM/GenreID** dans un fichier mp3, l’autre attribut sera modifié en correspondance.

### <a name="example"></a>Exemple



| Type de fichier | Valeur d'exemple   |
|-----------|-----------------|
| Audio     | « (4) Eurodisco » |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




