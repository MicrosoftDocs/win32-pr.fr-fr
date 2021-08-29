---
description: Définit le nombre de threads de travail utilisés par un décodeur vidéo.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: CODECAPI_AVDecNumWorkerThreads, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a17584e9a6e3d6f8efcfcf129a89bc0f94cb2629c0f130549a73757c20368f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035357"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>CODECAPI \_ propriété AVDecNumWorkerThreads

Définit le nombre de threads de travail utilisés par un décodeur vidéo.

## <a name="data-type"></a>Type de données

**Long** (**VT \_ I4**)

## <a name="property-guid"></a>Guid de propriété

CODECAPI \_ AVDecNumWorkerThreads

## <a name="remarks"></a>Remarques

Si la valeur est 1, le décodeur sélectionne le nombre de threads.

Pour l’interface [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) , définissez cette propriété sur une valeur **long** (**VT \_ I4**). Pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , définissez cette propriété sur **UInt32**, bien que la valeur soit signée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

