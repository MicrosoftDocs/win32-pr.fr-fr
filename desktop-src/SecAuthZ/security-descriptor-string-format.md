---
description: Le format de chaîne de descripteur de sécurité est un format texte permettant de stocker ou de transporter des informations dans un descripteur de sécurité.
ms.assetid: 0a226629-084c-40c5-bdd4-ad7355c807cf
title: Format de chaîne de descripteur de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42780c408908faf0a226584be7315ab6bf9e78e5
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925681"
---
# <a name="security-descriptor-string-format"></a><span data-ttu-id="1d2d7-103">Format de chaîne de descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="1d2d7-103">Security Descriptor String Format</span></span>

<span data-ttu-id="1d2d7-104">Le **format de chaîne de descripteur de sécurité** est un format texte permettant de stocker ou de transporter des informations dans un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-104">The **Security Descriptor String Format** is a text format for storing or transporting information in a security descriptor.</span></span> <span data-ttu-id="1d2d7-105">Les fonctions [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) utilisent ce format.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-105">The [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use this format.</span></span>

<span data-ttu-id="1d2d7-106">Le format est une chaîne se terminant par un caractère **null** avec des jetons pour indiquer chacun des quatre composants principaux d’un descripteur de sécurité : propriétaire (O :), groupe principal (G :), DACL (D :) et SACL (S :).</span><span class="sxs-lookup"><span data-stu-id="1d2d7-106">The format is a **null**-terminated string with tokens to indicate each of the four main components of a security descriptor: owner (O:), primary group (G:), DACL (D:), and SACL (S:).</span></span>

> [!Note]  
> <span data-ttu-id="1d2d7-107">Les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) et les ACE conditionnelles ont des formats différents.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-107">[*Access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and conditional ACEs have differing formats.</span></span> <span data-ttu-id="1d2d7-108">Pour les ACE, consultez [chaînes ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="1d2d7-108">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="1d2d7-109">Pour les ACE conditionnelles, consultez [langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="1d2d7-109">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 


```C++
O:owner_sid
G:group_sid
D:dacl_flags(string_ace1)(string_ace2)... (string_acen)
S:sacl_flags(string_ace1)(string_ace2)... (string_acen)
```



<dl> <dt>

<span data-ttu-id="1d2d7-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>sid du propriétaire \_</span><span class="sxs-lookup"><span data-stu-id="1d2d7-110"><span id="owner_sid"></span><span id="OWNER_SID"></span>owner\_sid</span></span>
</dt> <dd>

<span data-ttu-id="1d2d7-111">[Chaîne sid](sid-strings.md) qui identifie le propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-111">A [SID string](sid-strings.md) that identifies the object's owner.</span></span>

</dd> <dt>

<span data-ttu-id="1d2d7-112"><span id="group_sid"></span><span id="GROUP_SID"></span>sid du groupe \_</span><span class="sxs-lookup"><span data-stu-id="1d2d7-112"><span id="group_sid"></span><span id="GROUP_SID"></span>group\_sid</span></span>
</dt> <dd>

<span data-ttu-id="1d2d7-113">Chaîne SID qui identifie le groupe principal de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-113">A SID string that identifies the object's primary group.</span></span>

</dd> <dt>

<span data-ttu-id="1d2d7-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>\_indicateurs DACL</span><span class="sxs-lookup"><span data-stu-id="1d2d7-114"><span id="dacl_flags"></span><span id="DACL_FLAGS"></span>dacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="1d2d7-115">Indicateurs de contrôle du descripteur de sécurité qui s’appliquent à la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-115">Security descriptor control flags that apply to the DACL.</span></span> <span data-ttu-id="1d2d7-116">Pour obtenir une description de ces indicateurs de contrôle, consultez la fonction [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) .</span><span class="sxs-lookup"><span data-stu-id="1d2d7-116">For a description of these control flags, see the [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) function.</span></span> <span data-ttu-id="1d2d7-117">La \_ chaîne d’indicateurs DACL peut être une concaténation de zéro ou plusieurs des chaînes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-117">The dacl\_flags string can be a concatenation of zero or more of the following strings.</span></span>



