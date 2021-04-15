---
description: Spécifie un chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour l’initialisation.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485217"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH, propriété

Spécifie un chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour l’initialisation.


## <a name="data-type"></a>Type de données

**LPWStr** (VT_LPWSTR)

## <a name="property-guid"></a>Guid de propriété

**\_STOREPATH CONTENTDECRYPTIONMODULE \_ MF**

## <a name="property-value"></a>Valeur de la propriété

Chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour l’initialisation.

## <a name="remarks"></a>Notes

Le chemin d’accès spécifié avec cette propriété sera également utilisé pour les données spécifiques au contenu si la propriété [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) n’est pas définie.

Pour améliorer les performances de COM, l’application ne doit pas supprimer l’emplacement du magasin après la publication de l’objet CDM.



Définissez cette propriété lorsque vous créez un CDM en appelant [IMFContentDecryptionModuleAccess :: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Mise à jour 2020 de Windows 10 avril<br/>                                     |
| En-tête<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

- [Propriétés de la Media Foundation](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




