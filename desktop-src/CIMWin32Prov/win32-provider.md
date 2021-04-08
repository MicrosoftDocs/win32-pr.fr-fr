---
description: Microsoft&\# 160 ; Le fournisseur Win32 récupère et met à jour les données relatives aux systèmes Windows&\# 8212 ; des données telles que les paramètres actuels des variables d’environnement et les attributs d’un disque logique.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Fournisseur Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747901"
---
# <a name="win32-provider"></a><span data-ttu-id="83dd1-103">Fournisseur Win32</span><span class="sxs-lookup"><span data-stu-id="83dd1-103">Win32 Provider</span></span>

<span data-ttu-id="83dd1-104">Le fournisseur Microsoft Win32 récupère et met à jour les données relatives aux systèmes Windows, telles que les paramètres actuels des variables d’environnement et les attributs d’un disque logique.</span><span class="sxs-lookup"><span data-stu-id="83dd1-104">The Microsoft Win32 provider retrieves and updates data relevant to Windows systems—data such as the current settings of environment variables and the attributes of a logical disk.</span></span> <span data-ttu-id="83dd1-105">Avec le fournisseur Win32, les applications de gestion peuvent utiliser WMI pour accéder facilement à ces données.</span><span class="sxs-lookup"><span data-stu-id="83dd1-105">With the Win32 provider, management applications can use WMI to easily access this data.</span></span> <span data-ttu-id="83dd1-106">Le fournisseur Win32 récupère ses informations en effectuant des appels de fonction Windows et en interrogeant le registre système.</span><span class="sxs-lookup"><span data-stu-id="83dd1-106">The Win32 provider retrieves its information by making Windows function calls and querying the system registry.</span></span>

<span data-ttu-id="83dd1-107">Le fournisseur Win32 définit les classes utilisées pour décrire le matériel ou les logiciels disponibles sur les systèmes Windows et les relations entre eux.</span><span class="sxs-lookup"><span data-stu-id="83dd1-107">The Win32 provider defines the classes used to describe hardware or software available on Windows systems and the relationships between them.</span></span>

<span data-ttu-id="83dd1-108">En tant que fournisseur d’instance et de méthode, le fournisseur Win32 implémente l’interface [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) standard, ainsi que les méthodes [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) suivantes :</span><span class="sxs-lookup"><span data-stu-id="83dd1-108">As an instance and method provider, the Win32 provider implements the standard [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface as well as the following [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="83dd1-109">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="83dd1-109">**CreateInstanceEnumAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="83dd1-110">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="83dd1-110">**DeleteInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="83dd1-111">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="83dd1-111">**ExecMethodAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="83dd1-112">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="83dd1-112">**ExecQueryAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="83dd1-113">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="83dd1-113">**GetObjectAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="83dd1-114">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="83dd1-114">**PutInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="83dd1-115">Le tableau suivant répertorie les catégories de classes du fournisseur Win32.</span><span class="sxs-lookup"><span data-stu-id="83dd1-115">The following table lists the Win32 provider class categories.</span></span>



| <span data-ttu-id="83dd1-116">Classes</span><span class="sxs-lookup"><span data-stu-id="83dd1-116">Classes</span></span>                                                                             | <span data-ttu-id="83dd1-117">Description</span><span class="sxs-lookup"><span data-stu-id="83dd1-117">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="83dd1-118">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="83dd1-118">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)<br/> | <span data-ttu-id="83dd1-119">Objets liés au matériel.</span><span class="sxs-lookup"><span data-stu-id="83dd1-119">Hardware-related objects.</span></span><br/>                                      |
| [<span data-ttu-id="83dd1-120">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="83dd1-120">Operating System Classes</span></span>](operating-system-classes.md)<br/>                 | <span data-ttu-id="83dd1-121">Objets associés au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="83dd1-121">Operating system related objects.</span></span><br/>                              |
| [<span data-ttu-id="83dd1-122">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="83dd1-122">Performance Counter Classes</span></span>](performance-counter-classes.md)<br/>           | <span data-ttu-id="83dd1-123">Données de performances brutes et calculées à partir des compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="83dd1-123">Raw and calculated performance data from performance counters.</span></span><br/> |
| [<span data-ttu-id="83dd1-124">Classes de gestion des services WMI</span><span class="sxs-lookup"><span data-stu-id="83dd1-124">WMI Service Management Classes</span></span>](wmi-service-management-classes.md)<br/>     | <span data-ttu-id="83dd1-125">Gestion pour WMI.</span><span class="sxs-lookup"><span data-stu-id="83dd1-125">Management for WMI.</span></span><br/>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="83dd1-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83dd1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83dd1-127">Fournisseur WMI CIMWin32</span><span class="sxs-lookup"><span data-stu-id="83dd1-127">CIMWin32 WMI Provider</span></span>](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
