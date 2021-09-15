---
description: Permet à deux instances de la session multimédia de partager le même processus PMP (Protected Media Path).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Attribut MF_SESSION_SERVER_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525737"
---
# <a name="mf_session_server_context-attribute"></a>\_Attribut de \_ contexte de serveur de session MF \_

Permet à deux instances de la session multimédia de partager le même processus PMP (Protected Media Path).

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Notes

Utilisez cet attribut si vous souhaitez créer la session de média PMP dans un processus PMP existant. La valeur de l’attribut est un pointeur vers l’interface [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .

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

[Attributs de session multimédia](media-session-attributes.md)
</dt> </dl>

 

 




