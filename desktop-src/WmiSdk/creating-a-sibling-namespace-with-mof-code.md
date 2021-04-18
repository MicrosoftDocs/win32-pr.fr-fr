---
description: Une autre façon de créer un espace de noms consiste à utiliser du code format MOF (MOF) pour créer un espace de noms frère. Un espace de noms frère est un espace de noms qui n’existe pas en tant qu’enfant de l’espace de noms actuel.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Création d’un espace de noms frère avec du code MOF
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536610"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a><span data-ttu-id="eadc0-104">Création d’un espace de noms frère avec du code MOF</span><span class="sxs-lookup"><span data-stu-id="eadc0-104">Creating a Sibling Namespace with MOF Code</span></span>

<span data-ttu-id="eadc0-105">Une autre façon de créer un espace de noms consiste à utiliser du code format MOF (MOF) pour créer un espace de noms frère.</span><span class="sxs-lookup"><span data-stu-id="eadc0-105">Another way of creating a namespace is to use Managed Object Format (MOF) code to create a sibling namespace.</span></span> <span data-ttu-id="eadc0-106">Un espace de noms frère est un espace de noms qui n’existe pas en tant qu’enfant de l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="eadc0-106">A sibling namespace is a namespace that does not exist as a child of the current namespace.</span></span>

<span data-ttu-id="eadc0-107">La procédure suivante décrit comment créer un espace de noms frère avec du code MOF.</span><span class="sxs-lookup"><span data-stu-id="eadc0-107">The following procedure describes how to create a sibling namespace with MOF code.</span></span>

<span data-ttu-id="eadc0-108">**Pour créer un espace de noms frère avec du code MOF**</span><span class="sxs-lookup"><span data-stu-id="eadc0-108">**To create a sibling namespace with MOF code**</span></span>

1.  <span data-ttu-id="eadc0-109">Insérez la commande [**\# pragma namespace**](pragma-namespace.md) dans votre code MOF avant la déclaration d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="eadc0-109">Insert the [**\#pragma namespace**](pragma-namespace.md) command into your MOF code prior to the namespace declaration.</span></span>

    <span data-ttu-id="eadc0-110">La commande [**\# pragma namespace**](pragma-namespace.md) indique à WMI où créer les instances à la suite de la directive.</span><span class="sxs-lookup"><span data-stu-id="eadc0-110">The [**\#pragma namespace**](pragma-namespace.md) command instructs WMI where to create the instances following the directive.</span></span>

2.  <span data-ttu-id="eadc0-111">Créez une instance de la classe d' [**\_ \_ espace de noms**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="eadc0-111">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>
3.  <span data-ttu-id="eadc0-112">Compilez votre code à l’aide de l’utilitaire [mofcomp](mofcomp.md) ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="eadc0-112">Compile your code with the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="eadc0-113">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="eadc0-113">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="eadc0-114">L’exemple de code MOF suivant décrit comment créer un espace de noms en tant que frère de l’espace de noms « root \\ cimv2 ».</span><span class="sxs-lookup"><span data-stu-id="eadc0-114">The following MOF code example describes how to create a namespace as a sibling to the "Root\\CIMv2" namespace.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



