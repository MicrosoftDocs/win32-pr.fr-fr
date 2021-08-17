---
description: Attribut qui est transmis dans le IMFMediaEngineNeedKeyNotify au moteur multimédia lors de la création.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: Attribut MF_MEDIA_ENGINE_NEEDKEY_CALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bec8dd3b802d9fc378d43648ad1d29dd30b6573881a044cc9f0d3aba2015cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956309"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a>\_Attribut de \_ \_ rappel NEEDKEY du moteur multimédia MF \_

Attribut qui est transmis dans le [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) au moteur multimédia lors de la création.

## <a name="data-type"></a>Type de données

**IMFMediaEngineNeedKeyNotify \* *_ stocké en tant que _* IUnknown\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un pointeur vers l’interface [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) , implémentée par l’application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




