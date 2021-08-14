---
title: ASFLeakyBucketPairs
description: L’attribut ASFLeakyBucketPairs est un attribut facultatif qui décrit les exigences de mise en mémoire tampon pour un fichier de vitesse de transmission variable.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- Format Windows Media ASFLeakyBucketPairs
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76de649a069b0cfec74fabe1a41d6cfa659b39448257a4bc966065e1bce98ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434618"
---
# <a name="asfleakybucketpairs"></a>ASFLeakyBucketPairs

L’attribut **ASFLeakyBucketPairs** est un attribut facultatif qui décrit les exigences de mise en mémoire tampon pour un fichier de vitesse de transmission variable.

## <a name="global-constant"></a>Constante globale

\_wszASFLeakyBucketPairs g

## <a name="data-type"></a>Type de données

**\_binaire de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut a le format suivant :

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Où *wReserved* doit être égal à zéro et *compartiment* est un tableau de structures de [**\_ \_ \_ paires de compartiments WM Leaky**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) . Le tableau doit contenir au moins deux entrées, mais peut être plus grande. L’objet lecteur utilise cet attribut pour déterminer la quantité de contenu à mettre en mémoire tampon avant la lecture.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




