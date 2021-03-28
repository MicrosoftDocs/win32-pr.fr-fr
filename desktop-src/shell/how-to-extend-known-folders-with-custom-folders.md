---
description: Les éditeurs de logiciels indépendants (ISV) peuvent étendre l’ensemble des dossiers connus sur un système en inscrivant leurs propres dossiers connus.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Comment étendre des dossiers connus avec des dossiers personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202780"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>Comment étendre des dossiers connus avec des dossiers personnalisés

Les éditeurs de logiciels indépendants (ISV) peuvent étendre l’ensemble des dossiers connus sur un système en inscrivant leurs propres dossiers connus. Une fois inscrits, ces dossiers tiers sont connus du système. Ils sont trouvés par un appel à [**IKnownFolderManager :: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids). Notez qu’un dossier connu doit être un dossier par ordinateur. Vous ne pouvez pas créer un dossier connu par utilisateur.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Définissez votre dossier connu via une structure de [**\_ définition KNOWNFOLDER**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .

### <a name="step-2"></a>Étape 2 :

Inscrivez le dossier connu via un appel à [**IKnownFolderManager :: RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).

## <a name="remarks"></a>Notes

Si vous créez un dossier connu pour votre application dans le cadre de votre procédure d’installation, vous devez également inclure [**IKnownFolderManager :: UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) dans le cadre de votre code de désinstallation.

Prenez en compte la raison pour laquelle vous souhaitez que votre dossier soit inclus dans le système de dossiers connu avant de l’inscrire. Vous devez avoir une raison valable d’élever votre dossier à ce niveau de visibilité du système.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Dossiers connus, exemple](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
