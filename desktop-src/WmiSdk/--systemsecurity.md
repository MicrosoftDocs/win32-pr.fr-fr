---
description: Contient des méthodes qui vous permettent d’accéder aux paramètres de sécurité d’un espace de noms et de les modifier.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: Classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115967"
---
# <a name="__systemsecurity-class"></a><span data-ttu-id="90d4f-103">\_\_SystemSecurity, classe</span><span class="sxs-lookup"><span data-stu-id="90d4f-103">\_\_SystemSecurity class</span></span>

<span data-ttu-id="90d4f-104">La classe système **\_ \_ SystemSecurity** contient des méthodes qui vous permettent d’accéder aux paramètres de sécurité d’un espace de noms et de les modifier.</span><span class="sxs-lookup"><span data-stu-id="90d4f-104">The **\_\_SystemSecurity** system class contains methods that let you access and modify the security settings for a namespace.</span></span> <span data-ttu-id="90d4f-105">La classe **\_ \_ SystemSecurity** est une classe singleton dans chaque espace de noms.</span><span class="sxs-lookup"><span data-stu-id="90d4f-105">The **\_\_SystemSecurity** class is a singleton class in each namespace.</span></span>

> [!Note]  
> <span data-ttu-id="90d4f-106">Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="90d4f-106">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

 

<span data-ttu-id="90d4f-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="90d4f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="90d4f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="90d4f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d4f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90d4f-109">Syntax</span></span>

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a><span data-ttu-id="90d4f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="90d4f-110">Members</span></span>

<span data-ttu-id="90d4f-111">La classe **\_ \_ SystemSecurity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="90d4f-111">The **\_\_SystemSecurity** class has these types of members:</span></span>

-   [<span data-ttu-id="90d4f-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="90d4f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="90d4f-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="90d4f-113">Methods</span></span>

<span data-ttu-id="90d4f-114">La classe **\_ \_ SystemSecurity** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="90d4f-114">The **\_\_SystemSecurity** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="90d4f-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="90d4f-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="90d4f-116">Description</span><span class="sxs-lookup"><span data-stu-id="90d4f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="90d4f-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="90d4f-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="90d4f-118">Obtient une liste des utilisateurs autorisés à accéder à distance.</span><span class="sxs-lookup"><span data-stu-id="90d4f-118">Gets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90d4f-119">Cette méthode ne fonctionne pas sur les versions prises en charge de Windows.</span><span class="sxs-lookup"><span data-stu-id="90d4f-119">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="90d4f-120">Utilisez <a href="--systemsecurity-getsd.md"><strong>à</strong></a> la place.</span><span class="sxs-lookup"><span data-stu-id="90d4f-120">Use <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="90d4f-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span><span class="sxs-lookup"><span data-stu-id="90d4f-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="90d4f-122">Retourne un masque avec chaque bit qui correspond à un droit d’accès.</span><span class="sxs-lookup"><span data-stu-id="90d4f-122">Returns a mask with each bit that corresponds to an access right.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="90d4f-123"><a href="--systemsecurity-getsd.md"><strong>Getsd a</strong></a></span><span class="sxs-lookup"><span data-stu-id="90d4f-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="90d4f-124">Obtient le <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> de l’espace de noms auquel l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="90d4f-124">Gets the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="90d4f-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="90d4f-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="90d4f-126">Obtient le descripteur de sécurité qui contrôle l’accès à l’espace de noms WMI associé à l’instance de <strong>__SystemSecurity</strong>.</span><span class="sxs-lookup"><span data-stu-id="90d4f-126">Gets the security descriptor that controls access to the WMI namespace associated with the instance of <strong>__SystemSecurity</strong>.</span></span> <span data-ttu-id="90d4f-127">Le descripteur de sécurité est retourné sous la forme d’une instance de<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="90d4f-127">The security descriptor is returned as an instance of<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="90d4f-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="90d4f-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="90d4f-129">Définit une liste d’utilisateurs autorisés à accéder à distance.</span><span class="sxs-lookup"><span data-stu-id="90d4f-129">Sets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="90d4f-130">Cette méthode ne fonctionne pas sur les versions prises en charge de Windows.</span><span class="sxs-lookup"><span data-stu-id="90d4f-130">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="90d4f-131">Utilisez à la place <a href="--systemsecurity-setsd.md"><strong>sets</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="90d4f-131">Use <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="90d4f-132"><a href="--systemsecurity-setsd.md"><strong>Setsd a</strong></a></span><span class="sxs-lookup"><span data-stu-id="90d4f-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="90d4f-133">Définit le descripteur de sécurité pour l’espace de noms auquel l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="90d4f-133">Sets the security descriptor for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="90d4f-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="90d4f-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="90d4f-135">Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="90d4f-135">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="90d4f-136">Le descripteur de sécurité est représenté par une instance de <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="90d4f-136">The security descriptor is represented by an instance of <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="90d4f-137">Notes</span><span class="sxs-lookup"><span data-stu-id="90d4f-137">Remarks</span></span>

<span data-ttu-id="90d4f-138">Vous pouvez exiger que les applications et les scripts clients utilisent une connexion chiffrée pour l’authentification en ajoutant le qualificateur **RequiresEncryption** au fichier. MOF qui crée l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="90d4f-138">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="90d4f-139">Vous pouvez également modifier un espace de noms existant en ajoutant cet attribut et recompiler le fichier. mof.</span><span class="sxs-lookup"><span data-stu-id="90d4f-139">You can also modify an existing namespace by adding this attribute and compile the .mof file again.</span></span> <span data-ttu-id="90d4f-140">Pour plus d’informations sur l’utilisation de **RequiresEncryption**, consultez la page [exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="90d4f-140">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90d4f-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90d4f-141">Requirements</span></span>



| <span data-ttu-id="90d4f-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90d4f-142">Requirement</span></span> | <span data-ttu-id="90d4f-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="90d4f-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="90d4f-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90d4f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="90d4f-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90d4f-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="90d4f-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90d4f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="90d4f-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90d4f-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="90d4f-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="90d4f-148">Namespace</span></span><br/>                | <span data-ttu-id="90d4f-149">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="90d4f-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="90d4f-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90d4f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90d4f-151">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="90d4f-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="90d4f-152">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="90d4f-152">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="90d4f-153">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="90d4f-153">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="90d4f-154">Sécurisation des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="90d4f-154">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="90d4f-155">Établissement de l’héritage de la sécurité des espaces de noms</span><span class="sxs-lookup"><span data-stu-id="90d4f-155">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="90d4f-156">Listes de Access Control (ACL)</span><span class="sxs-lookup"><span data-stu-id="90d4f-156">Access Control Lists (ACLs)</span></span>](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[<span data-ttu-id="90d4f-157">**Descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="90d4f-157">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

