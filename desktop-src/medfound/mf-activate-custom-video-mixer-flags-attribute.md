---
description: Spécifie comment créer un mélangeur personnalisé pour le convertisseur vidéo amélioré (EVR).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414233"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>\_Attribut d' \_ \_ indicateur de \_ mélangeur vidéo personnalisé MF activé \_

Spécifie comment créer un mélangeur personnalisé pour le convertisseur vidéo amélioré (EVR).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Vous pouvez définir cet attribut sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtenu à partir de la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) . La valeur de cet attribut est **une opération or au niveau du bit** des valeurs suivantes.



| Valeur                                      | Description                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ALLOWFAIL de \_ \_ mixage personnalisé \_ MF MF** | Si la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ne parvient pas à créer le mélangeur personnalisé de l’application, elle utilise à la place le mélangeur EVR par défaut. Par défaut, si l’objet [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) échoue lors de la tentative de création du mélangeur personnalisé, la méthode **ActivateObject** échoue. |



 

Les applications peuvent utiliser l’attribut [**\_ \_ \_ \_ \_ CLSID du mélangeur vidéo personnalisé MF activer**](mf-activate-custom-video-mixer-clsid-attribute.md) pour spécifier un mélangeur personnalisé pour le EVR.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de convertisseur vidéo améliorés](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Objets d’activation](activation-objects.md)
</dt> </dl>

 

 




