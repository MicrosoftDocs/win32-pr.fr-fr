---
description: Spécifie une chaîne de contexte utilisée par les implémentations du module de déchiffrement de contenu (CDM) qui utilisent MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: e82bfb5bcf833957fa07ec5aa5c6dacdab346905692ab7cfcf6cbb18b940817b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060713"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT, propriété

Spécifie une chaîne de contexte utilisée par les implémentations du module de déchiffrement de contenu (CDM) qui utilisent [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).


## <a name="data-type"></a>Type de données

**LPWStr** (VT_LPWSTR)

## <a name="property-guid"></a>Guid de propriété

**\_PMPSTORECONTEXT CONTENTDECRYPTIONMODULE \_ MF**

## <a name="property-value"></a>Valeur de la propriété

Chaîne de contexte utilisée par les implémentations du module de déchiffrement de contenu (CDM).

## <a name="remarks"></a>Remarques

L’implémenteur CDM doit rechercher cette valeur et transmettre la valeur au [constructeur MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) à l’aide du nom de propriété «Windows. Media. protection. PMPStoreContext».


Les applications ne doivent pas créer cette propriété lors de l’appel de [IMFContentDecryptionModuleAccess :: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 Mise à jour d’avril 2020<br/>                                     |
| En-tête<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

- [Propriétés de la Media Foundation](media-foundation-properties.md)
- [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




