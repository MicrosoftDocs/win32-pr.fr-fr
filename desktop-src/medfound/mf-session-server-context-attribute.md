---
description: Permet à deux instances de la session multimédia de partager le même processus PMP (Protected Media Path).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Attribut MF_SESSION_SERVER_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc9674a2e25a7cdfd0a88ebcc43c18d6fd636bf22116f76a24255b55f857a677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102335"
---
# <a name="mf_session_server_context-attribute"></a>\_Attribut de \_ contexte de serveur de session MF \_

Permet à deux instances de la session multimédia de partager le même processus PMP (Protected Media Path).

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Remarques

Utilisez cet attribut si vous souhaitez créer la session de média PMP dans un processus PMP existant. La valeur de l’attribut est un pointeur vers l’interface [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .

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

[Attributs de session multimédia](media-session-attributes.md)
</dt> </dl>

 

 




