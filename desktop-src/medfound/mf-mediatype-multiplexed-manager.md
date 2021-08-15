---
description: Fournit une instance de IMFMuxStreamMediaTypeManager qui peut être utilisée pour obtenir les types de média des sous-flux d’une source de média multiplexée et contrôler la combinaison de sous-flux multiplexés par la source.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: Attribut MF_MEDIATYPE_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe00e8824997a0af89099c7fbaad4a2378b44c3360bad0d4b8808023355da2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973688"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a>\_Attribut de \_ Gestionnaire de multiplexage de MediaType MF \_

Fournit une instance de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) qui peut être utilisée pour obtenir les types de média des sous-flux d’une source de média multiplexée et contrôler la combinaison de sous-flux multiplexés par la source.

## <a name="data-type"></a>Type de données

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Remarques

Transmettez cette valeur dans [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) pour recevoir une instance de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
