---
title: Identifiable
description: L’attribut recherché est un attribut de niveau fichier qui spécifie si une application peut rechercher des points dans le contenu.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Format Windows Media recherché
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314498"
---
# <a name="seekable"></a>Identifiable

L’attribut **recherché** est un attribut de niveau fichier qui spécifie si une application peut rechercher des points dans le contenu.

## <a name="global-constant"></a>Constante globale

\_wszWMSeekable g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

La valeur de cet attribut pour un fichier peut varier en fonction de l’objet qui expose l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) utilisée pour la récupérer. Cela est dû au fait que les objets de lecteur (à la fois synchrones et asynchrones) effectuent une vérification plus approfondie que l’objet de l’éditeur de métadonnées, pour déterminer si vous pouvez rechercher un point dans un fichier. La valeur d’attribut **recherchée** retournée par un objet lecteur est plus précise.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




