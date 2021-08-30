---
description: Fournit une instance de IMFMuxStreamAttributesManager qui gère les IMFAttributes qui décrivent les sous-flux d’une source de média multiplexée.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: Attribut MF_DEVICESTREAM_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c022f2bb74756ce1a6afe471c23911c90a208e2940e9919f275df10a78ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956659"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a>\_Attribut de \_ Gestionnaire Multiplexed DEVICESTREAM MF \_

Fournit une instance de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) qui gère les [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) qui décrivent les sous-flux d’une source de média multiplexée.

## <a name="data-type"></a>Type de données

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Remarques

Transmettez cette valeur dans [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) pour déterminer si la source du média fournit des flux multiplexés et, si c’est le cas, obtenir une instance de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
