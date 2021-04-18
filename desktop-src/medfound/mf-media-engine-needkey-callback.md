---
description: Attribut qui est transmis dans le IMFMediaEngineNeedKeyNotify au moteur multimédia lors de la création.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: Attribut MF_MEDIA_ENGINE_NEEDKEY_CALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522504"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a>\_Attribut de \_ \_ rappel NEEDKEY du moteur multimédia MF \_

Attribut qui est transmis dans le [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) au moteur multimédia lors de la création.

## <a name="data-type"></a>Type de données

**IMFMediaEngineNeedKeyNotify \* *_ stocké en tant que _* IUnknown\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur vers l’interface [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) , implémentée par l’application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




