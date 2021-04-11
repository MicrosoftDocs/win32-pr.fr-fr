---
title: Attributs de texte prédéfinis (TsAttrid. h)
description: Les valeurs suivantes identifient les attributs de texte obtenus avec la méthode ITfContext GetAppProperty. Le format de données et le contenu de chaque type de propriété sont inclus.
ms.assetid: af73edb8-b706-40e4-a093-4ac22d33ecdc
keywords:
- Attributs de texte prédéfinis (Text Services Framework)
topic_type:
- apiref
api_name:
- Predefined Text Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cb214f6c555b589c52e9916325e38b46b0bfb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105382"
---
# <a name="predefined-text-attributes"></a>Attributs de texte prédéfinis

Les valeurs suivantes identifient les attributs de texte obtenus avec la méthode [**ITfContext :: GetAppProperty**](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Le format de données et le contenu de chaque type de propriété sont inclus.

## <a name="properties"></a>Propriétés



| Propriété                                     | Description                                                                                                                                              |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Texte TSATTRID                               | Non utilisé.                                                                                                                                                |
| TSATTRID \_ alignement du texte \_                    | Non utilisé.                                                                                                                                                |
| \_Centre d' \_ alignement du texte TSATTRID \_            | Contient une valeur différente de zéro si le texte est centré ou zéro dans le cas contraire.                                                                                      |
| TSATTRID \_ alignement du texte \_ \_ justifié           | Contient une valeur différente de zéro si le texte est justifié ou zéro dans le cas contraire.                                                                                     |
| TSATTRID \_ alignement du texte à \_ \_ gauche              | Contient une valeur différente de zéro si le texte est aligné à gauche ou zéro dans le cas contraire.                                                                                  |
| TSATTRID \_ alignement du texte à \_ \_ droite             | Contient une valeur différente de zéro si le texte est aligné à droite ou zéro dans le cas contraire.                                                                                 |
| TSATTRID \_ texte \_ EmbeddedObject               | Contient une valeur différente de zéro si le texte est un objet incorporé ou zéro dans le cas contraire.                                                                            |
| \_Césure de texte TSATTRID \_                  | Contient une valeur différente de zéro si le texte est coupé ou zéro dans le cas contraire.                                                                                    |
| \_Langue du texte TSATTRID \_                     | Contient l’identificateur de langue **LangID** du texte.                                                                                                 |
| \_Lien de texte TSATTRID \_                         | Contient un pointeur vers un objet de lien. L’appelant doit utiliser la méthode QueryInterface pour obtenir l’interface souhaitée, par exemple **IUniformResourceLocator**. |
| \_Orientation du texte TSATTRID \_                  | Spécifie l’angle, en dixièmes de degrés, entre la ligne de base de texte et l’axe des abscisses de l’appareil.                                                          |
| TSATTRID \_ paragraphe de texte \_                         | Non utilisé.                                                                                                                                                |
| TSATTRID \_ texte \_ para \_ FirstLineIndent        | Contient le nombre de points que la première ligne d’un paragraphe est mise en retrait.                                                                            |
| TSATTRID \_ texte \_ paragraphe \_ LeftIndent             | Contient le nombre de points que le paragraphe est mis en retrait à partir de la gauche.                                                                              |
| TSATTRID \_ texte des paragraphes de texte \_ \_            | Non utilisé.                                                                                                                                                |
| TSATTRID \_ texte des paragraphes de texte au \_ \_ \_ moins   | Contient le nombre minimal de lignes pour l’interligne du paragraphe.                                                                              |
| TSATTRID \_ texte des paragraphes de texte \_ \_ \_ double    | Contient une valeur différente de zéro si le paragraphe est doublement espacé ou zéro dans le cas contraire.                                                                            |
| TSATTRID \_ texte des paragraphes de texte \_ \_ \_ exactement   | Contient le nombre exact de lignes pour l’interligne du paragraphe.                                                                                |
| TSATTRID \_ texte des paragraphes de texte \_ \_ \_ multiples  | Contient le nombre de lignes pour l’espacement entre plusieurs lignes du paragraphe.                                                                             |
| TSATTRID \_ Text \_ para \_ \_ OnePtFive | Contient une valeur différente de zéro si le paragraphe est un et une demi-ligne, ou zéro dans le cas contraire.                                                             |
| TSATTRID \_ texte des paragraphes à la \_ \_ \_ une    | Contient une valeur différente de zéro si le paragraphe est à espacement simple ou zéro dans le cas contraire.                                                                            |
| TSATTRID \_ texte- \_ paragraphe \_ RightIndent            | Contient le nombre de points que le paragraphe est mis en retrait de droite.                                                                             |
| TSATTRID \_ texte \_ para \_ .             | Contient le nombre de points d’espacement après le paragraphe.                                                                                            |
| TSATTRID \_ texte \_ paragraphe \_ SpaceBefore            | Contient le nombre de points d’espacement avant le paragraphe.                                                                                           |
| TSATTRID \_ texte en \_ lecture seule                     | Contient zéro si le texte est en lecture seule ou différent de zéro dans le cas contraire.                                                                                             |
| TSATTRID \_ Text \_ RightToLeft                  | Contient zéro si le texte est une lecture de droite à gauche ou une valeur différente de zéro dans le cas contraire.                                                                                 |
| TSATTRID \_ texte \_ VerticalWriting              | Spécifie si le texte est vertical ou horizontal. Contient zéro si le texte est horizontal ou différent de zéro si le texte est vertical.                             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                       |
| En-tête<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



 

