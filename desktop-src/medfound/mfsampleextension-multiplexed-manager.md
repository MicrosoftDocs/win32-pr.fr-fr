---
description: Fournit une instance de IMFMuxStreamSampleManager qui est utilisée pour accéder à la collection d’exemples à partir des sous-flux d’une source de média multiplexée.
ms.assetid: 4FD8169D-FDDF-4C69-AD46-05B02B35028C
title: Attribut MFSampleExtension_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848b613c4f6de9086f3da9636a29cad73499b7f0b37bd3445cee3d1086d61d7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848099"
---
# <a name="mfsampleextension_multiplexed_manager-attribute"></a>\_Attribut MFSampleExtension Multiplexed \_ Manager

Fournit une instance de [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) qui est utilisée pour accéder à la collection d’exemples à partir des sous-flux d’une source de média multiplexée.

## <a name="data-type"></a>Type de données

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Remarques

Transmettez cette valeur dans [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) pour recevoir une instance de [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
