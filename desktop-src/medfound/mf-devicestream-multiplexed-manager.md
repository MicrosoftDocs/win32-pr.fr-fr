---
description: Fournit une instance de IMFMuxStreamAttributesManager qui gère les IMFAttributes qui décrivent les sous-flux d’une source de média multiplexée.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: Attribut MF_DEVICESTREAM_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522677"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a>\_Attribut de \_ Gestionnaire Multiplexed DEVICESTREAM MF \_

Fournit une instance de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) qui gère les [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) qui décrivent les sous-flux d’une source de média multiplexée.

## <a name="data-type"></a>Type de données

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Notes

Transmettez cette valeur dans [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) pour déterminer si la source du média fournit des flux multiplexés et, si c’est le cas, obtenir une instance de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
