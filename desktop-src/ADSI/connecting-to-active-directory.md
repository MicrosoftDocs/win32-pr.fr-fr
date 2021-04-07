---
title: Connexion à Active Directory
description: Plusieurs méthodes sont utilisées pour accéder à Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Connexion à Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939601"
---
# <a name="connecting-to-active-directory"></a><span data-ttu-id="e201b-104">Connexion à Active Directory</span><span class="sxs-lookup"><span data-stu-id="e201b-104">Connecting to Active Directory</span></span>

<span data-ttu-id="e201b-105">Plusieurs méthodes sont utilisées pour accéder à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e201b-105">There are several methods used to access Active Directory.</span></span> <span data-ttu-id="e201b-106">Il est recommandé d’utiliser l’API ADSI pour accéder à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e201b-106">It is recommended that you use the ADSI API to access Active Directory.</span></span> <span data-ttu-id="e201b-107">ADSI implémente le protocole LDAP pour communiquer avec Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e201b-107">ADSI implements the LDAP protocol to communicate with Active Directory.</span></span> <span data-ttu-id="e201b-108">Les exemples de code suivants montrent comment accéder à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e201b-108">The following code examples show how to access Active Directory.</span></span>


```VB
Set ns = GetObject("LDAP:")
```



<span data-ttu-id="e201b-109">Cela ouvre le fournisseur LDAP et le prépare à la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="e201b-109">This opens the LDAP provider and prepares it to retrieve data.</span></span> <span data-ttu-id="e201b-110">Aucune connexion n’est établie tant que les données ne sont pas demandées.</span><span class="sxs-lookup"><span data-stu-id="e201b-110">No connection is established until data is requested.</span></span> <span data-ttu-id="e201b-111">Lorsque les données sont demandées, ADSI, avec l’aide du service Localisateur, tente de trouver le meilleur contrôleur de domaine pour la connexion et établit une connexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="e201b-111">When data is requested, ADSI, with the help of the locator service, attempts to find the best domain controller (DC) for the connection and will establish a connection to the server.</span></span> <span data-ttu-id="e201b-112">Ce processus porte le nom de liaison sans serveur.</span><span class="sxs-lookup"><span data-stu-id="e201b-112">This process is known as serverless binding.</span></span>

<span data-ttu-id="e201b-113">ADSI vous permet également de spécifier le nom du serveur à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="e201b-113">ADSI also enables you to specify the server name to use for the connection.</span></span>


```VB
Set obj = GetObject("LDAP://mysrv01")
```



<span data-ttu-id="e201b-114">Dans un autre scénario, vous pouvez uniquement connaître le nom de domaine, mais pas le nom de serveur spécifique.</span><span class="sxs-lookup"><span data-stu-id="e201b-114">In another scenario, you may only know the domain name but not the specific server name.</span></span> <span data-ttu-id="e201b-115">Là encore, ADSI vous permet de spécifier le nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="e201b-115">Again, ADSI enables you to specify the domain name.</span></span> <span data-ttu-id="e201b-116">Dans Windows 2000, le nom de domaine est représenté sous la forme d’un nom DNS.</span><span class="sxs-lookup"><span data-stu-id="e201b-116">In Windows 2000, the domain name is represented as a DNS name.</span></span> <span data-ttu-id="e201b-117">Par exemple, si Joe worden, l’administrateur réseau, choisit de se connecter à l’aide du nom de domaine, il peut utiliser l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="e201b-117">For example, if Joe Worden, the network administrator, chooses to connect using the domain name, he could use the following code example.</span></span>


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



<span data-ttu-id="e201b-118">ADSI se connectera à l’un des contrôleurs de domaine dans le domaine fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="e201b-118">ADSI will connect to one of the domain controllers in the fabrikam.com domain.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e201b-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e201b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e201b-120">Liaison à des objets Active Directory</span><span class="sxs-lookup"><span data-stu-id="e201b-120">Binding to Active Directory Objects</span></span>](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




