---
description: Contient un pointeur vers le descripteur de présentation à partir du chemin d’accès du média protégé (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: Attribut MF_PD_APP_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295398"
---
# <a name="mf_pd_app_context-attribute"></a>Attribut de contexte de l' \_ application MF PD \_ \_

Contient un pointeur vers le descripteur de présentation à partir du chemin d’accès du média protégé (PMP).

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Notes

Le proxy de source multimédia, qui est créé dans le processus PMP, utilise cet attribut pour stocker le descripteur de présentation distant sur le descripteur de présentation de l’application.

La valeur de cet attribut est un pointeur vers l’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

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

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes :: Setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




