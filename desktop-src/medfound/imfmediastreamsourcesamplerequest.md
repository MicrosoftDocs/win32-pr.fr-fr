---
description: Représente une demande pour un exemple à partir d’un source.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Interface IMFMediaStreamSourceSampleRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: a0becbcef7e71f6859a9e4f09e81f98459911724127ade97e84de09e94a956f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941919"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a>Interface IMFMediaStreamSourceSampleRequest

Représente une demande pour un exemple à partir d’un source.

## <a name="members"></a>Membres

L’interface **IMFMediaStreamSourceSampleRequest** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMFMediaStreamSourceSampleRequest** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMFMediaStreamSourceSampleRequest** possède ces méthodes.



| Méthode                                                           | Description                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [**SetSample**](imfmediastreamsourcesamplerequest-setsample.md) | Définit l’exemple pour la source du flux multimédia.<br/> |



 

## <a name="remarks"></a>Remarques

**MFMediaStreamSourceSampleRequest** est implémenté par le [**Windows. Classe Runtime Media. Core. MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                       |
| MIDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces Media Foundation](media-foundation-interfaces.md)
</dt> </dl>

 

 
