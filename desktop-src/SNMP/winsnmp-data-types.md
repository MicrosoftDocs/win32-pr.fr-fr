---
title: Types de données WinSNMP
description: Les types de données WinSNMP standard sont définis dans l’WINSNMP. Fichier H.
ms.assetid: 20f1bbc3-5a08-4206-980d-22a794cda402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7061ade6f9b69c63ba4718d9d79bbd4d39c67b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031735"
---
# <a name="winsnmp-data-types"></a><span data-ttu-id="ff88d-103">Types de données WinSNMP</span><span class="sxs-lookup"><span data-stu-id="ff88d-103">WinSNMP Data Types</span></span>

<span data-ttu-id="ff88d-104">\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ff88d-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ff88d-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ff88d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ff88d-106">Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="ff88d-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="ff88d-107">Les types de données WinSNMP standard sont définis dans l’WINSNMP. Fichier H.</span><span class="sxs-lookup"><span data-stu-id="ff88d-107">The standard WinSNMP data types are defined in the WINSNMP.H file.</span></span>

<span data-ttu-id="ff88d-108">Notez que WinSNMP spécifie des paramètres avec le type entier long signé, **smiINT**.</span><span class="sxs-lookup"><span data-stu-id="ff88d-108">Note that WinSNMP specifies some parameters with the signed long integer type, **smiINT**.</span></span> <span data-ttu-id="ff88d-109">Ce qui permet à WinSNMP de se conformer aux éléments de données, en particulier les composants PDU, définis dans les RFC pertinentes.</span><span class="sxs-lookup"><span data-stu-id="ff88d-109">This enables WinSNMP to comply with the data elements, especially the PDU components, defined in the relevant RFCs.</span></span>

 

 