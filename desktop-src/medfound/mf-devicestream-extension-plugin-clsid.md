---
description: Spécifie le CLSID d’un plug-in de traitement de message pour un périphérique de capture vidéo.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: Attribut MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a474d66bfaa079cfc7b5e483ad1f10b3c09e600437f841fc062db8f0ca611d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956699"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a>\_ \_ \_ Attribut CLSID du plug-in d’extension DEVICESTREAM MF \_

Spécifie le CLSID d’un plug-in de traitement de message pour un périphérique de capture vidéo.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Remarques

Un plug-in de traitement de billet est un MFT qui traite l’image vidéo après sa capture. Le fournisseur de matériel peut inclure un plug-in de retraitement dans le cadre du package d’installation. Si c’est le cas, la source de capture vidéo affecte \_ \_ à l' \_ attribut CLSID du plug-in d’extension DEVICESTREAM MF \_ le CLSID du plug-in.

Pour accéder à cet attribut, procédez comme suit :

1.  Interrogez la source du média pour l’interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) pour obtenir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour le flux.
3.  Appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) pour accéder à l’attribut.

Pour créer le plug-in, appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
