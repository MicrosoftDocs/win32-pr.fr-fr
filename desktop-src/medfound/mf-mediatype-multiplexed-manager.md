---
description: Fournit une instance de IMFMuxStreamMediaTypeManager qui peut être utilisée pour obtenir les types de média des sous-flux d’une source de média multiplexée et contrôler la combinaison de sous-flux multiplexés par la source.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: Attribut MF_MEDIATYPE_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96c74bbff8f4858c8467fcd13253cfedf2f5dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414171"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a>\_Attribut de \_ Gestionnaire de multiplexage de MediaType MF \_

Fournit une instance de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) qui peut être utilisée pour obtenir les types de média des sous-flux d’une source de média multiplexée et contrôler la combinaison de sous-flux multiplexés par la source.

## <a name="data-type"></a>Type de données

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Notes

Transmettez cette valeur dans [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) pour recevoir une instance de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
