---
title: Attributs (AD DS)
description: Chaque objet dans Active Directory Domain Services contient un ensemble d’attributs qui définissent les caractéristiques de l’objet.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- attributs AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031054"
---
# <a name="attributes-ad-ds"></a><span data-ttu-id="08a31-104">Attributs (AD DS)</span><span class="sxs-lookup"><span data-stu-id="08a31-104">Attributes (AD DS)</span></span>

<span data-ttu-id="08a31-105">Chaque objet dans Active Directory Domain Services contient un ensemble d’attributs qui définissent les caractéristiques de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08a31-105">Each object in Active Directory Domain Services contains a set of attributes that define the characteristics of the object.</span></span> <span data-ttu-id="08a31-106">Chaque attribut est décrit par un objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) dans le conteneur de schéma qui définit l’attribut.</span><span class="sxs-lookup"><span data-stu-id="08a31-106">Each attribute is described by an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object in the schema container that defines the attribute.</span></span> <span data-ttu-id="08a31-107">La définition de l’attribut comprend une variété de données, par exemple, les types d’objets auxquels s’applique l’attribut et le type de syntaxe de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="08a31-107">The attribute definition includes a variety of data, for example, what object types that the attribute applies to and the syntax type of the attribute.</span></span> <span data-ttu-id="08a31-108">Pour plus d’informations sur les définitions de schéma d’attribut, consultez [caractéristiques des attributs](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="08a31-108">For more information about attribute schema definitions, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

<span data-ttu-id="08a31-109">La liste suivante répertorie les types d’attributs qui sont stockés dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="08a31-109">The following list lists the type of attributes that are stored in Active Directory Domain Services.</span></span>

<dl> <dt>

<span data-ttu-id="08a31-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Attributs stockés et répliqués dans un domaine</span><span class="sxs-lookup"><span data-stu-id="08a31-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Domain-replicated, stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="08a31-111">Certains attributs sont stockés dans le répertoire (par exemple, [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)et [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) et répliqués sur tous les contrôleurs de domaine dans un domaine.</span><span class="sxs-lookup"><span data-stu-id="08a31-111">Some attributes are stored in the directory (such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) and replicated to all domain controllers in a domain.</span></span> <span data-ttu-id="08a31-112">Un sous-ensemble de ces attributs est également répliqué dans le catalogue global.</span><span class="sxs-lookup"><span data-stu-id="08a31-112">A subset of these attributes is also replicated to the global catalog.</span></span> <span data-ttu-id="08a31-113">Si vous énumérez les attributs d’un objet à partir du catalogue global, seuls les attributs répliqués dans le catalogue global sont retournés.</span><span class="sxs-lookup"><span data-stu-id="08a31-113">If you enumerate attributes of an object from the global catalog, only the attributes replicated to the global catalog are returned.</span></span> <span data-ttu-id="08a31-114">Certains attributs sont également indexés, car l’inclusion d’une propriété indexée dans une requête améliore les performances des requêtes.</span><span class="sxs-lookup"><span data-stu-id="08a31-114">Some attributes are also indexed because including an indexed property in a query improves the query performance.</span></span>

</dd> <dt>

<span data-ttu-id="08a31-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Attributs non répliqués, stockés localement</span><span class="sxs-lookup"><span data-stu-id="08a31-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Non-replicated, locally stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="08a31-116">Les attributs non répliqués, tels que [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon)et [**Last-Logoff**](/windows/desktop/ADSchema/a-lastlogoff) , sont stockés sur chaque contrôleur de domaine, mais ne sont pas répliqués.</span><span class="sxs-lookup"><span data-stu-id="08a31-116">Non-replicated attributes, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon), and [**Last-Logoff**](/windows/desktop/ADSchema/a-lastlogoff) are stored on each domain controller, but are not replicated.</span></span> <span data-ttu-id="08a31-117">Les attributs non répliqués sont des attributs qui se rapportent à un contrôleur de domaine particulier.</span><span class="sxs-lookup"><span data-stu-id="08a31-117">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="08a31-118">Par exemple, l’attribut **Last-Logon** correspond à la date et à l’heure de la dernière validation de l’ouverture de session réseau de l’utilisateur par ce contrôleur de domaine particulier qui a retourné la propriété.</span><span class="sxs-lookup"><span data-stu-id="08a31-118">For example, **Last-Logon** attribute is the last date and time that the user's network logon was validated by that particular domain controller that returned the property.</span></span> <span data-ttu-id="08a31-119">Ces attributs peuvent être récupérés de la même façon que les attributs à l’ensemble du domaine décrits précédemment.</span><span class="sxs-lookup"><span data-stu-id="08a31-119">These attributes can be retrieved in the same way as the domain-wide attributes described previously.</span></span> <span data-ttu-id="08a31-120">Toutefois, pour ces attributs, chaque contrôleur de domaine stocke uniquement les valeurs qui se rapportent à ce contrôleur de domaine particulier.</span><span class="sxs-lookup"><span data-stu-id="08a31-120">However, for these attributes, each domain controller stores only values that pertain to that particular domain controller.</span></span> <span data-ttu-id="08a31-121">Par exemple, pour obtenir la dernière fois qu’un utilisateur a ouvert une session sur le domaine, récupérez l’attribut **Last-Logon** pour l’utilisateur de chaque contrôleur de domaine dans le domaine et recherchez la date et l’heure les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="08a31-121">For example, to obtain the last time that a user logged on to the domain, retrieve the **Last-Logon** attribute for the user from every domain controller in the domain and find that latest date and time.</span></span>

</dd> <dt>

<span data-ttu-id="08a31-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Attributs non stockés et construits</span><span class="sxs-lookup"><span data-stu-id="08a31-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Non-stored, constructed attributes</span></span>
</dt> <dd>

<span data-ttu-id="08a31-123">Un objet utilisateur a également des attributs construits qui ne sont pas stockés dans l’annuaire, mais qui sont calculés par le contrôleur de domaine, par exemple [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) et [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).</span><span class="sxs-lookup"><span data-stu-id="08a31-123">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) and [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).</span></span>

</dd> </dl>

 

 