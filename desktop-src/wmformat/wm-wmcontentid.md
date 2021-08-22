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
ms.openlocfilehash: ef6b1b77bf0305fa0890ea7e85172d77d6e213864c1fc114136bc42e08a8507b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083863"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

L’attribut **WM/WMContentID** contient un GUID identifiant le contenu.

## <a name="global-constant"></a>Constante globale

\_wszWMWMContentID g

## <a name="data-type"></a>Type de données

**\_GUID du type WMT \_**

## <a name="remarks"></a>Remarques

le contenu est identifié par Windows technologies multimédias à l’aide de trois valeurs : **wm/WMCollectionGroupID**, **wm/WMCollectionID** et **wm/WMContentID**. Ces valeurs identifient le contenu, la collection à laquelle il appartient et le groupe auquel appartient la collection. ces trois valeurs sont remplies par Lecteur Windows Media lorsque les métadonnées du contenu sont récupérées. Vous pouvez demander à votre application d’enregistrer ces valeurs et de les utiliser pour identifier le contenu, mais vous ne devez pas les modifier si elles sont présentes.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




