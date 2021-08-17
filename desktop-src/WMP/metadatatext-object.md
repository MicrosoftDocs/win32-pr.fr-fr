---
title: Objet MetadataText
description: L’objet MetadataText fournit un moyen de récupérer des métadonnées pour les attributs de métadonnées textuelles complexes.
ms.assetid: cf8e4524-6fc5-4534-9542-6bdc7d34bca4
keywords:
- objet MetadataText Lecteur Windows Media
topic_type:
- apiref
api_name:
- MetadataText Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f79c4f4bb80855cf84d576c126e30dc5301c45ca6f1a7c34c5d54e57844abfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135022"
---
# <a name="metadatatext-object"></a>Objet MetadataText

L’objet **MetadataText** fournit un moyen de récupérer des métadonnées pour les attributs de métadonnées textuelles complexes.

L’objet **MetadataText** prend en charge les propriétés suivantes.



| Propriété                                    | Description                                   |
|---------------------------------------------|-----------------------------------------------|
| [description](metadatatext-description.md) | Récupère une description du texte de métadonnées. |
| [text](metadatatext-text.md)               | Récupère le texte des métadonnées.                  |



 

L’objet **MetadataText** est accessible par le biais de la méthode suivante.



| Object                    | Méthode                                           |
|---------------------------|--------------------------------------------------|
| [Média](media-object.md) | [getItemInfoByType](media-getiteminfobytype.md) |



 

À des fins d’illustration, *joueur*. *currentMedia*. **getItemInfoByType**(*Name*, *Language*, *index*) est utilisé dans les sections de syntaxe de référence.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




