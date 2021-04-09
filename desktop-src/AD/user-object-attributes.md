---
title: Attributs d’objet utilisateur
description: Un objet utilisateur a plusieurs attributs. Cette section décrit les attributs clés utilisés par Windows, les outils d’administration et le carnet d’adresses Windows (WAB). Elle ne décrit pas tous les attributs ; de nombreux attributs ne sont pas utilisés pour l’objet utilisateur.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- Attributs de l’objet utilisateur Active Directory
- Utilisateurs AD, attributs d’objet utilisateur
- Objets AD, utilisateur, attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c90d8d5f28c41971f5f6910cfb8bef1fafd6f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940789"
---
# <a name="user-object-attributes"></a><span data-ttu-id="e54d4-108">Attributs d’objet utilisateur</span><span class="sxs-lookup"><span data-stu-id="e54d4-108">User Object Attributes</span></span>

<span data-ttu-id="e54d4-109">Un objet utilisateur a plusieurs attributs.</span><span class="sxs-lookup"><span data-stu-id="e54d4-109">A user object has multiple attributes.</span></span> <span data-ttu-id="e54d4-110">Cette section décrit les attributs clés utilisés par Windows, les outils d’administration et le carnet d’adresses Windows (WAB).</span><span class="sxs-lookup"><span data-stu-id="e54d4-110">This section documents key attributes used by Windows, administrative tools, and the Windows Address Book (WAB).</span></span> <span data-ttu-id="e54d4-111">Elle ne décrit pas tous les attributs ; de nombreux attributs ne sont pas utilisés pour l’objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e54d4-111">It does not describe all attributes; many attributes are not used for the user object.</span></span>

<span data-ttu-id="e54d4-112">Certains attributs sont stockés dans l’annuaire, tels que [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), etc., et répliqués sur tous les contrôleurs de domaine au sein d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="e54d4-112">Some attributes are stored in the directory, such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), and so on, and replicated to all domain controllers within a domain.</span></span> <span data-ttu-id="e54d4-113">Un sous-ensemble de ces attributs est également répliqué dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="e54d4-113">A subset of these attributes is also replicated to the global catalog.</span></span>

<span data-ttu-id="e54d4-114">Les attributs non répliqués sont stockés sur chaque contrôleur de domaine, mais ne sont pas répliqués ailleurs, tels que [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), etc.</span><span class="sxs-lookup"><span data-stu-id="e54d4-114">Non-replicated attributes are stored on each domain controller, but are not replicated elsewhere, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), and so on.</span></span> <span data-ttu-id="e54d4-115">Les attributs non répliqués sont des attributs qui se rapportent à un contrôleur de domaine particulier.</span><span class="sxs-lookup"><span data-stu-id="e54d4-115">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="e54d4-116">Par exemple, **lastLogon** est la dernière date et heure auxquelles l’ouverture de session réseau de l’utilisateur a été validée par le contrôleur de domaine particulier qui retourne la propriété.</span><span class="sxs-lookup"><span data-stu-id="e54d4-116">For example, **lastLogon** is the last date and time that the user network logon was validated by the particular domain controller that is returning the property.</span></span>

<span data-ttu-id="e54d4-117">Un objet utilisateur a également des attributs construits qui ne sont pas stockés dans l’annuaire, mais qui sont calculés par le contrôleur de domaine, tel que [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), etc.</span><span class="sxs-lookup"><span data-stu-id="e54d4-117">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), and so on.</span></span>

<span data-ttu-id="e54d4-118">Les attributs des objets utilisateur sont classés comme suit :</span><span class="sxs-lookup"><span data-stu-id="e54d4-118">Attributes for user objects are classified as:</span></span>

<dl> <dt>

<span data-ttu-id="e54d4-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Attributs d’objet de base</span><span class="sxs-lookup"><span data-stu-id="e54d4-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Base Object Attributes</span></span>
</dt> <dd>

