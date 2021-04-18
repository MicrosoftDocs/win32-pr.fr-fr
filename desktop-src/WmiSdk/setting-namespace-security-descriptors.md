---
description: Les applications C++ et les scripts s’exécutant sous un compte d’administrateur complet peuvent modifier un descripteur de sécurité d’espace de noms.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Définition des descripteurs de sécurité des espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519555"
---
# <a name="setting-namespace-security-descriptors"></a><span data-ttu-id="e926c-103">Définition des descripteurs de sécurité des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="e926c-103">Setting Namespace Security Descriptors</span></span>

<span data-ttu-id="e926c-104">Les applications C++ et les scripts s’exécutant sous un compte d’administrateur complet peuvent modifier un descripteur de sécurité d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e926c-104">Both C++ applications and scripts running under a full administrator account can change a namespace security descriptor.</span></span>

## <a name="namespace-security-descriptors"></a><span data-ttu-id="e926c-105">Descripteurs de sécurité des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="e926c-105">Namespace Security Descriptors</span></span>

<span data-ttu-id="e926c-106">Chaque espace de noms WMI possède un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)qui permet à chaque espace de noms d’avoir des paramètres de sécurité uniques qui déterminent qui a accès aux données et méthodes de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e926c-106">Each WMI namespace has a [*security descriptor*](/windows/desktop/SecGloss/s-gly), which allows each namespace to have unique security settings that determine who has access to the namespace data and methods.</span></span> <span data-ttu-id="e926c-107">Pour plus d’informations sur la sécurité d’accès WMI, consultez [accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e926c-107">For more information about WMI access security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span> <span data-ttu-id="e926c-108">[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md) décrit les paramètres de sécurité par défaut pour les espaces de noms WMI et l’audit de sécurité dans WMI.</span><span class="sxs-lookup"><span data-stu-id="e926c-108">[Access to WMI Namespaces](access-to-wmi-namespaces.md) describes the default security settings for WMI namespaces and security auditing in WMI.</span></span>

<span data-ttu-id="e926c-109">Vous pouvez définir des autorisations de compte pour chaque espace de noms WMI dans le référentiel WMI (CIM) de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="e926c-109">You can set account permissions for each WMI namespace in the WMI (CIM) repository in the following ways:</span></span>

-   <span data-ttu-id="e926c-110">Lorsque l’espace de noms est créé dans le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="e926c-110">When the namespace is created in the MOF file.</span></span> <span data-ttu-id="e926c-111">Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms lors de la création de l’espace de noms](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="e926c-111">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>
-   <span data-ttu-id="e926c-112">Manuellement, à l’aide du contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="e926c-112">Manually, using the WMI Control.</span></span> <span data-ttu-id="e926c-113">Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="e926c-113">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>
-   <span data-ttu-id="e926c-114">Par programmation, en appelant les méthodes de la classe [**\_ \_ SystemSecurity**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="e926c-114">Programmatically, by calling the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span>

<span data-ttu-id="e926c-115">Les méthodes suivantes de l’objet [**\_ \_ SystemSecurity**](--systemsecurity.md) associé à chaque espace de noms vous permettent de lire ou de modifier la sécurité sur un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="e926c-115">The following methods of the [**\_\_SystemSecurity**](--systemsecurity.md) object associated with each namespace allow you to read or change security on a namespace.</span></span>

<dl> <dt>

<span data-ttu-id="e926c-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span><span class="sxs-lookup"><span data-stu-id="e926c-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span></span>
</dt> <dd>

<span data-ttu-id="e926c-117">Définit le paramètre *Rights* en tant que bitmap avec chaque bit correspondant à un droit d’accès.</span><span class="sxs-lookup"><span data-stu-id="e926c-117">Sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span>

</dd> <dt>

<span data-ttu-id="e926c-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**Getsd a**](--systemsecurity-getsd.md)</span><span class="sxs-lookup"><span data-stu-id="e926c-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="e926c-119">Obtient le descripteur de sécurité pour l’espace de noms auquel l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="e926c-119">Gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="e926c-120">Cette méthode retourne un descripteur de sécurité au format de tableau d’octets binaire.</span><span class="sxs-lookup"><span data-stu-id="e926c-120">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="e926c-121">Si vous écrivez un script, utilisez la méthode [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="e926c-121">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e926c-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**Setsd a**](--systemsecurity-setsd.md)</span><span class="sxs-lookup"><span data-stu-id="e926c-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="e926c-123">Définit le descripteur de sécurité (SD) pour l’espace de noms auquel un utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="e926c-123">Sets the security descriptor (SD) for the namespace to which a user is connected.</span></span> <span data-ttu-id="e926c-124">Cette méthode requiert un descripteur de sécurité au format de tableau d’octets binaire.</span><span class="sxs-lookup"><span data-stu-id="e926c-124">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="e926c-125">Si vous écrivez un script, utilisez la méthode [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="e926c-125">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e926c-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span><span class="sxs-lookup"><span data-stu-id="e926c-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span></span>
</dt> <dd>

<span data-ttu-id="e926c-127">Obtient le descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI associé à l’instance de [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="e926c-127">Gets the security descriptor that controls access to the WMI namespace associated with the instance of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="e926c-128">Le descripteur de sécurité est retourné en tant qu’instance de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="e926c-128">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e926c-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span><span class="sxs-lookup"><span data-stu-id="e926c-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span></span>
</dt> <dd>

<span data-ttu-id="e926c-130">Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="e926c-130">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="e926c-131">Le descripteur de sécurité est représenté par une instance de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="e926c-131">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e926c-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="e926c-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="e926c-133">Obtient les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès via les descripteurs de sécurité Windows n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="e926c-133">Gets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e926c-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="e926c-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="e926c-135">Définit les droits d’accès à distance pour une liste d’utilisateurs individuels sur des ordinateurs exécutant des versions obsolètes de Windows, où le contrôle d’accès via les descripteurs de sécurité Windows n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="e926c-135">Sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> </dl>

<span data-ttu-id="e926c-136">Si vous écrivez des scripts, utilisez [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) et [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="e926c-136">If you are writing scripts, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) and [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span></span> <span data-ttu-id="e926c-137">Vous pouvez utiliser les méthodes de la classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) pour modifier les descripteurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e926c-137">You can use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to alter the security descriptors.</span></span>

<span data-ttu-id="e926c-138">Si vous programmez en C++, vous pouvez manipuler le descripteur de sécurité binaire à l’aide du [langage SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)et des méthodes de conversion [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) et [**convertstringsecuritydescriptortosecuritydescriptor a**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="e926c-138">If you are programming in C++, you can manipulate the binary security descriptor using [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="e926c-139">Sachez que, à partir de Windows Vista, le contrôle de compte d’utilisateur (UAC, [User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) ) affecte l’accès aux données WMI et ce qui peut être configuré avec le [*contrôle WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="e926c-139">Be aware that, starting with Windows Vista, [User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="e926c-140">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="e926c-140">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e926c-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e926c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e926c-142">Sécurisation des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="e926c-142">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="e926c-143">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="e926c-143">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="e926c-144">Accès aux espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="e926c-144">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="e926c-145">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="e926c-145">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
