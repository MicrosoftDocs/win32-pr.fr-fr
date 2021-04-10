---
title: Création d’un nouveau groupe
description: Joe worden, administrateur d’entreprise, doit créer un nouveau groupe.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941371"
---
# <a name="creating-a-new-group"></a><span data-ttu-id="e7e07-103">Création d’un nouveau groupe</span><span class="sxs-lookup"><span data-stu-id="e7e07-103">Creating a New Group</span></span>

<span data-ttu-id="e7e07-104">Joe worden, administrateur d’entreprise, doit créer un nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="e7e07-104">Joe Worden, the enterprise administrator, must create a new group.</span></span> <span data-ttu-id="e7e07-105">Il souhaite sécuriser certaines ressources, telles que les objets de fichier, de Active Directory ou d’autres objets, en fonction de l’appartenance de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="e7e07-105">He would like to secure some resources, such as file, Active Directory objects, or other objects, based on the membership of this group.</span></span> <span data-ttu-id="e7e07-106">L’exemple de code suivant montre comment créer un nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="e7e07-106">The following code example shows how to create a new group.</span></span>


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



<span data-ttu-id="e7e07-107">Ce groupe, gestion, est créé dans l’unité d’organisation Sales.</span><span class="sxs-lookup"><span data-stu-id="e7e07-107">This group, Management, will be created in the Sales organizational unit.</span></span> <span data-ttu-id="e7e07-108">En premier lieu, Joe doit créer un objet ADSI pour l’unité d’organisation Sales.</span><span class="sxs-lookup"><span data-stu-id="e7e07-108">First, Joe must create an ADSI object for the Sales organizational unit.</span></span> <span data-ttu-id="e7e07-109">Ensuite, il doit définir l’attribut [**sAMAccountName**](/windows/desktop/AD/group-objects) sur cet objet, car il s’agit d’un attribut obligatoire pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="e7e07-109">Second, he must set the [**samAccountName**](/windows/desktop/AD/group-objects) attribute on this object, because it is a mandatory attribute for backward compatibility.</span></span> <span data-ttu-id="e7e07-110">Pour cet exemple, lorsque **sAMAccountName** est défini, les outils Windows NT 4,0 tels que le gestionnaire des utilisateurs voient l’attribut en tant que **Mgmt** et non **gestion**.</span><span class="sxs-lookup"><span data-stu-id="e7e07-110">For this example, when **samAccountName** is set, Windows NT 4.0 tools such as User Manager see the attribute as **mgmt** instead of **Management**.</span></span>

<span data-ttu-id="e7e07-111">Enfin, Joe doit spécifier le type de groupe.</span><span class="sxs-lookup"><span data-stu-id="e7e07-111">Third, Joe must specify the type of group.</span></span> <span data-ttu-id="e7e07-112">Dans un domaine Windows 2000, il existe trois types de groupes : global, domaine local et universel.</span><span class="sxs-lookup"><span data-stu-id="e7e07-112">In a Windows 2000 domain, there are three types of groups: Global, Domain Local, and Universal.</span></span> <span data-ttu-id="e7e07-113">En outre, le groupe présente ses caractéristiques de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e7e07-113">In addition, the group carries its security characteristic.</span></span> <span data-ttu-id="e7e07-114">Un groupe peut être un groupe avec sécurité ou non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e7e07-114">A group can be either a security-enabled or a non-secured group.</span></span> <span data-ttu-id="e7e07-115">Pour l’essentiel, les groupes à sécurité activée sont ceux qui peuvent se voir accorder ou refuser des droits d’accès aux ressources, à l’instar d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7e07-115">Essentially, security-enabled groups are those that can be granted or denied access rights to resources, similar to a user.</span></span> <span data-ttu-id="e7e07-116">L’octroi à un groupe d’un accès à un partage de fichiers, par exemple, implique que tous les membres du groupe peuvent accéder au partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e7e07-116">Granting a group access to a file share, for example, implies that all members of the group can access the file share.</span></span> <span data-ttu-id="e7e07-117">Les listes de distribution ne peuvent pas être utilisées de la même façon : vous ne pouvez pas, par exemple, accorder à une liste de distribution le droit d’accéder à un partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e7e07-117">Distribution lists cannot be used in a similar manner—you cannot, for example, grant a distribution list the right to access a file share.</span></span> <span data-ttu-id="e7e07-118">Pendant la mise à niveau, les groupes Windows NT 4,0 sont migrés en tant que groupes à sécurité activée.</span><span class="sxs-lookup"><span data-stu-id="e7e07-118">During the upgrade, Windows NT 4.0 groups are migrated as security-enabled groups.</span></span> <span data-ttu-id="e7e07-119">Dans Active Directory, les groupes non sécurisés sont similaires aux listes de distribution dans Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7e07-119">Non-secured groups in Active Directory are similar to distribution lists in Exchange.</span></span> <span data-ttu-id="e7e07-120">Par conséquent, la création de groupes ou de listes de distribution est une opération similaire dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e7e07-120">Hence, creating groups or distribution lists are similar operations in Windows 2000.</span></span> <span data-ttu-id="e7e07-121">Dans le mode natif de Windows 2000 (le mode natif signifie que tous les contrôleurs de domaine d’un domaine sont des ordinateurs exécutant le serveur Windows 2000), les groupes peuvent être imbriqués à n’importe quel niveau.</span><span class="sxs-lookup"><span data-stu-id="e7e07-121">In the Windows 2000 native mode (native mode means that all domain controllers in a domain are computers running Windows 2000 Server), the groups can be nested to any level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7e07-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7e07-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7e07-123">Énumération d’objets</span><span class="sxs-lookup"><span data-stu-id="e7e07-123">Enumerating Objects</span></span>](enumerating-objects.md)
</dt> </dl>

 

 