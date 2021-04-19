---
description: Fournit une interface de rappel permettant à l’application de recevoir un objet d’activateur de contenu à partir de la session de chemin d’accès multimédia protégée (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: Attribut MF_SESSION_CONTENT_PROTECTION_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520636"
---
# <a name="mf_session_content_protection_manager-attribute"></a>\_Attribut de \_ Content \_ protection \_ Manager de session MF

Fournit une interface de rappel permettant à l’application de recevoir un objet d’activateur de contenu à partir de la session de chemin d’accès multimédia protégée (PMP).

## <a name="data-type"></a>Type de données

**IUnknown \** _

## <a name="remarks"></a>Notes

La valeur de cet attribut est un pointeur vers l’interface [_ *IMFContentProtectionManager* *](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de l’application.

Définissez cet attribut sur la session PMP à l’aide du paramètre *pConfiguration* de la fonction [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

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

[Attributs de session multimédia](media-session-attributes.md)
</dt> <dt>

[Comment lire des fichiers multimédias protégés](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




