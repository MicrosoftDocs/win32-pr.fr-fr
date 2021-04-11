---
description: Contient un pointeur vers le descripteur de présentation à partir du chemin d’accès du média protégé (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: Attribut MF_PD_APP_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209789"
---
# <a name="mf_pd_app_context-attribute"></a>Attribut de contexte de l' \_ application MF PD \_ \_

Contient un pointeur vers le descripteur de présentation à partir du chemin d’accès du média protégé (PMP).

## <a name="data-type"></a>Type de données

**IUnknown \** _

## <a name="remarks"></a>Notes

Le proxy de source multimédia, qui est créé dans le processus PMP, utilise cet attribut pour stocker le descripteur de présentation distant sur le descripteur de présentation de l’application.

La valeur de cet attribut est un pointeur vers l’interface [_ *IMFPresentationDescriptor* *](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

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

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes :: Setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




