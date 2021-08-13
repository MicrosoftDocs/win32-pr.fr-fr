---
title: WM/WMCollectionGroupID
description: L’attribut WM/WMCollectionGroupID contient un GUID identifiant le groupe de collections.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- Format Windows Media WM/WMCollectionGroupID
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b9d89724751e778eb9545b6c743dbfbcf077b860a8d85c5ab9297680deb930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698233"
---
# <a name="wmwmcollectiongroupid"></a>WM/WMCollectionGroupID

L’attribut **WM/WMCollectionGroupID** contient un GUID identifiant le groupe de collections.

## <a name="global-constant"></a>Constante globale

\_wszWMWMCollectionGroupID g

## <a name="data-type"></a>Type de données

**\_GUID du type WMT \_**

## <a name="remarks"></a>Remarques

le contenu est identifié par Windows technologies multimédias à l’aide de trois valeurs : **wm/WMCollectionGroupID**, **wm/WMCollectionID** et **wm/WMContentID**. Ces valeurs identifient le contenu, la collection à laquelle il appartient et le groupe auquel appartient la collection. ces trois valeurs sont remplies par Lecteur Windows Media lorsque les métadonnées du contenu sont récupérées. Vous pouvez demander à votre application d’enregistrer ces valeurs et de les utiliser pour identifier le contenu, mais vous ne devez pas les modifier si elles sont présentes.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




