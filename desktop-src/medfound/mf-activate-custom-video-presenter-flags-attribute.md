---
description: Spécifie comment créer un présentateur personnalisé pour le convertisseur vidéo amélioré (EVR).
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: Attribut MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3681edaed39b63b0f7c13313039f1c6e72311a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034831"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a>\_ \_ \_ \_ Attribut indicateurs de présentateur vidéo personnalisé MF activé \_

Spécifie comment créer un présentateur personnalisé pour le convertisseur vidéo amélioré (EVR).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Vous pouvez définir cet attribut sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtenu à partir de la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) . La valeur de cet attribut est **une opération or au niveau du bit** des valeurs suivantes.



| Valeur                                          | Description                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ activer \_ le \_ présentateur personnalisé \_ ALLOWFAIL** | Si la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ne parvient pas à créer le présentateur personnalisé de l’application, il utilise à la place le présentateur EVR par défaut. Par défaut, si l’objet [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) échoue lorsqu’il tente de créer le présentateur personnalisé, la méthode **ActivateObject** échoue. |



 

Les applications peuvent utiliser l’attribut de [**\_ CLSID d’activation de \_ \_ vidéo \_ \_ personnalisée MF**](mf-activate-custom-video-presenter-clsid-attribute.md) pour spécifier un présentateur personnalisé pour le EVR.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
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
</dt> <dt>

[Comment écrire un présentateur EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




