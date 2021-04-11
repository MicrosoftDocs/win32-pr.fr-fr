---
title: Descripteur de sécurité par défaut
description: Avec Active Directory Domain Services, vous pouvez également spécifier la sécurité par défaut pour chaque type d’objet.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Descripteur de sécurité par défaut AD
- descripteurs de sécurité Active Directory, par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031025"
---
# <a name="default-security-descriptor"></a><span data-ttu-id="35514-105">Descripteur de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="35514-105">Default Security Descriptor</span></span>

<span data-ttu-id="35514-106">Avec Active Directory Domain Services, vous pouvez également spécifier la sécurité par défaut pour chaque type d’objet.</span><span class="sxs-lookup"><span data-stu-id="35514-106">With Active Directory Domain Services, you can also specify default security for each type of object.</span></span> <span data-ttu-id="35514-107">Cela est spécifié dans l’attribut [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de la définition de l’objet [**classSchema**](/windows/desktop/ADSchema/c-classschema) dans le [schéma Active Directory](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="35514-107">This is specified in the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) attribute in the [**classSchema**](/windows/desktop/ADSchema/c-classschema) object definition in the [Active Directory schema](active-directory-schema.md).</span></span> <span data-ttu-id="35514-108">Ce descripteur de sécurité est utilisé pour fournir la protection par défaut sur l’objet si aucun descripteur de sécurité n’est spécifié lors de la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35514-108">This security descriptor is used to provide default protection on the object if there is no security descriptor specified during the creation of the object.</span></span>

> [!Note]  
> <span data-ttu-id="35514-109">Les entrées du descripteur de sécurité par défaut sont gérées comme si elles avaient été spécifiées dans le cadre de la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35514-109">ACEs from a default security descriptor are handled as if they were specified as part of object creation.</span></span> <span data-ttu-id="35514-110">Par conséquent, les ACE par défaut sont placées avant les ACE héritées et les remplacent, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="35514-110">Therefore, the default ACEs are placed preceding inherited ACEs and override them as appropriate.</span></span> <span data-ttu-id="35514-111">Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="35514-111">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="35514-112">Le [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) est spécifié dans un format de chaîne spécial à l’aide du langage SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ).</span><span class="sxs-lookup"><span data-stu-id="35514-112">The [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) is specified in a special string format using the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="35514-113">Deux fonctions peuvent être utilisées pour convertir le format binaire du descripteur de sécurité en format de chaîne et vice versa.</span><span class="sxs-lookup"><span data-stu-id="35514-113">Two functions can be used to convert binary form of the security descriptor to string format and vice versa.</span></span> <span data-ttu-id="35514-114">Ces fonctions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="35514-114">These functions are:</span></span>

-   [<span data-ttu-id="35514-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="35514-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [<span data-ttu-id="35514-116">Convertstringsecuritydescriptortosecuritydescriptor a</span><span class="sxs-lookup"><span data-stu-id="35514-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

<span data-ttu-id="35514-117">Pour plus d’informations et pour connaître les descripteurs de sécurité par défaut des classes d’objets prédéfinies, consultez les pages de référence de la classe dans la référence de schéma Active Directory de la [référence de Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="35514-117">For more information and the default security descriptors of the predefined object classes, see the class reference pages in the Active Directory Schema Reference of the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="35514-118">Pour plus d’informations et pour obtenir un exemple de code qui lit ou modifie la propriété [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) d’une classe d’objet, consultez [lecture du DefaultSecurityDescriptor pour une classe d’objet](reading-the-defaultsecuritydescriptor-for-an-object-class.md) et [modification de DefaultSecurityDescriptor pour une classe d’objet](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span><span class="sxs-lookup"><span data-stu-id="35514-118">For more information and a code example that reads or modifies the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) property of an object class, see [Reading the defaultSecurityDescriptor for an Object Class](reading-the-defaultsecuritydescriptor-for-an-object-class.md) and [Modifying the defaultSecurityDescriptor for an Object Class](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span></span>

 

 