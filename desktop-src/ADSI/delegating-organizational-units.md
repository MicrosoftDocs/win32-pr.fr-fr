---
title: Délégation d’unités d’organisation
description: La société Fabrikam engage deux administrateurs, Mike et Paul, à gérer les unités d’organisation est et ouest, respectivement.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510388"
---
# <a name="delegating-organizational-units"></a><span data-ttu-id="078ea-103">Délégation d’unités d’organisation</span><span class="sxs-lookup"><span data-stu-id="078ea-103">Delegating Organizational Units</span></span>

<span data-ttu-id="078ea-104">La société Fabrikam engage deux administrateurs, Mike et Paul, à gérer les unités d’organisation est et ouest, respectivement.</span><span class="sxs-lookup"><span data-stu-id="078ea-104">The Fabrikam company hires two administrators, Mike and Paul, to manage the East and West organizational units, respectively.</span></span> <span data-ttu-id="078ea-105">Jean délègue ses responsabilités administratives pour qu’il puisse créer et supprimer des utilisateurs dans leurs unités d’organisation respectives.</span><span class="sxs-lookup"><span data-stu-id="078ea-105">Joe delegates his administrative responsibilities to them so that they can create and delete users in their respective organizational units.</span></span>

<span data-ttu-id="078ea-106">Avant de voir comment configurer ces unités d’organisation sous Mike et Paul, vous devez comprendre comment configurer l’accès aux objets dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="078ea-106">Before seeing how to set up these organizational units under Mike and Paul, you must understand how to set up access to objects in Active Directory.</span></span> <span data-ttu-id="078ea-107">Chaque objet dans Active Directory possède un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="078ea-107">Each object in Active Directory has a security descriptor.</span></span> <span data-ttu-id="078ea-108">Avec le descripteur de sécurité, vous pouvez modifier les autorisations sur l’objet, propager les autorisations, activer l’audit, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="078ea-108">With the security descriptor, you can modify permissions on the object, propagate permissions, enable auditing, and so on.</span></span> <span data-ttu-id="078ea-109">Le descripteur de sécurité a lui-même deux listes de contrôle d’accès (ACL) : une liste ACL discrétionnaire (DACL) et une ACL système (SACL).</span><span class="sxs-lookup"><span data-stu-id="078ea-109">The security descriptor itself has two access control lists (ACLs): a discretionary ACL (DACL) and a system ACL (SACL).</span></span> <span data-ttu-id="078ea-110">Chaque liste ACL peut contenir des entrées de contrôle d’accès (ACE).</span><span class="sxs-lookup"><span data-stu-id="078ea-110">Each ACL can contain access control entries (ACEs).</span></span> <span data-ttu-id="078ea-111">Avec une entrée du contrôle d’accès, vous pouvez définir l’accès autorisé ou refusé sur un objet.</span><span class="sxs-lookup"><span data-stu-id="078ea-111">With an ACE, you can set allowed or denied access on an object.</span></span> <span data-ttu-id="078ea-112">En outre, vous pouvez spécifier des actions spécifiques à autoriser ou refuser.</span><span class="sxs-lookup"><span data-stu-id="078ea-112">In addition, you can specify specific actions to allow or deny.</span></span> <span data-ttu-id="078ea-113">Voici quelques exemples d’actions : créer un enfant, supprimer un enfant, lire la propriété et écrire la propriété.</span><span class="sxs-lookup"><span data-stu-id="078ea-113">Examples of actions include Create Child, Delete Child, Read Property, and Write Property.</span></span> <span data-ttu-id="078ea-114">Ces droits sont spécifiés avec [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="078ea-114">These rights are specified with the [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span></span>

<span data-ttu-id="078ea-115">Ensuite, vous pouvez spécifier les classes ou les attributs auxquels cette entrée du contrôle d’accès (ACE) est associée.</span><span class="sxs-lookup"><span data-stu-id="078ea-115">Next, you may specify the classes or attributes to which this ACE is associated.</span></span> <span data-ttu-id="078ea-116">Dans l’exemple Fabrikam qui suit, Joe choisit la classe utilisateur afin que chaque administrateur puisse ajouter des utilisateurs au système.</span><span class="sxs-lookup"><span data-stu-id="078ea-116">In the Fabrikam example that follows, Joe picks the user class so that each administrator can add users to the system.</span></span> <span data-ttu-id="078ea-117">Ensuite, vous devez répondre à la question suivante : « qui sera le bénéficiaire de cette entrée de contrôle d’accès ? »</span><span class="sxs-lookup"><span data-stu-id="078ea-117">Next, you must answer the question: "Who will be the beneficiary of this ACE?"</span></span> <span data-ttu-id="078ea-118">Joe spécifie Mike.</span><span class="sxs-lookup"><span data-stu-id="078ea-118">Joe will specify Mike.</span></span>

<span data-ttu-id="078ea-119">Enfin, vous pouvez définir le comportement d’héritage de l’entrée du contrôle d’accès. par exemple, les entrées de contrôle d’accès peuvent être spécifiées pour se propager dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="078ea-119">Finally, you can set the ACE inheritance behavior—for example, ACEs can be specified to propagate down the hierarchy.</span></span> <span data-ttu-id="078ea-120">En résumé, l’exemple précédent donne à Mike la possibilité de créer et de supprimer des objets utilisateur sous l’unité d’organisation East Sales.</span><span class="sxs-lookup"><span data-stu-id="078ea-120">In summary, the previous example will result in Mike being able to create and delete user objects under the East Sales organizational unit.</span></span>

<span data-ttu-id="078ea-121">Joe utilise l’exemple de code suivant pour configurer les ACE et les listes de contrôle d’accès sur l’unité d’organisation East.</span><span class="sxs-lookup"><span data-stu-id="078ea-121">Joe uses the following code example to set up the ACEs and ACLs on the East organizational unit.</span></span>


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



<span data-ttu-id="078ea-122">L’illustration suivante montre le menu Active Directory **créer une nouvelle vue** après l’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="078ea-122">The following figure shows the Active Directory **Create New View** menu after the code runs.</span></span> <span data-ttu-id="078ea-123">Quand Jean, l’administrateur ouvre une session, il voit plusieurs classes qu’il peut créer.</span><span class="sxs-lookup"><span data-stu-id="078ea-123">When Joe, the administrator, logs on, he sees several classes that he can create.</span></span> <span data-ttu-id="078ea-124">Toutefois, lorsque Mike ouvre une session, il peut uniquement créer des objets utilisateur.</span><span class="sxs-lookup"><span data-stu-id="078ea-124">However, when Mike logs on, he is able only to create user objects.</span></span>

![menu créer une option de vue](images/adadsi5.png)

<span data-ttu-id="078ea-126">Pour plus d’informations, consultez [modèle de sécurité ADSI](adsi-security-model.md).</span><span class="sxs-lookup"><span data-stu-id="078ea-126">For more information, see [ADSI Security Model](adsi-security-model.md).</span></span>

 

 




