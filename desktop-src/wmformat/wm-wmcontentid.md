---
title: WM/WMContentID
description: L’attribut WM/WMContentID contient un GUID identifiant le contenu.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Format Windows Media WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380845"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

L’attribut **WM/WMContentID** contient un GUID identifiant le contenu.

## <a name="global-constant"></a>Constante globale

\_wszWMWMContentID g

## <a name="data-type"></a>Type de données

**\_GUID du type WMT \_**

## <a name="remarks"></a>Notes

Le contenu est identifié par les technologies Windows Media à l’aide de trois valeurs : **WM/WMCollectionGroupID**, **WM/WMCollectionID** et **WM/WMContentID**. Ces valeurs identifient le contenu, la collection à laquelle il appartient et le groupe auquel appartient la collection. Ces trois valeurs sont remplies par le lecteur Windows Media lorsque les métadonnées du contenu sont récupérées. Vous pouvez demander à votre application d’enregistrer ces valeurs et de les utiliser pour identifier le contenu, mais vous ne devez pas les modifier si elles sont présentes.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




