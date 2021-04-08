---
title: RootDSE (ADSI)
description: Chaque serveur d’annuaire possède une entrée unique appelée RootDSE. Il fournit des données sur le serveur, telles que ses fonctionnalités, la version LDAP qu’il prend en charge et les contextes d’attribution de noms qu’il utilise.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730244"
---
# <a name="rootdse-adsi"></a><span data-ttu-id="e0961-104">RootDSE (ADSI)</span><span class="sxs-lookup"><span data-stu-id="e0961-104">RootDSE (ADSI)</span></span>

<span data-ttu-id="e0961-105">Chaque serveur d’annuaire possède une entrée unique appelée **rootDSE**.</span><span class="sxs-lookup"><span data-stu-id="e0961-105">Each directory server has a unique entry called **RootDSE**.</span></span> <span data-ttu-id="e0961-106">Il fournit des données sur le serveur, telles que ses fonctionnalités, la version LDAP qu’il prend en charge et les contextes d’attribution de noms qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="e0961-106">It provides data about the server, such as its capabilities, the LDAP version it supports, and the naming contexts it uses.</span></span>

<span data-ttu-id="e0961-107">Par exemple, pour créer un script ou une application qui peut s’exécuter sur n’importe quel environnement de domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="e0961-107">For example, to create a script, or application, that can run on any Windows domain environment.</span></span> <span data-ttu-id="e0961-108">Vous pouvez spécifier le nom unique, le nom du serveur ou le nom de domaine lors de la connexion à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e0961-108">You can specify either the distinguished name, server name, or domain name when connecting to Active Directory.</span></span> <span data-ttu-id="e0961-109">Si vous ne disposez pas de ces informations, vous pouvez utiliser l’objet **rootDSE** pour établir une connexion.</span><span class="sxs-lookup"><span data-stu-id="e0961-109">If you do not have this information, you can then use the **RootDSE** object to establish a connection.</span></span> <span data-ttu-id="e0961-110">L’exemple de code suivant modifie la description de domaine dans n’importe quel domaine.</span><span class="sxs-lookup"><span data-stu-id="e0961-110">The following code example changes the domain description in any domain.</span></span>


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



<span data-ttu-id="e0961-111">En obtenant l’attribut **defaultNamingContext** à partir de **rootDSE**, vous pouvez effectuer une liaison au domaine actuel, par exemple, le **DefaultNamingContext** Fabrikam est DC = fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="e0961-111">By getting the **defaultNamingContext** attribute from **RootDSE**, you can bind to the current domain, for example, the Fabrikam **defaultNamingContext** is DC=Fabrikam, DC=COM.</span></span>

<span data-ttu-id="e0961-112">Pour énumérer les propriétés du **rootDSE**, utilisez l’interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) .</span><span class="sxs-lookup"><span data-stu-id="e0961-112">To enumerate the properties of the **RootDSE**, use the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface.</span></span> <span data-ttu-id="e0961-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ne peut pas être utilisé pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="e0961-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) cannot be used for this task.</span></span>

<span data-ttu-id="e0961-114">Pour plus d’informations, consultez [liaison sans serveur et RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span><span class="sxs-lookup"><span data-stu-id="e0961-114">For more information, see [Serverless Binding and RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span></span>

 

 