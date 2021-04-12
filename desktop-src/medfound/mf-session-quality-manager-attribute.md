---
description: Contient le CLSID d’un gestionnaire de qualité pour la session multimédia.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: Attribut MF_SESSION_QUALITY_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319638"
---
# <a name="mf_session_quality_manager-attribute"></a>\_Attribut de \_ Gestionnaire de qualité de session MF \_

Contient le CLSID d’un gestionnaire de qualité pour la session multimédia.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

Vous pouvez utiliser cet attribut pour fournir un gestionnaire de qualité personnalisé pour la session multimédia.

Définissez cet attribut à l’aide du paramètre *pConfiguration* de la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Si cet attribut est défini, la session multimédia appelle **CoCreateInstance** avec le CLSID spécifié pour créer le gestionnaire de qualité. L’objet créé par ce CLSID doit exposer l’interface [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .

Si cet attribut n’est pas défini, la session multimédia crée le gestionnaire de qualité par défaut fourni dans Media Foundation.

Si vous souhaitez exécuter la session multimédia sans le gestionnaire de qualité, définissez cet attribut sur **GUID \_ null**.

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

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Attributs de session multimédia](media-session-attributes.md)
</dt> </dl>

 

 




