---
description: Contient un pointeur vers le descripteur de présentation pour la source du média.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: Attribut MF_TOPONODE_PRESENTATION_DESCRIPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bfa43a57bcead1312ba8138ab085771d29a008fe2558ea7c6bfb29121d631bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113705"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a>\_Attribut de \_ descripteur de présentation TOPONODE MF \_

Contient un pointeur vers le descripteur de présentation pour la source du média.

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux nœuds sources (**\_ \_ \_ nœud SOURCESTREAM de topologie MF**).

La valeur de l’attribut est un pointeur vers l’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) du descripteur de présentation. Cet attribut est obligatoire.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



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

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




