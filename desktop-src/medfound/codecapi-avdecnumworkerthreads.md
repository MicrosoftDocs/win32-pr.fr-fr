---
description: Définit le nombre de threads de travail utilisés par un décodeur vidéo.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: CODECAPI_AVDecNumWorkerThreads, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514966"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>CODECAPI \_ propriété AVDecNumWorkerThreads

Définit le nombre de threads de travail utilisés par un décodeur vidéo.

## <a name="data-type"></a>Type de données

**Long** (**VT \_ I4**)

## <a name="property-guid"></a>Guid de propriété

CODECAPI \_ AVDecNumWorkerThreads

## <a name="remarks"></a>Notes

Si la valeur est 1, le décodeur sélectionne le nombre de threads.

Pour l’interface [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) , définissez cette propriété sur une valeur **long** (**VT \_ I4**). Pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , définissez cette propriété sur **UInt32**, bien que la valeur soit signée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

