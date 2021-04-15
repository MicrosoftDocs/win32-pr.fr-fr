---
title: Liaison sans serveur et RootDSE
description: Si possible, ne codez pas en dur un nom de serveur.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Liaison sans serveur et RootDSE AD
- PUBLICITÉ de liaison sans serveur
- RootDSE Active Directory
- Active Directory, utilisation de, liaison, liaison sans serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462827"
---
# <a name="serverless-binding-and-rootdse"></a><span data-ttu-id="64718-107">Liaison sans serveur et RootDSE</span><span class="sxs-lookup"><span data-stu-id="64718-107">Serverless Binding and RootDSE</span></span>

<span data-ttu-id="64718-108">Si possible, ne codez pas en dur un nom de serveur.</span><span class="sxs-lookup"><span data-stu-id="64718-108">If possible, do not hard-code a server name.</span></span> <span data-ttu-id="64718-109">En outre, dans la plupart des cas, la liaison ne doit pas être inutilement liée à un serveur unique.</span><span class="sxs-lookup"><span data-stu-id="64718-109">Furthermore, under most circumstances, binding should not be unnecessarily tied to a single server.</span></span> <span data-ttu-id="64718-110">Active Directory Domain Services prendre en charge la liaison sans serveur, ce qui signifie que Active Directory peut être lié à sur le domaine par défaut sans spécifier le nom d’un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="64718-110">Active Directory Domain Services support serverless binding, which means that Active Directory can be bound to on the default domain without specifying the name of a domain controller.</span></span> <span data-ttu-id="64718-111">Pour les applications ordinaires, il s’agit généralement du domaine de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="64718-111">For ordinary applications, this is typically the domain of the logged-on user.</span></span> <span data-ttu-id="64718-112">Pour les applications de service, il s’agit soit du domaine du compte d’ouverture de session du service, soit de celui du client emprunté par le service.</span><span class="sxs-lookup"><span data-stu-id="64718-112">For service applications, this is either the domain of the service logon account or that of the client that the service impersonates.</span></span>

<span data-ttu-id="64718-113">Dans LDAP 3,0, rootDSE est défini comme la racine de l’arborescence de données de l’annuaire sur un serveur d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="64718-113">In LDAP 3.0, rootDSE is defined as the root of the directory data tree on a directory server.</span></span> <span data-ttu-id="64718-114">RootDSE ne fait partie d’aucun espace de noms.</span><span class="sxs-lookup"><span data-stu-id="64718-114">The rootDSE is not part of any namespace.</span></span> <span data-ttu-id="64718-115">L’objectif de rootDSE est de fournir des données sur le serveur d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="64718-115">The purpose of the rootDSE is to provide data about the directory server.</span></span> <span data-ttu-id="64718-116">Voici la chaîne de liaison utilisée pour effectuer une liaison à rootDSE.</span><span class="sxs-lookup"><span data-stu-id="64718-116">The following is the binding string that is used to bind to rootDSE.</span></span>


```C++
LDAP://<servername>/rootDSE
```



<span data-ttu-id="64718-117"><servername>Est le nom DNS d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="64718-117">The <servername> is the DNS name of a server.</span></span> <span data-ttu-id="64718-118"><servername>Est facultatif, comme indiqué dans le format suivant.</span><span class="sxs-lookup"><span data-stu-id="64718-118">The <servername> is optional, as shown in the following format.</span></span>


```C++
LDAP://rootDSE
```



<span data-ttu-id="64718-119">Dans ce cas, un contrôleur de domaine par défaut du domaine dans lequel se trouve le contexte de sécurité du thread appelant sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="64718-119">In this case, a default domain controller from the domain that the security context of the calling thread is in will be used.</span></span> <span data-ttu-id="64718-120">Si un contrôleur de domaine n’est pas accessible à l’intérieur du site, le premier contrôleur de domaine qui peut être trouvé sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="64718-120">If a domain controller cannot be accessed within the site, the first domain controller that can be found will be used.</span></span>

<span data-ttu-id="64718-121">Le rootDSE est un emplacement bien connu et fiable sur chaque serveur d’annuaire pour obtenir les noms uniques des conteneurs de domaine, de schéma et de configuration, ainsi que d’autres données sur le serveur et le contenu de l’arborescence de données de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="64718-121">The rootDSE is a well-known and reliable location on every directory server to get distinguished names of the domain, schema, and configuration containers, and other data about the server and the contents of its directory data tree.</span></span> <span data-ttu-id="64718-122">Ces propriétés changent rarement sur un serveur particulier.</span><span class="sxs-lookup"><span data-stu-id="64718-122">These properties rarely change on a particular server.</span></span> <span data-ttu-id="64718-123">Une application peut lire ces propriétés au démarrage et les utiliser tout au long de la session.</span><span class="sxs-lookup"><span data-stu-id="64718-123">An application can read these properties at startup and use them throughout the session.</span></span>

<span data-ttu-id="64718-124">En résumé, une application doit utiliser une liaison sans serveur pour effectuer la liaison au répertoire sur le domaine actuel, utiliser rootDSE pour obtenir le nom unique d’un espace de noms et utiliser ce nom unique pour effectuer une liaison à des objets dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="64718-124">In summary, an application should use serverless binding to bind to the directory on the current domain, use rootDSE to get the distinguished name for a namespace, and use that distinguished name to bind to objects in the namespace.</span></span>

<span data-ttu-id="64718-125">Pour plus d’informations sur les attributs pris en charge par rootDSE, consultez [rootDSE](/windows/desktop/ADSchema/rootdse) dans la documentation du schéma Active Directory.</span><span class="sxs-lookup"><span data-stu-id="64718-125">For more information about attributes supported by rootDSE, see [RootDSE](/windows/desktop/ADSchema/rootdse) in the Active Directory Schema documentation.</span></span>

<span data-ttu-id="64718-126">Pour plus d’informations et pour obtenir un exemple de code qui montre comment utiliser une liaison sans serveur et rootDSE, consultez [l’exemple de code permettant d’obtenir le nom unique du domaine](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span><span class="sxs-lookup"><span data-stu-id="64718-126">For more information and a code example that shows how to use serverless binding and rootDSE, see [Example Code for Getting the Distinguished Name of the Domain](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span></span>

 

 