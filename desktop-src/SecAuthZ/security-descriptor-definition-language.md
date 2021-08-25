---
description: Explique le langage SDDL (Security Descriptor Definition Language).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Langage de définition du descripteur de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b72e74f49d34577251aef3d875a3c0e9aede07556be1b918ad532f3987c54d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907409"
---
# <a name="security-descriptor-definition-language"></a>Langage de définition du descripteur de sécurité

Le langage SDDL (Security Descriptor Definition Language) définit le format de chaîne que les fonctions [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) utilisent pour décrire un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) sous la forme d’une chaîne de texte. Le langage définit également des éléments de chaîne pour décrire les informations dans les composants d’un descripteur de sécurité.

> [!Note]  
> Les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) conditionnel (ACE) ont un format SDDL différent des autres types ACE. Pour les ACE, consultez [chaînes ACE](ace-strings.md). Pour les ACE conditionnelles, consultez [langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format de chaîne de descripteur de sécurité](security-descriptor-string-format.md)
</dt> <dt>

[Langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[Chaînes ACE](ace-strings.md)
</dt> <dt>

[Chaînes SID](sid-strings.md)
</dt> <dt>

[\[MS-DTYP \] : langage de description du descripteur de sécurité](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

 

 
