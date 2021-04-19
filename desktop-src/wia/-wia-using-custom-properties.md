---
description: Utilisation des propriétés personnalisées.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Utilisation de propriétés personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517524"
---
# <a name="using-custom-properties"></a><span data-ttu-id="f2c0a-103">Utilisation de propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="f2c0a-103">Using Custom Properties</span></span>

<span data-ttu-id="f2c0a-104">**Utilisation des propriétés personnalisées**.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-104">**Using Custom Properties**.</span></span>

<span data-ttu-id="f2c0a-105">Un pilote WIA (Windows Image Acquisition) peut définir ses propres propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-105">A Windows Image Acquisition (WIA) driver can define its own custom properties.</span></span> <span data-ttu-id="f2c0a-106">Les appelants peuvent manipuler des propriétés personnalisées de la même façon que les propriétés WIA normales.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-106">Callers can manipulate custom properties just as they would normal WIA properties.</span></span> <span data-ttu-id="f2c0a-107">Toutefois, seul votre application ou votre module d’interface utilisateur personnalisé peuvent accéder à ces propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-107">However, only your application or custom UI module can access these custom properties.</span></span>

<span data-ttu-id="f2c0a-108">Les pilotes WIA doivent définir les propriétés personnalisées de façon à ce qu’elles aient des identificateurs de propriété qui sont décalées par les \_ DEVPROP privées WIA \_ pour les propriétés de l’appareil, et utiliser \_ \_ des ITEMPROP privées WIA pour les propriétés d’élément normales, par exemple dans [IWiaMiniDrv ::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx).</span><span class="sxs-lookup"><span data-stu-id="f2c0a-108">WIA drivers should define the custom properties to have property identifiers that are offset by WIA\_PRIVATE\_DEVPROP for device properties, and use WIA\_PRIVATE\_ITEMPROP for normal item properties, such as inside [IWiaMiniDrv::drvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx).</span></span> <span data-ttu-id="f2c0a-109">Pour plus d’informations, consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f2c0a-109">For more information, see [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="f2c0a-110">Il existe deux façons de passer des paramètres personnalisés à des pilotes WIA.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-110">There are two ways to pass custom parameters to WIA drivers.</span></span>

<span data-ttu-id="f2c0a-111">La première option consiste à utiliser la méthode **IWiaItemExtras :: Escape** (décrite dans la documentation du kit de développement logiciel (SDK) Platform).</span><span class="sxs-lookup"><span data-stu-id="f2c0a-111">The first option is to use the **IWiaItemExtras::Escape** method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="f2c0a-112">Cela est similaire à la méthode [IStiUSD :: Escape](https://msdn.microsoft.com/library/ms794396.aspx) , mais permet aux appelants d’utiliser WIA directement, au lieu d’utiliser les méthodes STI.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-112">This is similar to the [IStiUSD::Escape](https://msdn.microsoft.com/library/ms794396.aspx) method, but it allows callers to use WIA directly, instead of using STI methods.</span></span> <span data-ttu-id="f2c0a-113">À l’aide de **IWiaItemExtras :: Escape**, vous pouvez transmettre n’importe quelle information au pilote et le pilote peut transférer toutes les informations.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-113">Using **IWiaItemExtras::Escape**, you can pass any information to the driver, and the driver can pass any information back.</span></span> <span data-ttu-id="f2c0a-114">Le service WIA gère uniquement les mémoires tampons transmises entre l’appelant et le pilote.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-114">The WIA service manages only those buffers passed between the caller and the driver.</span></span>

<span data-ttu-id="f2c0a-115">La deuxième option consiste à utiliser des propriétés personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-115">The second option is to use custom properties.</span></span> <span data-ttu-id="f2c0a-116">L’utilisation de la méthode **IWiaItemExtras :: Escape** est plus souple que l’utilisation de propriétés WIA personnalisées, mais les propriétés WIA personnalisées vous permettent de stocker des informations dans le flux de propriété de l’élément afin que le pilote puisse lire les informations à un autre moment.</span><span class="sxs-lookup"><span data-stu-id="f2c0a-116">Using the **IWiaItemExtras::Escape** method is more flexible than using custom WIA properties, but custom WIA properties allow you to store information in the item's property stream so that the driver can read the information at another time.</span></span>

 

 



