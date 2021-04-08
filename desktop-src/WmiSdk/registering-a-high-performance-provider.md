---
description: Comme les autres fournisseurs d’instances, vous inscrivez un fournisseur de haute performance auprès de Microsoft Windows&\# 160 ; Management Instrumentation (WMI) en créant une instance des \_ \_ classes Win32Provider et \_ \_ InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Inscription d’un fournisseur de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034255"
---
# <a name="registering-a-high-performance-provider"></a><span data-ttu-id="ef8fe-103">Inscription d’un fournisseur de High-Performance</span><span class="sxs-lookup"><span data-stu-id="ef8fe-103">Registering a High-Performance Provider</span></span>

<span data-ttu-id="ef8fe-104">Comme les autres fournisseurs d’instances, vous inscrivez un fournisseur de haute performance auprès de Microsoft Windows Management Instrumentation (WMI) en créant une instance des classes [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="ef8fe-104">Like other instance providers, you register a high-performance provider with Microsoft Windows Management Instrumentation (WMI) by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes.</span></span> <span data-ttu-id="ef8fe-105">L’instance **\_ \_ Win32Provider** définit l’implémentation physique du fournisseur et l’instance **\_ \_ InstanceProviderRegistration** définit l’ensemble de fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-105">The **\_\_Win32Provider** instance defines the provider's physical implementation, and the **\_\_InstanceProviderRegistration** instance defines the provider's feature set.</span></span> <span data-ttu-id="ef8fe-106">Pour plus d’informations, consultez [inscription d’un fournisseur](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ef8fe-106">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="ef8fe-107">La procédure suivante décrit comment inscrire un fournisseur d’instances à hautes performances.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-107">The following procedure describes how to register a high-performance instance provider.</span></span>

<span data-ttu-id="ef8fe-108">**Pour inscrire un fournisseur d’instances à hautes performances**</span><span class="sxs-lookup"><span data-stu-id="ef8fe-108">**To register a high-performance instance provider**</span></span>

1.  <span data-ttu-id="ef8fe-109">Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) décrivant le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class describing the provider.</span></span>

    <span data-ttu-id="ef8fe-110">Veillez à ajouter une propriété **ClientLoadableCLSID** à l’instance [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="ef8fe-110">Be sure to add a **ClientLoadableCLSID** property to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span> <span data-ttu-id="ef8fe-111">Si le fournisseur et le client résident sur le même ordinateur, WMI charge le fournisseur in-process sur le client à l’aide de **ClientLoadableCLSID** comme identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-111">If both the provider and client reside on the same computer, WMI loads the provider in-process to the client using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="ef8fe-112">Lorsque le fournisseur et le client résident sur des ordinateurs différents, WMI charge le fournisseur in-process dans le processus WMI.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-112">When the provider and client reside on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="ef8fe-113">WMI utilise également **ClientLoadableCLSID** pour prendre en charge les opérations d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-113">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

2.  <span data-ttu-id="ef8fe-114">Créez une instance de la classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-114">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="ef8fe-115">Veillez à baliser la classe avec les qualificateurs [**Dynamic**](dynamic-qualifier.md) et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="ef8fe-115">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="ef8fe-116">Le qualificateur **dynamique** indique que WMI doit utiliser un fournisseur pour récupérer les instances de classe.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-116">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="ef8fe-117">Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-117">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

    <span data-ttu-id="ef8fe-118">Un fournisseur à hautes performances doit également indiquer la prise en charge des opérations, des opérations d’énumération ou des deux.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-118">A high-performance provider also needs to state support for operations, enumeration operations, or both.</span></span> <span data-ttu-id="ef8fe-119">Veillez à utiliser les propriétés **SupportsGet** et **SupportsEnumeration** dans votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-119">Make sure you use the **SupportsGet** and **SupportsEnumeration** properties in your implementation.</span></span>

<span data-ttu-id="ef8fe-120">L’exemple de code suivant montre comment implémenter les classes [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) pour un fournisseur à hautes performances.</span><span class="sxs-lookup"><span data-stu-id="ef8fe-120">The following code example shows you how to implement the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes for a high-performance provider.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a><span data-ttu-id="ef8fe-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef8fe-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef8fe-122">Création d’un fournisseur d’instances dans un fournisseur de High-Performance</span><span class="sxs-lookup"><span data-stu-id="ef8fe-122">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



