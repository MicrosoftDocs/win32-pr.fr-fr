---
description: Spécifie une chaîne de contexte utilisée par les implémentations du module de déchiffrement de contenu (CDM) qui utilisent MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543106"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT, propriété

Spécifie une chaîne de contexte utilisée par les implémentations du module de déchiffrement de contenu (CDM) qui utilisent [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).


## <a name="data-type"></a>Type de données

**LPWStr** (VT_LPWSTR)

## <a name="property-guid"></a>Guid de propriété

**\_PMPSTORECONTEXT CONTENTDECRYPTIONMODULE \_ MF**

## <a name="property-value"></a>Valeur de la propriété

Chaîne de contexte utilisée par les implémentations du module de déchiffrement de contenu (CDM).

## <a name="remarks"></a>Notes

L’implémenteur CDM doit rechercher cette valeur et transmettre la valeur au [constructeur MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) à l’aide du nom de propriété « Windows. Media. protection. PMPStoreContext ».


Les applications ne doivent pas créer cette propriété lors de l’appel de [IMFContentDecryptionModuleAccess :: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Mise à jour 2020 de Windows 10 avril<br/>                                     |
| En-tête<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

- [Propriétés de la Media Foundation](media-foundation-properties.md)
- [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




