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
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414253"
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



 

## <a name="remarks"></a>Notes

**MFMediaStreamSourceSampleRequest** est implémenté par le [**Windows. Classe Runtime Media. Core. MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                       |
| MIDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces Media Foundation](media-foundation-interfaces.md)
</dt> </dl>

 

 
