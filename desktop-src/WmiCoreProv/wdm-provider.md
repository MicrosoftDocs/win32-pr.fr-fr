---
description: Le fournisseur WDM (Windows Driver Model) accorde l’accès aux classes, aux instances, aux méthodes et aux événements des pilotes matériels conformes au modèle WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Fournisseur WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753709"
---
# <a name="wdm-provider"></a><span data-ttu-id="62102-103">Fournisseur WDM</span><span class="sxs-lookup"><span data-stu-id="62102-103">WDM Provider</span></span>

<span data-ttu-id="62102-104">Le fournisseur WDM (Windows Driver Model) accorde l’accès aux classes, aux instances, aux méthodes et aux événements des pilotes matériels conformes au modèle WDM.</span><span class="sxs-lookup"><span data-stu-id="62102-104">The WDM (Windows Driver Model) provider grants access to the classes, instances, methods, and events of hardware drivers that conform to the WDM model.</span></span> <span data-ttu-id="62102-105">Les classes pour les pilotes de matériel résident dans l' \\ espace de noms WMI racine.</span><span class="sxs-lookup"><span data-stu-id="62102-105">The classes for hardware drivers reside in the "root\\wmi namespace".</span></span>

<span data-ttu-id="62102-106">Les classes WDM sont définies principalement dans WMI. mof.</span><span class="sxs-lookup"><span data-stu-id="62102-106">WDM classes are defined primarily in Wmi.mof.</span></span>

<span data-ttu-id="62102-107">WDM est une interface de système d’exploitation par le biais de laquelle les composants matériels fournissent des informations et des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="62102-107">WDM is an operating system interface through which hardware components provide information and event notification.</span></span> <span data-ttu-id="62102-108">Le fournisseur WDM est un fournisseur de classes, d’instances, d’événements et de méthodes qui permet aux applications de gestion d’accéder aux données et aux événements à partir des pilotes de périphérique compatibles WMI-pour-WDM.</span><span class="sxs-lookup"><span data-stu-id="62102-108">The WDM provider is a class, instance, event, and method provider that allows management applications access to data and events from WMI-for-WDM enabled device drivers.</span></span> <span data-ttu-id="62102-109">Les classes créées par le fournisseur WDM pour représenter des données de pilote de périphérique résident uniquement dans l' \\ espace de noms WMI racine.</span><span class="sxs-lookup"><span data-stu-id="62102-109">The classes created by the WDM provider to represent device driver data reside only in the "Root\\WMI" namespace.</span></span> <span data-ttu-id="62102-110">Cet espace de noms doit déjà exister avant que le fournisseur WDM ne traite les pilotes WDM installés.</span><span class="sxs-lookup"><span data-stu-id="62102-110">This namespace must already exist before the WDM provider will process the installed WDM drivers.</span></span>

<span data-ttu-id="62102-111">Le fournisseur WDM enregistre des informations sur les opérations WDM dans le fichier WmiProv. log.</span><span class="sxs-lookup"><span data-stu-id="62102-111">The WDM provider records information about WDM operations in the WmiProv.log file.</span></span> <span data-ttu-id="62102-112">Pour plus d’informations, consultez [fichiers journaux WMI](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="62102-112">For more information, see [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span>

<span data-ttu-id="62102-113">En tant que classe, instance, méthode et fournisseur d’événements, le fournisseur WDM implémente l’interface [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) standard, ainsi que les méthodes [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) suivantes :</span><span class="sxs-lookup"><span data-stu-id="62102-113">As a class, instance, method, and event provider, the WDM provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the following [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="62102-114">**CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="62102-114">**CreateClassEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="62102-115">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="62102-115">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="62102-116">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="62102-116">**GetObjectAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="62102-117">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="62102-117">**ExecMethodAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="62102-118">**ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="62102-118">**ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="62102-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="62102-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="62102-120">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="62102-120">**PutInstanceAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="62102-121">Le fournisseur WDM prend en charge l’événement extrinsèque [**WmiEvent**](/windows/desktop/WmiCoreProv/wmievent) , qui NOTIFIe WMI en ce qui concerne les événements des pilotes basés sur WDM.</span><span class="sxs-lookup"><span data-stu-id="62102-121">The WDM provider supports the [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) extrinsic event, which notifies WMI regarding events from WDM-based drivers.</span></span> <span data-ttu-id="62102-122">Vous pouvez inscrire vos consommateurs d’événements pour les événements **WmiEvent** comme vous le feriez pour n’importe quel autre événement.</span><span class="sxs-lookup"><span data-stu-id="62102-122">You can register your event consumers for **WMIEvent** events as you would any other event.</span></span> <span data-ttu-id="62102-123">Pour plus d’informations, consultez [réception d’un événement WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span><span class="sxs-lookup"><span data-stu-id="62102-123">For more information, see [Receiving a WMI Event](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span></span> <span data-ttu-id="62102-124">Aucun événement de création de classe n’est déclenché lors du démarrage d’un pilote.</span><span class="sxs-lookup"><span data-stu-id="62102-124">No class creation events are raised when starting a driver.</span></span>

<span data-ttu-id="62102-125">Le fournisseur WDM prend en charge la classe suivante :</span><span class="sxs-lookup"><span data-stu-id="62102-125">The WDM provider supports the following class:</span></span>

-   [<span data-ttu-id="62102-126">**WMIBinaryMofResource**</span><span class="sxs-lookup"><span data-stu-id="62102-126">**WMIBinaryMofResource**</span></span>](wmibinarymofresource.md)

## <a name="related-topics"></a><span data-ttu-id="62102-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62102-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62102-128">Fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="62102-128">WMI Providers</span></span>](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[<span data-ttu-id="62102-129">Accès aux données à partir des pilotes de périphérique</span><span class="sxs-lookup"><span data-stu-id="62102-129">Accessing Data from Device Drivers</span></span>](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
