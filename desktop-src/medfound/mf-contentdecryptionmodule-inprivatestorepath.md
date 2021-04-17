---
description: Spécifie un chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour les données spécifiques au contenu.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526901"
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
| Client minimal pris en charge<br/> | Mise à jour 2020 de Windows 10 avril<br/>                                     |
| En-tête<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

- [Propriétés de la Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




