---
description: Pour supprimer les compteurs de performance de vos applications du système, procédez comme suit.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Suppression de compteurs de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530861"
---
# <a name="deleting-performance-counters"></a><span data-ttu-id="77353-103">Suppression de compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="77353-103">Deleting Performance Counters</span></span>

<span data-ttu-id="77353-104">Pour supprimer les compteurs de performance de votre application du système, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="77353-104">To remove your application's performance counters from the system, perform the following steps.</span></span>

1.  <span data-ttu-id="77353-105">Utilisez l’outil **unlodctr** inclus avec l’ordinateur pour supprimer les données relatives aux compteurs du Registre.</span><span class="sxs-lookup"><span data-stu-id="77353-105">Use the **unlodctr** tool included with the computer to remove the counter related data from the registry.</span></span> <span data-ttu-id="77353-106">Notez que la clé de **performance** de l’application doit exister pour que l’outil **unlodctr** aboutisse.</span><span class="sxs-lookup"><span data-stu-id="77353-106">Note that the application's **Performance** key must exist for the **unlodctr** tool to succeed.</span></span> <span data-ttu-id="77353-107">Pour plus d’informations, consultez [suppression des noms et des descriptions des compteurs du Registre](removing-counter-names-and-descriptions-from-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="77353-107">For details, see [Removing Counter Names and Descriptions from the Registry](removing-counter-names-and-descriptions-from-the-registry.md).</span></span>
2.  <span data-ttu-id="77353-108">Supprimez les clés de **performances** et de **liaison** sous la clé **services** de l’application.</span><span class="sxs-lookup"><span data-stu-id="77353-108">Delete the **Performance** and **Linkage** keys under the application's **Services** key.</span></span> <span data-ttu-id="77353-109">Pour supprimer ces clés, utilisez l’utilitaire Regedt32.exe ou appelez [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span><span class="sxs-lookup"><span data-stu-id="77353-109">To delete these keys, use either the Regedt32.exe utility or call [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span></span>

 

 
