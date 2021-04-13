---
description: La corrélation affecte l’ensemble des classes retournées à partir du stockage SMIR.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Corrélation de classe SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202280"
---
# <a name="wmi-snmp-class-correlation"></a><span data-ttu-id="7225e-103">Corrélation de classe SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="7225e-103">WMI SNMP Class Correlation</span></span>

<span data-ttu-id="7225e-104">La corrélation affecte l’ensemble des classes retournées à partir du stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="7225e-104">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="7225e-105">Les classes corrélées sont celles qu’un appareil SNMP donné peut prendre en charge au moment de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="7225e-105">Correlated classes are those that a given SNMP device is known to support at the time enumeration occurs.</span></span> <span data-ttu-id="7225e-106">L’énumération non corrélée retourne toutes les classes présentes dans le stockage SMIR, que l’appareil les prenne en charge ou non.</span><span class="sxs-lookup"><span data-stu-id="7225e-106">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="7225e-107">La corrélation est une fonctionnalité du fournisseur SNMP SNMP qui peut être activée ou désactivée (par défaut).</span><span class="sxs-lookup"><span data-stu-id="7225e-107">Correlation is a feature of the WMI SNMP provider and can be turned off or on (default).</span></span>

> [!Note]  
> <span data-ttu-id="7225e-108">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7225e-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="7225e-109">La corrélation peut vous empêcher de voir toutes les classes qui sont réellement prises en charge par un appareil.</span><span class="sxs-lookup"><span data-stu-id="7225e-109">Correlation might prevent you from seeing all of the classes that are actually supported by a device.</span></span> <span data-ttu-id="7225e-110">Si vous savez qu’une classe particulière est prise en charge, mais qu’elle n’apparaît pas dans le stockage SMIR, cela peut être dû à plusieurs raisons, dont l’une est la corrélation.</span><span class="sxs-lookup"><span data-stu-id="7225e-110">If you know that a particular class is supported but it does not appear in the SMIR, this could be due to several reasons, one of which is correlation.</span></span> <span data-ttu-id="7225e-111">Envisagez de désactiver la corrélation avant d’écrire sur l’appareil en question.</span><span class="sxs-lookup"><span data-stu-id="7225e-111">Consider turning correlation off before writing to the device in question.</span></span> <span data-ttu-id="7225e-112">Toutefois, la désactivation de la corrélation entraîne la probabilité que de nombreuses classes non prises en charge par l’appareil s’affichent dans le stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="7225e-112">However, turning correlation off results in the likelihood that many classes not supported by the device will appear in the SMIR.</span></span> <span data-ttu-id="7225e-113">En outre, il y a un coût de performance dans l’utilisation de la corrélation, car l’appareil est interrogé pour voir les classes qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="7225e-113">Also, there is a performance cost in using correlation because the device is queried to see what classes it supports.</span></span> <span data-ttu-id="7225e-114">Lorsque la corrélation est activée, le fournisseur SNMP provoque une énumération des classes prises en charge par l’appareil, comme le résultat de l’exécution d’un outil de *parcours MIB* .</span><span class="sxs-lookup"><span data-stu-id="7225e-114">When correlation is turned on, the SNMP provider causes an enumeration of device-supported classes similar to the result of running a *mib walk* tool.</span></span>

<span data-ttu-id="7225e-115">Par exemple, un gestionnaire de réseau souhaite connaître plusieurs éléments clés de données sur tous les hubs gérés dans un réseau particulier.</span><span class="sxs-lookup"><span data-stu-id="7225e-115">For example, a network manager wants to know several key pieces of data about all the managed hubs in a particular network.</span></span> <span data-ttu-id="7225e-116">Une base de données des appareils actuels et leurs MIB pris en charge existent déjà. il n’est donc pas nécessaire de s’appuyer sur la fonction de corrélation de l’appareil pour fournir les éléments de données pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7225e-116">A database of the current devices and their supported MIBs already exists, so there is no need to rely on the correlation function of the device to provide the supported data elements.</span></span> <span data-ttu-id="7225e-117">Dans ce cas, la corrélation peut être désactivée.</span><span class="sxs-lookup"><span data-stu-id="7225e-117">In this case, correlation could be turned off.</span></span>

<span data-ttu-id="7225e-118">L’exemple suivant montre comment désactiver la corrélation.</span><span class="sxs-lookup"><span data-stu-id="7225e-118">The following example shows how to turn off correlation.</span></span>


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



<span data-ttu-id="7225e-119">En revanche, un autre gestionnaire de réseau peut souhaiter surveiller tous les lecteurs de disque d’ordinateur UNIX sur le réseau, mais il n’est pas familiarisé avec les données MIB sur ces machines.</span><span class="sxs-lookup"><span data-stu-id="7225e-119">On the other hand, another network manager may want to monitor all the UNIX machine disk drives on the network but is unfamiliar with the MIB data on those machines.</span></span> <span data-ttu-id="7225e-120">Dans ce cas, la corrélation est activée.</span><span class="sxs-lookup"><span data-stu-id="7225e-120">In that case, correlation would be turned on.</span></span>

 

 