<span data-ttu-id="e54d4-120">Cette catégorie comprend les attributs requis pour tous les objets d’annuaire, tels que [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), etc.</span><span class="sxs-lookup"><span data-stu-id="e54d4-120">This category includes attributes required for all directory objects, such as [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and so on.</span></span>

</dd> <dt>

<span data-ttu-id="e54d4-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Nommer des attributs</span><span class="sxs-lookup"><span data-stu-id="e54d4-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Naming Attributes</span></span>
</dt> <dd>

<span data-ttu-id="e54d4-122">Cette catégorie comprend les attributs utilisés pour faire référence à l’objet ou l’identifier, par exemple [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), etc.</span><span class="sxs-lookup"><span data-stu-id="e54d4-122">This category includes attributes used to refer to or identify the object, such as [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), and so on.</span></span> <span data-ttu-id="e54d4-123">Pour plus d’informations sur les attributs d’attribution de noms pour les objets utilisateur, consultez [User Naming Attributes](naming-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e54d4-123">For more information about naming attributes for user objects, see [User Naming Attributes](naming-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="e54d4-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Attributs de sécurité</span><span class="sxs-lookup"><span data-stu-id="e54d4-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Security Attributes</span></span>
</dt> <dd>

<span data-ttu-id="e54d4-125">Cette catégorie comprend des attributs pour l’ouverture de session et le contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="e54d4-125">This category includes attributes for logon and access control.</span></span> <span data-ttu-id="e54d4-126">Pour plus d’informations sur les attributs de sécurité pour les objets utilisateur, consultez [attributs de sécurité](security-properties.md)de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e54d4-126">For more information about security attributes for user objects, see [User Security Attributes](security-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="e54d4-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Attributs du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="e54d4-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Address Book Attributes</span></span>
</dt> <dd>

<span data-ttu-id="e54d4-128">Cette catégorie comprend les attributs des données de messagerie et utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e54d4-128">This category includes attributes for email and user data.</span></span> <span data-ttu-id="e54d4-129">Pour plus d’informations sur les attributs de carnet d’adresses pour les objets utilisateur, consultez [attributs de carnet d’adresses utilisateur](address-book-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e54d4-129">For more information about address book attributes for user objects, see [User Address Book Attributes](address-book-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="e54d4-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Attributs spécifiques à l’application</span><span class="sxs-lookup"><span data-stu-id="e54d4-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Application Specific Attributes</span></span>
</dt> <dd>

<span data-ttu-id="e54d4-131">Cette catégorie comprend des données de configuration spécifiques à l’utilisateur pour des applications spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e54d4-131">This category includes user-specific configuration data for specific applications.</span></span>

</dd> </dl>

<span data-ttu-id="e54d4-132">Pour plus d’informations sur la lecture et la modification des attributs d’un objet utilisateur, consultez [lecture et écriture des attributs d’objets dans Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="e54d4-132">For more information about reading and modifying attributes for a user object, see [Reading and Writing Attributes of Objects in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="e54d4-133">Pour plus d’informations sur la classe User, y compris la liste complète des attributs [**mayContain**](/windows/desktop/ADSchema/a-maycontain) et [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) de la classe, consultez [**User**](/windows/desktop/ADSchema/c-user).</span><span class="sxs-lookup"><span data-stu-id="e54d4-133">For more information about the User class, including a complete list of the [**mayContain**](/windows/desktop/ADSchema/a-maycontain) and [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) attributes of the class, see [**User**](/windows/desktop/ADSchema/c-user).</span></span>

## <a name="setting-passwords"></a><span data-ttu-id="e54d4-134">Définition des mots de passe</span><span class="sxs-lookup"><span data-stu-id="e54d4-134">Setting Passwords</span></span>

<span data-ttu-id="e54d4-135">Le mot de passe d’un utilisateur ne peut pas être modifié directement, car cela implique l’envoi d’un mot de passe non chiffré sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="e54d4-135">The password for a user cannot be modified directly because this would involve sending an unencrypted password over the network.</span></span> <span data-ttu-id="e54d4-136">Pour définir le mot de passe d’un utilisateur, il est nécessaire d’utiliser la méthode [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) ou [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="e54d4-136">To set the password for a user, it is necessary to use the [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) or [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="e54d4-137">La méthode **IADsUser. ChangePassword** est utilisée lorsque l’application permet à l’utilisateur de modifier son propre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e54d4-137">The **IADsUser.ChangePassword** method is used when the application is allowing the user to change their own password.</span></span> <span data-ttu-id="e54d4-138">La méthode **IADsUser. SetPassword** est utilisée lorsque l’application permet à un administrateur de réinitialiser un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e54d4-138">The **IADsUser.SetPassword** method is used when the application enables an administrator to reset a password.</span></span>

 

 