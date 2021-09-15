---
description: Fournit une interface de rappel permettant à l’application de recevoir un objet d’activateur de contenu à partir de la session de chemin d’accès multimédia protégée (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: Attribut MF_SESSION_CONTENT_PROTECTION_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523636"
---
# <a name="mf_session_content_protection_manager-attribute"></a>\_Attribut de \_ Content \_ protection \_ Manager de session MF

Fournit une interface de rappel permettant à l’application de recevoir un objet d’activateur de contenu à partir de la session de chemin d’accès multimédia protégée (PMP).

## <a name="data-type"></a>Type de données

**IUnknown\***

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur vers l’interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de l’application.

Définissez cet attribut sur la session PMP à l’aide du paramètre *pConfiguration* de la fonction [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

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
</dt> <dt>

[Comment lire des fichiers multimédias protégés](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




