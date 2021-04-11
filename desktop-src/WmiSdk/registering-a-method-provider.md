---
description: Pour créer un fournisseur de méthode WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Inscription d’un fournisseur de méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203729"
---
# <a name="registering-a-method-provider"></a><span data-ttu-id="a02f3-103">Inscription d’un fournisseur de méthode</span><span class="sxs-lookup"><span data-stu-id="a02f3-103">Registering a Method Provider</span></span>

<span data-ttu-id="a02f3-104">Pour créer un [*fournisseur de méthode*](gloss-m.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="a02f3-104">To create a WMI [*method provider*](gloss-m.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_MethodProviderRegistration**](--methodproviderregistration.md).</span></span> <span data-ttu-id="a02f3-105">Après avoir créé une instance de [**\_ \_ Win32Provider**](--win32provider.md), vous devez inscrire ce fournisseur auprès de WMI.</span><span class="sxs-lookup"><span data-stu-id="a02f3-105">After creating an instance of [**\_\_Win32Provider**](--win32provider.md), you must register that provider with WMI.</span></span> <span data-ttu-id="a02f3-106">En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI.</span><span class="sxs-lookup"><span data-stu-id="a02f3-106">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="a02f3-107">La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a02f3-107">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="a02f3-108">La procédure suivante décrit comment inscrire un fournisseur de méthodes.</span><span class="sxs-lookup"><span data-stu-id="a02f3-108">The following procedure describes how to register a method provider.</span></span>

<span data-ttu-id="a02f3-109">**Pour inscrire un fournisseur de méthode**</span><span class="sxs-lookup"><span data-stu-id="a02f3-109">**To register a method provider**</span></span>

1.  <span data-ttu-id="a02f3-110">Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a02f3-110">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>

    <span data-ttu-id="a02f3-111">La classe système [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) hérite de nombreuses propriétés de la classe parente [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) . Toutefois, la seule propriété pertinente pour un fournisseur de méthode est le chemin d’accès de l’objet à l’instance [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="a02f3-111">The [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) system class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, However, the only property relevant for a method provider is the object path to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span>

2.  <span data-ttu-id="a02f3-112">Créez une instance de la classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a02f3-112">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="a02f3-113">Veillez à baliser la classe avec les qualificateurs [**Dynamic**](dynamic-qualifier.md) et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="a02f3-113">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="a02f3-114">Le qualificateur **dynamique** indique que WMI doit utiliser un fournisseur pour récupérer les instances de classe.</span><span class="sxs-lookup"><span data-stu-id="a02f3-114">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="a02f3-115">Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="a02f3-115">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="a02f3-116">L’exemple de code suivant décrit comment inscrire un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="a02f3-116">The following code example describes how to register a method provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



