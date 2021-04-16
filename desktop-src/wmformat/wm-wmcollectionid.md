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
ms.openlocfilehash: 21d2ffe9ca827b19b4ce403b2e2929dea64ae684
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380847"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

L’attribut **WM/WMCollectionID** contient un GUID identifiant la collection.

## <a name="global-constant"></a>Constante globale

\_wszWMWMCollectionID g

## <a name="data-type"></a>Type de données

**\_GUID du type WMT \_**

## <a name="remarks"></a>Notes

Le contenu est identifié par les technologies Windows Media à l’aide de trois valeurs : **WM/WMCollectionGroupID**, **WM/WMCollectionID** et **WM/WMContentID**. Ces valeurs identifient le contenu, la collection à laquelle il appartient et le groupe auquel appartient la collection. Ces trois valeurs sont remplies par le lecteur Windows Media lorsque les métadonnées du contenu sont récupérées. Vous pouvez demander à votre application d’enregistrer ces valeurs et de les utiliser pour identifier le contenu, mais vous ne devez pas les modifier si elles sont présentes.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




