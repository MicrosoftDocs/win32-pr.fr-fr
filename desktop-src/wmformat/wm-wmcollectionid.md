---
title: WM/WMCollectionID
description: L’attribut WM/WMCollectionID contient un GUID identifiant la collection.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- Format Windows Media WM/WMCollectionID
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ad7e22c6769d459dc3d99b964a2df8e4dc562c709a231163d05a1b6b0be911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928829"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

L’attribut **WM/WMCollectionID** contient un GUID identifiant la collection.

## <a name="global-constant"></a>Constante globale

\_wszWMWMCollectionID g

## <a name="data-type"></a>Type de données

**\_GUID du type WMT \_**

## <a name="remarks"></a>Remarques

le contenu est identifié par Windows technologies multimédias à l’aide de trois valeurs : **wm/WMCollectionGroupID**, **wm/WMCollectionID** et **wm/WMContentID**. Ces valeurs identifient le contenu, la collection à laquelle il appartient et le groupe auquel appartient la collection. ces trois valeurs sont remplies par Lecteur Windows Media lorsque les métadonnées du contenu sont récupérées. Vous pouvez demander à votre application d’enregistrer ces valeurs et de les utiliser pour identifier le contenu, mais vous ne devez pas les modifier si elles sont présentes.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




