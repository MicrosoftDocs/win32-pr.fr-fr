---
description: GUID de type principal pour un type de média.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: Attribut MF_MT_MAJOR_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515049"
---
# <a name="mf_mt_major_type-attribute"></a>\_Attribut de \_ type de majeure-MF MT \_

GUID de type principal pour un type de média.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

Le type principal définit la catégorie globale des données multimédia. Les principaux types sont les suivants : vidéo, audio, script et ainsi de suite. Pour obtenir la liste des valeurs possibles, consultez [types de média majeurs](media-type-guids.md).

Une autre façon de récupérer cet attribut consiste à appeler [**IMFMediaType :: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
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

 

 




