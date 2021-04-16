---
description: WMI a des objets et des méthodes qui vous permettent de lire et manipuler les descripteurs de sécurité pour déterminer qui a accès aux objets sécurisables.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Objets descripteurs de sécurité WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550399"
---
# <a name="wmi-security-descriptor-objects"></a><span data-ttu-id="aef64-103">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="aef64-103">WMI Security Descriptor Objects</span></span>

<span data-ttu-id="aef64-104">WMI a des objets et des méthodes qui vous permettent de lire et manipuler les descripteurs de sécurité pour déterminer qui a accès aux objets sécurisables.</span><span class="sxs-lookup"><span data-stu-id="aef64-104">WMI has objects and methods that allow you to read and manipulate security descriptors to determine who has access to securable objects.</span></span>

-   [<span data-ttu-id="aef64-105">Rôle des descripteurs de sécurité</span><span class="sxs-lookup"><span data-stu-id="aef64-105">The Role of Security Descriptors</span></span>](#the-role-of-security-descriptors)
-   [<span data-ttu-id="aef64-106">Objets de sécurité Access Control et WMI</span><span class="sxs-lookup"><span data-stu-id="aef64-106">Access Control and WMI Security Objects</span></span>](#access-control-and-wmi-security-objects)
-   [<span data-ttu-id="aef64-107">\_Objet Win32 SecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="aef64-107">Win32\_SecurityDescriptor Object</span></span>](/windows)
-   [<span data-ttu-id="aef64-108">DACL et SACL</span><span class="sxs-lookup"><span data-stu-id="aef64-108">DACL and SACL</span></span>](#dacl-and-sacl)
-   [<span data-ttu-id="aef64-109">\_ACE Win32, \_ approuvé Win32, \_ sid Win32</span><span class="sxs-lookup"><span data-stu-id="aef64-109">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>](/windows)
-   [<span data-ttu-id="aef64-110">Exemple : vérification de l’accès aux imprimantes</span><span class="sxs-lookup"><span data-stu-id="aef64-110">Example: Checking Who has Access to Printers</span></span>](#example-checking-who-has-access-to-printers)
-   [<span data-ttu-id="aef64-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aef64-111">Related topics</span></span>](#related-topics)

## <a name="the-role-of-security-descriptors"></a><span data-ttu-id="aef64-112">Rôle des descripteurs de sécurité</span><span class="sxs-lookup"><span data-stu-id="aef64-112">The Role of Security Descriptors</span></span>

<span data-ttu-id="aef64-113">Les descripteurs de sécurité définissent les attributs de sécurité des objets sécurisables tels que les fichiers, les clés de Registre, les espaces de noms WMI, les imprimantes, les services ou les partages.</span><span class="sxs-lookup"><span data-stu-id="aef64-113">Security descriptors define the security attributes of securable objects such as files, registry keys, WMI namespaces, printers, services, or shares.</span></span> <span data-ttu-id="aef64-114">Un descripteur de sécurité contient des informations sur le propriétaire et le groupe principal d’un objet.</span><span class="sxs-lookup"><span data-stu-id="aef64-114">A security descriptor contains information about the owner and primary group of an object.</span></span> <span data-ttu-id="aef64-115">Un fournisseur peut comparer le descripteur de sécurité des ressources à l’identité d’un utilisateur demandeur et déterminer si l’utilisateur a le droit d’accéder à la ressource demandée par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aef64-115">A provider can compare the resource security descriptor to the identity of a requesting user, and determine whether or not the user has the right to access the resource that a user is requesting.</span></span> <span data-ttu-id="aef64-116">Pour plus d’informations, consultez [accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="aef64-116">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="aef64-117">Certaines méthodes WMI, telles que [**est**](--systemsecurity-getsd.md), retournent un descripteur de sécurité dans le format de tableau d’octets binaire.</span><span class="sxs-lookup"><span data-stu-id="aef64-117">Some WMI methods, such as [**GetSD**](--systemsecurity-getsd.md), return a security descriptor in the binary byte array format.</span></span> <span data-ttu-id="aef64-118">À compter de Windows Vista, utilisez les méthodes de la classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) pour convertir un descripteur de sécurité binaire en une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), qui peut être manipulée plus facilement.</span><span class="sxs-lookup"><span data-stu-id="aef64-118">Starting with Windows Vista, use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to convert a binary security descriptor to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), which can be manipulated more easily.</span></span> <span data-ttu-id="aef64-119">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="aef64-119">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="access-control-and-wmi-security-objects"></a><span data-ttu-id="aef64-120">Objets de sécurité Access Control et WMI</span><span class="sxs-lookup"><span data-stu-id="aef64-120">Access Control and WMI Security Objects</span></span>

<span data-ttu-id="aef64-121">La liste suivante répertorie les objets de sécurité WMI :</span><span class="sxs-lookup"><span data-stu-id="aef64-121">The following is a list of WMI security objects:</span></span>

-   [<span data-ttu-id="aef64-122">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="aef64-122">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [<span data-ttu-id="aef64-123">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="aef64-123">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [<span data-ttu-id="aef64-124">**\_Confiance Win32**</span><span class="sxs-lookup"><span data-stu-id="aef64-124">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [<span data-ttu-id="aef64-125">**\_Sid Win32**</span><span class="sxs-lookup"><span data-stu-id="aef64-125">**Win32\_SID**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

<span data-ttu-id="aef64-126">Le diagramme suivant montre les relations entre les objets de sécurité WMI.</span><span class="sxs-lookup"><span data-stu-id="aef64-126">The following diagram shows the relationships among WMI security objects.</span></span>

![relations entre les objets de sécurité WMI](images/security-descriptor.png)

<span data-ttu-id="aef64-128">Pour plus d’informations sur le rôle de sécurité d’accès, consultez [meilleures pratiques de sécurité](/windows/desktop/SecBP/best-practices-for-the-security-apis), [maintenance de la sécurité WMI](maintaining-wmi-security.md)et [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="aef64-128">For more information about the role of access security, see [Security Best Practices](/windows/desktop/SecBP/best-practices-for-the-security-apis), [Maintaining WMI Security](maintaining-wmi-security.md), and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

## <a name="win32_securitydescriptor-object"></a><span data-ttu-id="aef64-129">\_Objet Win32 SecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="aef64-129">Win32\_SecurityDescriptor Object</span></span>

<span data-ttu-id="aef64-130">Le tableau suivant répertorie les propriétés de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="aef64-130">The following table lists the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class properties.</span></span>



| <span data-ttu-id="aef64-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="aef64-131">Property</span></span>         | <span data-ttu-id="aef64-132">Description</span><span class="sxs-lookup"><span data-stu-id="aef64-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef64-133">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="aef64-133">**ControlFlags**</span></span> | <span data-ttu-id="aef64-134">Ensemble de bits de contrôle qui qualifient la signification d’un SD ou de ses membres individuels.</span><span class="sxs-lookup"><span data-stu-id="aef64-134">Set of control bits that qualify the meaning of an SD or its individual members.</span></span> <span data-ttu-id="aef64-135">Pour plus d’informations sur la définition des valeurs de bit **ControlFlags** , consultez [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="aef64-135">For more information about setting the **ControlFlags** bit values, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span><br/>                                                                                                                                                                      |
| <span data-ttu-id="aef64-136">**DACL**</span><span class="sxs-lookup"><span data-stu-id="aef64-136">**DACL**</span></span>         | <span data-ttu-id="aef64-137">[Liste de Access Control discrétionnaire (ACL)](/windows/desktop/SecAuthZ/access-control-lists) d’utilisateurs et de groupes et leurs droits d’accès à un objet sécurisé.</span><span class="sxs-lookup"><span data-stu-id="aef64-137">[Discretionary Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) of users and groups, and their access rights to a secured object.</span></span> <span data-ttu-id="aef64-138">Cette propriété contient un tableau d’instances de l' [**\_ entrée**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) de contrôle d’accès Win32 qui représentent les [entrées Access Control](/windows/desktop/SecAuthZ/access-control-entries).</span><span class="sxs-lookup"><span data-stu-id="aef64-138">This property contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent [Access Control Entries](/windows/desktop/SecAuthZ/access-control-entries).</span></span> <span data-ttu-id="aef64-139">Pour plus d’informations, consultez [création d’une liste DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="aef64-139">For more information, see [Creating a DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span><br/> |
| <span data-ttu-id="aef64-140">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="aef64-140">**Group**</span></span>        | <span data-ttu-id="aef64-141">Groupe auquel appartient cet objet sécurisé.</span><span class="sxs-lookup"><span data-stu-id="aef64-141">Group to which this secured object belongs.</span></span> <span data-ttu-id="aef64-142">Cette propriété contient une instance de [**l' \_ approbation Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) qui contient le nom, le domaine et l’identificateur de sécurité (SID) du groupe auquel appartient le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="aef64-142">This property contains an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the group to which the owner belongs.</span></span><br/>                                                                                                                                                             |
| <span data-ttu-id="aef64-143">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="aef64-143">**Owner**</span></span>        | <span data-ttu-id="aef64-144">Propriétaire de cet objet sécurisé.</span><span class="sxs-lookup"><span data-stu-id="aef64-144">Owner of this secured object.</span></span> <span data-ttu-id="aef64-145">Cette propriété contient une instance de [l' \_ approbation Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) qui contient le nom, le domaine et l’identificateur de sécurité (SID) du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="aef64-145">This property contains an instance of [Win32\_Trustee](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the owner.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="aef64-146">**SACL**</span><span class="sxs-lookup"><span data-stu-id="aef64-146">**SACL**</span></span>         | <span data-ttu-id="aef64-147">La [liste de Access Control système (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contient un tableau d’instances de [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) qui représentent le type de tentatives d’accès qui génèrent des enregistrements d’audit pour les utilisateurs ou les groupes.</span><span class="sxs-lookup"><span data-stu-id="aef64-147">[System Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent the type of access attempts that generate audit records for users or groups.</span></span> <span data-ttu-id="aef64-148">Pour plus d’informations, consultez [SACL pour un nouvel objet](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span><span class="sxs-lookup"><span data-stu-id="aef64-148">For more information, see [SACL for a New Object](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span></span><br/>                                                                        |



 

## <a name="dacl-and-sacl"></a><span data-ttu-id="aef64-149">DACL et SACL</span><span class="sxs-lookup"><span data-stu-id="aef64-149">DACL and SACL</span></span>

<span data-ttu-id="aef64-150">Les tableaux d’objets [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) de la liste de contrôle d’accès discrétionnaire (DACL) et de la liste de contrôle d’accès système {SACL) créent un lien entre un utilisateur ou un groupe et leurs droits d’accès.</span><span class="sxs-lookup"><span data-stu-id="aef64-150">The arrays of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) objects in the discretionary access control list (DACL) and system access control list {SACL) create a link between a user or group and their access rights.</span></span>

<span data-ttu-id="aef64-151">Lorsqu’une propriété DACL ne contient pas d’entrée de contrôle d’accès (ACE), les droits d’accès ne sont pas accordés et l’accès à l’objet est refusé.</span><span class="sxs-lookup"><span data-stu-id="aef64-151">When a DACL property does not contain an access control entry (ACE), access rights are not granted and access to the object is denied.</span></span>

> [!Note]  
> <span data-ttu-id="aef64-152">Une liste DACL **null** accorde un accès complet à tout le monde, ce qui constitue un risque sérieux pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="aef64-152">A **NULL** DACL gives full access to everyone, which is a serious security risk.</span></span> <span data-ttu-id="aef64-153">Pour plus d’informations, consultez [création d’une liste DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="aef64-153">For more information, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

## <a name="win32_ace-win32_trustee-win32_sid"></a><span data-ttu-id="aef64-154">\_ACE Win32, \_ approuvé Win32, \_ sid Win32</span><span class="sxs-lookup"><span data-stu-id="aef64-154">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>

<span data-ttu-id="aef64-155">Un [**objet \_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) contient une instance de la classe [**Win32 \_ Trusted**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) qui identifie un utilisateur ou un groupe, et une propriété **AccessMask** qui est un masque de masque, qui spécifie les actions qu’un utilisateur ou un groupe peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="aef64-155">A [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object contains an instance of the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class that identifies a user or group, and an **AccessMask** property that is a bitmask, which specifies the actions that a user or group can take.</span></span> <span data-ttu-id="aef64-156">Par exemple, un utilisateur ou un groupe peut se voir accorder le droit de lire un fichier, mais pas d’écrire dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="aef64-156">For example, a user or group might be granted the right to read a file but not write to the file.</span></span> <span data-ttu-id="aef64-157">Un **objet \_ ACE Win32** contient également un ACE qui indique s’il s’agit d’un accès Allow ou Deny.</span><span class="sxs-lookup"><span data-stu-id="aef64-157">A **Win32\_ACE** object also contains an ACE that indicates whether or not it is an allow or a deny access.</span></span>

> [!Note]  
> <span data-ttu-id="aef64-158">L’ordre des entrées de contrôle d’accès [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) dans une liste DACL est important, car l’entrée de contrôle d’accès Allow et Deny est autorisée dans une liste DACL.</span><span class="sxs-lookup"><span data-stu-id="aef64-158">The [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) order in a DACL is important because both allow and deny access control entry (ACE) are permitted in a DACL.</span></span> <span data-ttu-id="aef64-159">Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="aef64-159">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="aef64-160">Chaque compte d’utilisateur ou groupe représenté par [**un \_ tiers de confiance Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) possède un identificateur de sécurité (SID) qui identifie de manière unique un compte, et spécifie les privilèges d’accès du compte.</span><span class="sxs-lookup"><span data-stu-id="aef64-160">Each user account or group represented by a [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) has a security identifier (SID) that uniquely identifies an account, and specifies the access privileges of the account.</span></span> <span data-ttu-id="aef64-161">La façon dont vous spécifiez les données SID dépend du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="aef64-161">How you specify the SID data depends on the operating system.</span></span> <span data-ttu-id="aef64-162">Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="aef64-162">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="aef64-163">Le diagramme suivant montre le contenu d’une instance de l' [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="aef64-163">The following diagram shows the contents of one [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instance.</span></span>

![contenu d’une \- instance ACE Win32](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a><span data-ttu-id="aef64-165">Exemple : vérification de l’accès aux imprimantes</span><span class="sxs-lookup"><span data-stu-id="aef64-165">Example: Checking Who has Access to Printers</span></span>

<span data-ttu-id="aef64-166">L’exemple de code VBScript suivant montre comment utiliser le descripteur de sécurité de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="aef64-166">The following VBScript code example shows how to use the printer security descriptor.</span></span> <span data-ttu-id="aef64-167">Le script appelle la méthode [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) dans la classe [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) pour obtenir le descripteur, puis détermine s’il existe une liste de Access Control discrétionnaire (DACL) présente dans le descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="aef64-167">The script calls the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method in the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class to obtain the descriptor then determines if there is a Discretionary Access Control List (DACL) present in the security descriptor.</span></span> <span data-ttu-id="aef64-168">S’il existe une liste de contrôle d’accès discrétionnaire, le script obtient la liste des entrées de Access Control (ACE) à partir de la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="aef64-168">If there is a DACL, then the script obtains the list of Access Control Entries (ACE) from the DACL.</span></span> <span data-ttu-id="aef64-169">Chaque ACE est représenté par une instance de [**l' \_ entrée**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)du contrôle d’accès Win32.</span><span class="sxs-lookup"><span data-stu-id="aef64-169">Each ACE is represented by an instance of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span></span> <span data-ttu-id="aef64-170">Le script vérifie chaque ACE pour obtenir le nom de l’utilisateur et détermine si l’utilisateur a accès à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="aef64-170">The script checks every ACE to get the name of the user and determine whether the user has access to the printer.</span></span> <span data-ttu-id="aef64-171">L’utilisateur est représenté par une instance de [**\_ confiance Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) incorporée dans l' **instance \_ ACE Win32** .</span><span class="sxs-lookup"><span data-stu-id="aef64-171">The user is represented in by an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded in the **Win32\_ACE** instance.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a><span data-ttu-id="aef64-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aef64-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aef64-173">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="aef64-173">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> <dt>

[<span data-ttu-id="aef64-174">Classe d’assistance du descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="aef64-174">Security Descriptor Helper Class</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[<span data-ttu-id="aef64-175">Meilleures pratiques de sécurité</span><span class="sxs-lookup"><span data-stu-id="aef64-175">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[<span data-ttu-id="aef64-176">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="aef64-176">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="aef64-177">Contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="aef64-177">Access Control</span></span>](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[<span data-ttu-id="aef64-178">Accès aux espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="aef64-178">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

