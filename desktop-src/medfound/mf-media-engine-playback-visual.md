---
description: Définit un visuel Microsoft DirectComposition comme région de lecture pour le moteur multimédia.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: Attribut MF_MEDIA_ENGINE_PLAYBACK_VISUAL (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538956"
---
# <a name="mf_media_engine_playback_visual-attribute"></a>\_ \_ \_ Attribut visuel lecture du moteur multimédia MF \_

Définit un visuel Microsoft DirectComposition comme région de lecture pour le moteur multimédia.

## <a name="data-type"></a>Type de données

**IDCompositionVisual \* *_ stocké en tant que _* IUnknown\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Notes

Pour plus d’informations sur DirectComposition, consultez [DirectComposition](../directcomp/directcomposition-portal.md) et [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).

Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
