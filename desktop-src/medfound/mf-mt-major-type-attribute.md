---
description: GUID de type principal pour un type de média.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: Attribut MF_MT_MAJOR_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98efe9d8ff86769faa8fecd911f80caa87e7266e60cf0c36c2850fe3c12922df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692244"
---
# <a name="mf_mt_major_type-attribute"></a>\_Attribut de \_ type de majeure-MF MT \_

GUID de type principal pour un type de média.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Remarques

Le type principal définit la catégorie globale des données multimédia. Les principaux types sont les suivants : vidéo, audio, script et ainsi de suite. Pour obtenir la liste des valeurs possibles, consultez [types de média majeurs](media-type-guids.md).

Une autre façon de récupérer cet attribut consiste à appeler [**IMFMediaType :: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).

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

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




