---
description: Une autre façon de créer un espace de noms consiste à utiliser l’API WMI pour créer l’espace de noms par programme.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Création d’un espace de noms avec l’API WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534450"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a><span data-ttu-id="d633e-103">Création d’un espace de noms avec l’API WMI</span><span class="sxs-lookup"><span data-stu-id="d633e-103">Creating a Namespace with the WMI API</span></span>

<span data-ttu-id="d633e-104">Une autre façon de créer un espace de noms consiste à utiliser l’API WMI pour créer l’espace de noms par programme.</span><span class="sxs-lookup"><span data-stu-id="d633e-104">Another way of creating a namespace is to use the WMI API to create the namespace programmatically.</span></span> <span data-ttu-id="d633e-105">L’avantage de créer un espace de noms par programme est que vous pouvez créer l’espace de noms à partir d’une application.</span><span class="sxs-lookup"><span data-stu-id="d633e-105">The advantage to creating a namespace programmatically is that you can create the namespace from within an application.</span></span> <span data-ttu-id="d633e-106">Toutefois, l’utilisation de l’API WMI est plus complexe que l’utilisation de code format MOF (MOF) et vous ne pouvez pas aussi partager facilement vos espaces de noms avec d’autres développeurs.</span><span class="sxs-lookup"><span data-stu-id="d633e-106">However, using the WMI API is more complex than using Managed Object Format (MOF) code, and you cannot as easily share your namespaces with other developers.</span></span>

<span data-ttu-id="d633e-107">La procédure suivante décrit comment créer un espace de noms à l’aide de l’API WMI.</span><span class="sxs-lookup"><span data-stu-id="d633e-107">The following procedure describes how to create a namespace using the WMI API.</span></span>

<span data-ttu-id="d633e-108">**Pour créer un espace de noms à l’aide de l’API WMI**</span><span class="sxs-lookup"><span data-stu-id="d633e-108">**To create a namespace using the WMI API**</span></span>

1.  <span data-ttu-id="d633e-109">Utilisez [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) pour récupérer un pointeur vers un objet [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) qui pointe vers la classe système d' [**\_ \_ espace de noms**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="d633e-109">Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a pointer to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) object that points to the [**\_\_Namespace**](--namespace.md) system class.</span></span>
2.  <span data-ttu-id="d633e-110">Définissez une instance de la classe système d' [**\_ \_ espace de noms**](--namespace.md) avec un appel à [**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span><span class="sxs-lookup"><span data-stu-id="d633e-110">Define an instance of the [**\_\_Namespace**](--namespace.md) system class with a call to [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span></span>
3.  <span data-ttu-id="d633e-111">Définissez la propriété **Name** de l’instance d' [**\_ \_ espace de noms**](--namespace.md) avec un appel à [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="d633e-111">Set the **Name** property of the [**\_\_Namespace**](--namespace.md) instance with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>
4.  <span data-ttu-id="d633e-112">Créez l’espace de noms avec un appel à [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span><span class="sxs-lookup"><span data-stu-id="d633e-112">Create the namespace with a call to [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span></span>

    <span data-ttu-id="d633e-113">Le paramètre *Pint* de [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) doit pointer vers la nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="d633e-113">The *pInst* parameter of [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) should point to the new instance.</span></span>

 

 



