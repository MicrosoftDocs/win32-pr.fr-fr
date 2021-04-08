---
description: Pour créer un fournisseur de consommateur d’événements WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Inscription d’un fournisseur de consommateur d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755045"
---
# <a name="registering-an-event-consumer-provider"></a><span data-ttu-id="f0475-103">Inscription d’un fournisseur de consommateur d’événements</span><span class="sxs-lookup"><span data-stu-id="f0475-103">Registering an Event Consumer Provider</span></span>

<span data-ttu-id="f0475-104">Pour créer un [*fournisseur de consommateur d’événements*](gloss-e.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="f0475-104">To create a WMI [*event consumer provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="f0475-105">En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI.</span><span class="sxs-lookup"><span data-stu-id="f0475-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="f0475-106">La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f0475-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="f0475-107">La procédure suivante décrit comment inscrire un fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="f0475-107">The following procedure describes how to register an event consumer provider.</span></span>

<span data-ttu-id="f0475-108">**Pour inscrire un fournisseur de consommateur d’événements**</span><span class="sxs-lookup"><span data-stu-id="f0475-108">**To register an event consumer provider**</span></span>

1.  <span data-ttu-id="f0475-109">Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f0475-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="f0475-110">Créez une instance de la classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f0475-110">Create an instance of the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="f0475-111">Les propriétés définies par [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) incluent le chemin d’accès de l’objet au fournisseur et les noms des classes de consommateur logiques prises en charge par le fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="f0475-111">The properties that are defined by [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) include the object path to the provider and the names of the logical consumer classes that the event consumer provider supports.</span></span>

    <span data-ttu-id="f0475-112">Veillez à baliser la classe avec les qualificateurs **Dynamic** et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="f0475-112">Be sure to tag the class with both the **Dynamic** and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="f0475-113">Le qualificateur **dynamique** indique que WMI doit utiliser un fournisseur pour récupérer les instances de classe.</span><span class="sxs-lookup"><span data-stu-id="f0475-113">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="f0475-114">Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="f0475-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="f0475-115">L’exemple de code suivant montre comment inscrire un fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="f0475-115">The following code example shows how to register an event consumer provider.</span></span>

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



