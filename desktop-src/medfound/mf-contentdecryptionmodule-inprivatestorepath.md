---
description: Spécifie un chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour les données spécifiques au contenu.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: bf03d4411ac2959a336b931bc5e45ec969772ab35c194de03cbd9c74aaca0c0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244772"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH, propriété

Spécifie un chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour les données spécifiques au contenu.


## <a name="data-type"></a>Type de données

**LPWStr** (VT_LPWSTR)

## <a name="property-guid"></a>Guid de propriété

**\_INPRIVATESTOREPATH CONTENTDECRYPTIONMODULE \_ MF**

## <a name="property-value"></a>Valeur de la propriété

Chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour les données spécifiques au contenu.

## <a name="remarks"></a>Notes

L’application doit supprimer l’emplacement du magasin après la libération de l’objet CDM.

Si cette propriété n’est pas définie, le système utilise le chemin d’accès spécifié avec la propriété [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) pour les données spécifiques au contenu.

Définissez cette propriété lorsque vous créez un CDM en appelant [IMFContentDecryptionModuleAccess :: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 Mise à jour d’avril 2020<br/>                                     |
| En-tête<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

- [Propriétés de la Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




