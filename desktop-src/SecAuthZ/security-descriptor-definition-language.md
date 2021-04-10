---
description: Explique le langage SDDL (Security Descriptor Definition Language).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Langage de définition du descripteur de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9de9d3535efe5c33ac633a9dbd295405d74b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863013"
---
# <a name="security-descriptor-definition-language"></a><span data-ttu-id="eb0e1-103">Langage de définition du descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="eb0e1-103">Security Descriptor Definition Language</span></span>

<span data-ttu-id="eb0e1-104">Le langage SDDL (Security Descriptor Definition Language) définit le format de chaîne que les fonctions [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) utilisent pour décrire un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="eb0e1-104">The security descriptor definition language (SDDL) defines the string format that the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use to describe a [*security descriptor*](/windows/desktop/SecGloss/s-gly) as a text string.</span></span> <span data-ttu-id="eb0e1-105">Le langage définit également des éléments de chaîne pour décrire les informations dans les composants d’un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="eb0e1-105">The language also defines string elements for describing information in the components of a security descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="eb0e1-106">Les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) conditionnel (ACE) ont un format SDDL différent des autres types ACE.</span><span class="sxs-lookup"><span data-stu-id="eb0e1-106">Conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) have a different SDDL format than other ACE types.</span></span> <span data-ttu-id="eb0e1-107">Pour les ACE, consultez [chaînes ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="eb0e1-107">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="eb0e1-108">Pour les ACE conditionnelles, consultez [langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="eb0e1-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eb0e1-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb0e1-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb0e1-110">Format de chaîne de descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="eb0e1-110">Security Descriptor String Format</span></span>](security-descriptor-string-format.md)
</dt> <dt>

[<span data-ttu-id="eb0e1-111">Langage de définition du descripteur de sécurité pour les ACE conditionnelles</span><span class="sxs-lookup"><span data-stu-id="eb0e1-111">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="eb0e1-112">Chaînes ACE</span><span class="sxs-lookup"><span data-stu-id="eb0e1-112">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="eb0e1-113">Chaînes SID</span><span class="sxs-lookup"><span data-stu-id="eb0e1-113">SID Strings</span></span>](sid-strings.md)
</dt> <dt>

<span data-ttu-id="eb0e1-114">[\[MS-DTYP \] : langage de description du descripteur de sécurité](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="eb0e1-114">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

 

 
