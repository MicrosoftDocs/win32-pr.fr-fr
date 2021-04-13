---
description: Pour créer un fournisseur d’instances WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ InstanceProviderRegistration.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Inscription d’un fournisseur d’instances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528503"
---
# <a name="registering-an-instance-provider"></a><span data-ttu-id="880ef-103">Inscription d’un fournisseur d’instances</span><span class="sxs-lookup"><span data-stu-id="880ef-103">Registering an Instance Provider</span></span>

<span data-ttu-id="880ef-104">Pour créer un [*fournisseur d’instances*](gloss-i.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="880ef-104">To create a WMI [*instance provider*](gloss-i.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="880ef-105">En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI.</span><span class="sxs-lookup"><span data-stu-id="880ef-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="880ef-106">La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="880ef-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="880ef-107">La procédure suivante décrit comment inscrire un fournisseur d’instances.</span><span class="sxs-lookup"><span data-stu-id="880ef-107">The following procedure describes how to register an instance provider.</span></span>

<span data-ttu-id="880ef-108">**Pour inscrire un fournisseur d’instances**</span><span class="sxs-lookup"><span data-stu-id="880ef-108">**To register an instance provider**</span></span>

1.  <span data-ttu-id="880ef-109">Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="880ef-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="880ef-110">Créez une instance de la classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="880ef-110">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="880ef-111">La classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) hérite de nombreuses propriétés de la classe parente [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , qui fournit des valeurs booléennes qui indiquent la prise en charge de fonctionnalités particulières et un tableau de chaînes pour indiquer la prise en charge des requêtes.</span><span class="sxs-lookup"><span data-stu-id="880ef-111">The [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="880ef-112">Veillez à baliser la classe avec les qualificateurs [**Dynamic**](standard-wmi-qualifiers.md) et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="880ef-112">Be sure to tag the class with both the [**Dynamic**](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="880ef-113">Le qualificateur indique que WMI doit utiliser un fournisseur **dynamique** pour récupérer les instances de classe.</span><span class="sxs-lookup"><span data-stu-id="880ef-113">The qualifier signals that WMI should use a **Dynamic** provider to retrieve the class instances.</span></span> <span data-ttu-id="880ef-114">Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="880ef-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="880ef-115">L’exemple de code suivant décrit comment inscrire une instance [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="880ef-115">The following code example describes how to register a [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) instance.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



