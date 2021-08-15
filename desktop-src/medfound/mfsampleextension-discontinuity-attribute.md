---
description: Spécifie si un échantillon de média est le premier échantillon après un intervalle dans le flux.
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: Attribut MFSampleExtension_Discontinuity (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac76b8e4d220ece7c34277bfac031213c1c042615d7ca48677839e54b77e5da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241079"
---
# <a name="mfsampleextension_discontinuity-attribute"></a>\_Attribut de discontinuité MFSampleExtension

Spécifie si un échantillon de média est le premier échantillon après un intervalle dans le flux.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Notes

Cet attribut s’applique aux exemples de supports. Si cet attribut a la **valeur true**, cela signifie qu’il y a une discontinuité dans le flux et que cet exemple est le premier à apparaître après l’intervalle.

Si cet attribut n’est pas défini, la valeur par défaut est **false**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> </dl>

 

 