| <span data-ttu-id="1d2d7-118">Contrôler</span><span class="sxs-lookup"><span data-stu-id="1d2d7-118">Control</span></span>               | <span data-ttu-id="1d2d7-119">Constante dans SDDL. h</span><span class="sxs-lookup"><span data-stu-id="1d2d7-119">Constant in Sddl.h</span></span>       | <span data-ttu-id="1d2d7-120">Signification</span><span class="sxs-lookup"><span data-stu-id="1d2d7-120">Meaning</span></span>                                       |
|-----------------------|--------------------------|-----------------------------------------------|
| <span data-ttu-id="1d2d7-121">P</span><span class="sxs-lookup"><span data-stu-id="1d2d7-121">"P"</span></span>                   | <span data-ttu-id="1d2d7-122">SDDL \_ protégé</span><span class="sxs-lookup"><span data-stu-id="1d2d7-122">SDDL\_PROTECTED</span></span>          | <span data-ttu-id="1d2d7-123">L' \_ indicateur de \_ protection discrétionnaire se est défini.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-123">The SE\_DACL\_PROTECTED flag is set.</span></span>          |
| <span data-ttu-id="1d2d7-124">AR</span><span class="sxs-lookup"><span data-stu-id="1d2d7-124">"AR"</span></span>                  | <span data-ttu-id="1d2d7-125">\_demande d' \_ héritage \_ automatique SDDL</span><span class="sxs-lookup"><span data-stu-id="1d2d7-125">SDDL\_AUTO\_INHERIT\_REQ</span></span> | <span data-ttu-id="1d2d7-126">L’indicateur de demande d’héritage automatique de la liste d’accès \_ discrétionnaire \_ \_ \_ est défini.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-126">The SE\_DACL\_AUTO\_INHERIT\_REQ flag is set.</span></span> |
| <span data-ttu-id="1d2d7-127">AI</span><span class="sxs-lookup"><span data-stu-id="1d2d7-127">"AI"</span></span>                  | <span data-ttu-id="1d2d7-128">SDDL \_ \_ hérité automatiquement</span><span class="sxs-lookup"><span data-stu-id="1d2d7-128">SDDL\_AUTO\_INHERITED</span></span>    | <span data-ttu-id="1d2d7-129">L' \_ indicateur d’héritage automatique de la liste de \_ \_ rédépendance se définit.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-129">The SE\_DACL\_AUTO\_INHERITED flag is set.</span></span>    |
| <span data-ttu-id="1d2d7-130">« AUCUN \_ contrôle d’accès \_ »</span><span class="sxs-lookup"><span data-stu-id="1d2d7-130">"NO\_ACCESS\_CONTROL"</span></span> | <span data-ttu-id="1d2d7-131">ACL de la \_ valeur SDDL null \_</span><span class="sxs-lookup"><span data-stu-id="1d2d7-131">SDDL\_NULL\_ACL</span></span>          | <span data-ttu-id="1d2d7-132">La liste de contrôle d’accès a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-132">The ACL is null.</span></span>                              |



 

</dd> <dt>

<span data-ttu-id="1d2d7-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>\_indicateurs SACL</span><span class="sxs-lookup"><span data-stu-id="1d2d7-133"><span id="sacl_flags"></span><span id="SACL_FLAGS"></span>sacl\_flags</span></span>
</dt> <dd>

<span data-ttu-id="1d2d7-134">Indicateurs de contrôle du descripteur de sécurité qui s’appliquent à la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-134">Security descriptor control flags that apply to the SACL.</span></span> <span data-ttu-id="1d2d7-135">La \_ chaîne d’indicateurs SACL utilise les mêmes chaînes de bits de contrôle que la \_ chaîne d’indicateurs DACL.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-135">The sacl\_flags string uses the same control bit strings as the dacl\_flags string.</span></span>

</dd> <dt>

<span data-ttu-id="1d2d7-136"><span id="string_ace"></span><span id="STRING_ACE"></span>chaîne \_ ACE</span><span class="sxs-lookup"><span data-stu-id="1d2d7-136"><span id="string_ace"></span><span id="STRING_ACE"></span>string\_ace</span></span>
</dt> <dd>

