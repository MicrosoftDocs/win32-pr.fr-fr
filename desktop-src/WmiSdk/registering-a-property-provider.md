---
description: Pour créer un fournisseur de propriétés WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Inscription d’un fournisseur de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202179"
---
# <a name="registering-a-property-provider"></a><span data-ttu-id="bf271-103">Inscription d’un fournisseur de propriétés</span><span class="sxs-lookup"><span data-stu-id="bf271-103">Registering a Property Provider</span></span>

<span data-ttu-id="bf271-104">Pour créer un [*fournisseur de propriétés*](gloss-p.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="bf271-104">To create a WMI [*property provider*](gloss-p.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span> <span data-ttu-id="bf271-105">En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI.</span><span class="sxs-lookup"><span data-stu-id="bf271-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="bf271-106">La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bf271-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="bf271-107">La procédure suivante décrit comment inscrire un fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="bf271-107">The following procedure describes how to register a property provider.</span></span>

<span data-ttu-id="bf271-108">**Pour inscrire un fournisseur de propriétés**</span><span class="sxs-lookup"><span data-stu-id="bf271-108">**To register a property provider**</span></span>

1.  <span data-ttu-id="bf271-109">Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="bf271-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the property provider.</span></span>

    <span data-ttu-id="bf271-110">La classe [**\_ \_ Win32Provider**](--win32provider.md) accepte les valeurs par défaut pour les autres propriétés, telles que la valeur **true** pour la propriété **pure** .</span><span class="sxs-lookup"><span data-stu-id="bf271-110">The [**\_\_Win32Provider**](--win32provider.md) class accepts the default values for other properties, such as the **TRUE** value for the **Pure** property.</span></span> <span data-ttu-id="bf271-111">Pour plus d’informations, consultez [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="bf271-111">For more information, see [**\_\_Win32Provider**](--win32provider.md).</span></span>

2.  <span data-ttu-id="bf271-112">Créez une instance de la classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bf271-112">Create an instance of the [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="bf271-113">La classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) hérite de nombreuses propriétés de la classe parente [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , qui fournit des valeurs booléennes qui indiquent la prise en charge de fonctionnalités particulières et un tableau de chaînes pour indiquer la prise en charge des requêtes.</span><span class="sxs-lookup"><span data-stu-id="bf271-113">The [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="bf271-114">Veillez à baliser la classe avec les qualificateurs [**Dynamic**](dynamic-qualifier.md) et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="bf271-114">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="bf271-115">Le qualificateur **dynamique** indique que WMI doit utiliser un fournisseur dynamique pour récupérer les instances de classe qui contiennent les propriétés prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bf271-115">The **Dynamic** qualifier signals that WMI should use a dynamic provider to retrieve the class instances that contain the supported properties.</span></span> <span data-ttu-id="bf271-116">Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="bf271-116">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="bf271-117">WMI appelle NewQuery sur un fournisseur d’événements lorsqu’un consommateur client inscrit une requête de filtre d’événement qui contient des références aux événements pris en charge par ce fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="bf271-117">WMI calls NewQuery on an event provider when a client consumer registers an event filter query that contains references to events supported by that event provider.</span></span> <span data-ttu-id="bf271-118">Ainsi, le fournisseur d’événements responsable des événements de modification d’instance pour la classe EmailClass peut être configuré pour générer des notifications uniquement pour l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="bf271-118">So the event provider responsible for instance modification events for the EmailClass class can be set up to generate notifications only for sender.</span></span> <span data-ttu-id="bf271-119">Lorsque le fournisseur reçoit une requête demandant la notification des modifications apportées à la propriété Subject, le fournisseur peut commencer à générer ces notifications.</span><span class="sxs-lookup"><span data-stu-id="bf271-119">When the provider receives a query requesting notification of changes to the subject property, the provider can start generating those notifications.</span></span> <span data-ttu-id="bf271-120">Dans ce scénario, WMI n’est pas obligé d’ignorer les notifications qui modifient uniquement les destinataires du rapport.</span><span class="sxs-lookup"><span data-stu-id="bf271-120">In this scenario, WMI is not required to discard the notifications that report recipient changes only.</span></span>

<span data-ttu-id="bf271-121">L’exemple de code MOF suivant décrit des instances qui peuvent être utilisées pour inscrire un fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="bf271-121">The following MOF code example describes instances that can be used to register a property provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> <span data-ttu-id="bf271-122">Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur de propriétés en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="bf271-122">Only administrators can register or delete a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span>

 

 

 



