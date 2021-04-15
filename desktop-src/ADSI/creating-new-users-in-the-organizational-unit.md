---
title: Création de nouveaux utilisateurs dans l’unité d’organisation
description: Terry Adams a été embauché dans l’organisation Fabrikam Sales. Son rapport direct est Patrick Hines.
ms.assetid: bc31ed04-e505-4d64-9fa3-d06af7351db0
ms.tgt_platform: multiple
keywords:
- Création d’utilisateurs dans l’ADSI de l’unité d’organisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45f9dc91f1c36493a4ae8e1c9bb1a69268c9987
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461990"
---
# <a name="creating-new-users-in-the-organizational-unit"></a><span data-ttu-id="8f9c0-105">Création de nouveaux utilisateurs dans l’unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="8f9c0-105">Creating New Users in the Organizational Unit</span></span>

<span data-ttu-id="8f9c0-106">Terry Adams a été embauché dans l’organisation Fabrikam Sales.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-106">Terry Adams was hired into the Fabrikam Sales organization.</span></span> <span data-ttu-id="8f9c0-107">Son rapport direct est Patrick Hines.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-107">His direct report is Patrick Hines.</span></span>

<span data-ttu-id="8f9c0-108">Comme indiqué dans l’exemple de code suivant, Joe Durand, administrateur d’entreprise, crée un compte pour lui.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-108">As shown in the following code example, Joe Andreshak, the enterprise administrator, will create a new account for him.</span></span>


```VB
Dim salesOU as IADsContainer
Set salesOU = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set usr = salesOU.Create("user", "CN=Terry Adams")
usr.Put "sAMAccountName", "terryadams"
usr.Put "userPrincipalName", "terryadams@fabrikam.com" 
usr.Put "title" "Marketing Manager"
usr.SetInfo

usr.SetPassword "seahorse"
usr.AccountDisabled = False
usr.SetInfo
```



<span data-ttu-id="8f9c0-109">Lorsque vous créez un utilisateur, vous devez spécifier un **sAMAccountName**.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-109">When creating a new user, you must specify a **sAMAccountName**.</span></span> <span data-ttu-id="8f9c0-110">Il s’agit d’un attribut obligatoire pour la classe utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-110">This is a mandatory attribute for the user class.</span></span> <span data-ttu-id="8f9c0-111">Avant de pouvoir créer une instance d’un objet, vous devez définir tous les attributs obligatoires.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-111">Before an instance of an object can be created, all mandatory attributes must be set.</span></span> <span data-ttu-id="8f9c0-112">Le **sAMAccountName** est généré automatiquement s’il n’est pas spécifié pour un nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-112">The **sAMAccountName** will automatically be generated if one is not specified for a new user.</span></span>

<span data-ttu-id="8f9c0-113">Lorsque vous créez un utilisateur, tous les attributs requis doivent être définis dans le cache local avant l’appel de la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="8f9c0-113">When creating a new user, all of the required attributes must be set in the local cache before the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

<span data-ttu-id="8f9c0-114">Joe, en tant qu’administrateur, peut attribuer le mot de passe de Terry à l’aide de la méthode [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="8f9c0-114">Joe, as an administrator, can assign Terry's password using the [**IADsUser.SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="8f9c0-115">La méthode **IADsUser. SetPassword** ne fonctionnera pas tant que la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-115">The **IADsUser.SetPassword** method will not work until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method has been called.</span></span>

<span data-ttu-id="8f9c0-116">Joe active ensuite le compte d’utilisateur en affectant à la propriété [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-116">Then, Joe enables the user account by setting the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property to **FALSE**.</span></span>

<span data-ttu-id="8f9c0-117">L’exemple de code suivant montre comment définir Thierry comme responsable de Patrick.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-117">The following code example shows how to set Terry as Patrick's manager.</span></span>


```VB
Set usr = GetObject("LDAP://CN=patrickhines,OU=Sales,DC=Fabrikam,DC=COM")
usr.Put "manager", "CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM"
usr.SetInfo
```



<span data-ttu-id="8f9c0-118">Vous vous demandez peut-être ce qui se passe si Thierry change de nom, passe à une autre organisation ou quitte l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-118">You may wonder what happens if Terry changes his name, moves to a different organization, or leaves the company.</span></span> <span data-ttu-id="8f9c0-119">Qui gère ce lien de rapport direct du gestionnaire ?</span><span class="sxs-lookup"><span data-stu-id="8f9c0-119">Who maintains this manager-direct report link?</span></span> <span data-ttu-id="8f9c0-120">Pour plus d’informations et pour obtenir la solution à ce problème, consultez [réorganisation](reorganization.md).</span><span class="sxs-lookup"><span data-stu-id="8f9c0-120">For more information, and the solution to this problem, see [Reorganization](reorganization.md).</span></span> <span data-ttu-id="8f9c0-121">Étant donné que le schéma de Active Directory est extensible, vous pouvez modéliser vos objets de manière à inclure des relations de style gestionnaire-directe similaires.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-121">Because the Active Directory schema is extensible, you can model your objects to include similar manager-direct report style relationships.</span></span>

<span data-ttu-id="8f9c0-122">Avant de passer à la tâche suivante, consultez un exemple de code qui montre comment Joe affichera les collaborateurs directs de Terry.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-122">Before going on to the next task, look at a code example that shows how Joe would view Terry's direct reports.</span></span>


```VB
Set usr = GetObject("LDAP://CN=Terry Adams,OU=Sales,DC=Fabrikam,DC=COM")
reports = usr.GetEx ("directReports")

For each directReport in reports
    Debug.Print directReport
Next
```



<span data-ttu-id="8f9c0-123">Dans cet exemple de code, Patrick s’affiche comme le rapport direct de Terry, même si l’attribut **DirectReports** n’a jamais été modifié.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-123">In this code example, Patrick will display as Terry's direct report, even though the **directReports** attribute was never modified.</span></span> <span data-ttu-id="8f9c0-124">Active Directory le fait automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-124">Active Directory does this automatically.</span></span>

<span data-ttu-id="8f9c0-125">Dans le monde de l’annuaire, un attribut peut avoir une ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-125">In the directory world, an attribute can have single or multiple values.</span></span> <span data-ttu-id="8f9c0-126">Comme **DirectReports** a plusieurs valeurs, vous pouvez accéder à ces informations en examinant le schéma, il est plus facile d’utiliser la méthode [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) , qui retourne un tableau de valeurs, qu’une seule ou plusieurs valeurs soient retournées.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-126">Because **directReports** has multiple values, you can get this information by looking at the schema, it is easier to use the [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, which returns an array of values regardless of whether single or multiple values are returned.</span></span>

<span data-ttu-id="8f9c0-127">Le composant logiciel enfichable utilisateurs et ordinateurs Active Directory vous permet d’afficher les rapports directs et les relations du gestionnaire sur la page de propriétés de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f9c0-127">The Active Directory Users and Computers snap-in lets you view direct reports and manager relationships on the user's property page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f9c0-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f9c0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f9c0-129">Ajout d’utilisateurs à un groupe</span><span class="sxs-lookup"><span data-stu-id="8f9c0-129">Adding Users to a Group</span></span>](adding-users-to-a-group.md)
</dt> </dl>

 

 