<span data-ttu-id="1d2d7-137">Chaîne qui décrit une entrée du contrôle d’accès dans la liste DACL ou SACL du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-137">A string that describes an ACE in the security descriptor's DACL or SACL.</span></span> <span data-ttu-id="1d2d7-138">Pour obtenir une description du format de chaîne ACE, consultez [chaînes ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="1d2d7-138">For a description of the ACE string format, see [ACE strings](ace-strings.md).</span></span> <span data-ttu-id="1d2d7-139">Chaque chaîne ACE est placée entre parenthèses (()).</span><span class="sxs-lookup"><span data-stu-id="1d2d7-139">Each ACE string is enclosed in parentheses (()).</span></span>

</dd> </dl>

<span data-ttu-id="1d2d7-140">Les composants inutiles peuvent être omis de la chaîne de descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-140">Unneeded components can be omitted from the security descriptor string.</span></span> <span data-ttu-id="1d2d7-141">Par exemple, si l' \_ \_ indicateur de présence DACL se n’est pas défini dans le descripteur de sécurité d’entrée, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) n’inclut pas de composant D : dans la chaîne de sortie.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-141">For example, if the SE\_DACL\_PRESENT flag is not set in the input security descriptor, [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) does not include a D: component in the output string.</span></span> <span data-ttu-id="1d2d7-142">Vous pouvez également utiliser les indicateurs de bits des [**\_ informations de sécurité**](security-information.md) pour indiquer les composants à inclure dans une chaîne de descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-142">You can also use the [**SECURITY\_INFORMATION**](security-information.md) bit flags to indicate the components to include in a security descriptor string.</span></span>

<span data-ttu-id="1d2d7-143">Le format de chaîne de descripteur de sécurité ne prend pas en charge les ACL **null** .</span><span class="sxs-lookup"><span data-stu-id="1d2d7-143">The security descriptor string format does not support **NULL** ACLs.</span></span>

<span data-ttu-id="1d2d7-144">Pour désigner une liste de contrôle d’accès vide, la chaîne de descripteur de sécurité comprend le jeton D : ou S : sans informations de chaîne supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-144">To denote an empty ACL, the security descriptor string includes the D: or S: token with no additional string information.</span></span>

<span data-ttu-id="1d2d7-145">La chaîne de descripteur de sécurité stocke les bits de [**contrôle de DEscripteur de sécurité**](security-descriptor-control.md) de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-145">The security descriptor string stores the [**SECURITY DESCRIPTOR CONTROL**](security-descriptor-control.md) bits in different ways.</span></span> <span data-ttu-id="1d2d7-146">Les éléments \_ de la liste de réédition DACL se présentent \_ par la \_ \_ présence du jeton D : ou S : dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-146">The SE\_DACL\_PRESENT or SE\_SACL\_PRESENT bits are indicated by the presence of the D: or S: token in the string.</span></span> <span data-ttu-id="1d2d7-147">Les autres bits qui s’appliquent à la liste DACL ou SACL sont stockés dans les \_ indicateurs DACL et les \_ indicateurs SACL.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-147">Other bits that apply to the DACL or SACL are stored in dacl\_flags and sacl\_flags.</span></span> <span data-ttu-id="1d2d7-148">Le propriétaire SE est \_ \_ par défaut, le groupe de se par défaut, le \_ \_ \_ DACL de se \_ par défaut et les \_ bits SACL par défaut de se ne \_ sont pas stockés dans une chaîne de descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-148">The SE\_OWNER\_DEFAULTED, SE\_GROUP\_DEFAULTED, SE\_DACL\_DEFAULTED, and SE\_SACL\_DEFAULTED bits are not stored in a security descriptor string.</span></span> <span data-ttu-id="1d2d7-149">Le \_ bit Auto \_ relatif de se n’est pas stocké dans la chaîne, mais [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) définit toujours ce bit dans le descripteur de sécurité de sortie.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-149">The SE\_SELF\_RELATIVE bit is not stored in the string, but [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) always sets this bit in the output security descriptor.</span></span>

<span data-ttu-id="1d2d7-150">Les exemples suivants montrent des chaînes de descripteur de sécurité et les informations contenues dans les descripteurs de sécurité associés.</span><span class="sxs-lookup"><span data-stu-id="1d2d7-150">The following examples show security descriptor strings and the information in the associated security descriptors.</span></span>

<span data-ttu-id="1d2d7-151">Chaîne 1 :</span><span class="sxs-lookup"><span data-stu-id="1d2d7-151">String 1:</span></span>


```C++
"O:AOG:DAD:(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-0-0)"
```



<span data-ttu-id="1d2d7-152">Descripteur de sécurité 1 :</span><span class="sxs-lookup"><span data-stu-id="1d2d7-152">Security Descriptor 1:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0004
        SE_DACL_PRESENT
    Owner: (S-1-5-32-548)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x02
    Size:     0x001c
    AceCount: 0x0001
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x100e003f
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            GENERIC_ALL
                            Others(0x0000003f)
        Ace Sid      : (S-1-0-0)
SACL
    Not present
```



<span data-ttu-id="1d2d7-153">Chaîne 2 :</span><span class="sxs-lookup"><span data-stu-id="1d2d7-153">String 2:</span></span>


```C++
"O:DAG:DAD:(A;;RPWPCCDCLCRCWOWDSDSW;;;SY)
(A;;RPWPCCDCLCRCWOWDSDSW;;;DA)
(OA;;CCDC;bf967aba-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;bf967a9c-0de6-11d0-a285-00aa003049e2;;AO)
(OA;;CCDC;6da8a4ff-0e52-11d0-a286-00aa003049e2;;AO)
(OA;;CCDC;bf967aa8-0de6-11d0-a285-00aa003049e2;;PO)
(A;;RPLCRC;;;AU)S:(AU;SAFA;WDWOSDWPCCDCSW;;;WD)"
```



<span data-ttu-id="1d2d7-154">Descripteur de sécurité 2 :</span><span class="sxs-lookup"><span data-stu-id="1d2d7-154">Security Descriptor 2:</span></span>


```C++
    Revision:  0x00000001
    Control:   0x0014
        SE_DACL_PRESENT
        SE_SACL_PRESENT
    Owner: (S-1-5-21-397955417-626881126-188441444-512)
    PrimaryGroup: (S-1-5-21-397955417-626881126-188441444-512)
DACL
    Revision: 0x04
    Size:     0x0104
    AceCount: 0x0007
    Ace[00]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-18)
    Ace[01]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0024
        InheritFlags:  0x00
        Access Mask:   0x000f003f
                            DELETE
                            READ_CONTROL
                            WRITE_DAC
                            WRITE_OWNER
                            Others(0x0000003f)
        Ace Sid:       (S-1-5-21-397955417-626881126-188441444-512)
    Ace[02]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_USER
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[03]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_GROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[04]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_LOCALGROUP
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-548)
    Ace[05]
        AceType:       0x05 (ACCESS_ALLOWED_OBJECT_ACE_TYPE)
        AceSize:       0x002c
        InheritFlags:  0x00
        Access Mask:   0x00000003
                            Others(0x00000003)
        Flags:         0x00000001, ACE_OBJECT_TYPE_PRESENT
        ObjectType:    GUID_C_PRINT_QUEUE
        InhObjectType: GUID ptr is NULL
        Ace Sid:       (S-1-5-32-550)
    Ace[06]
        AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
        AceSize:       0x0014
        InheritFlags:  0x00
        Access Mask:   0x00020014
                            READ_CONTROL
                            Others(0x00000014)
        Ace Sid:       (S-1-5-11)
    SACL
        Revision: 0x02
        Size:     0x001c
        AceCount: 0x0001
        Ace[00]
            AceType:       0x02 (SYSTEM_AUDIT_ACE_TYPE)
            AceSize:       0x0014
            InheritFlags:  0xc0
                SUCCESSFUL_ACCESS_ACE_FLAG
                FAILED_ACCESS_ACE_FLAG
            Access Mask:    0x000d002b
                                DELETE
                                WRITE_DAC
                                WRITE_OWNER
                                Others(0x0000002b)
            Ace Sid:       (S-1-1-0)
```



## <a name="related-topics"></a><span data-ttu-id="1d2d7-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d2d7-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d2d7-156">Chaînes ACE</span><span class="sxs-lookup"><span data-stu-id="1d2d7-156">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="1d2d7-157">Langage de définition du descripteur de sécurité pour les ACE conditionnelles</span><span class="sxs-lookup"><span data-stu-id="1d2d7-157">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 
