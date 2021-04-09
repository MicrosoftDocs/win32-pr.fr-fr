---
description: Le routeur multifournisseur (MPR) appelle NPGetCaps pour déterminer à quel moment les fournisseurs de réseau démarrent (nIndex est défini sur WNNC \_ Start).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Remplacement de l’intervalle de délai d’attente MPR par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952582"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a><span data-ttu-id="47a10-103">Remplacement de l’intervalle de délai d’attente MPR par défaut</span><span class="sxs-lookup"><span data-stu-id="47a10-103">Overriding the Default MPR Time-out Interval</span></span>

<span data-ttu-id="47a10-104">Le [*routeur multifournisseur*](../secgloss/m-gly.md) (MPR) appelle [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) pour déterminer à quel moment les fournisseurs de réseau démarrent (*nIndex* est défini sur WNNC \_ Start).</span><span class="sxs-lookup"><span data-stu-id="47a10-104">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) calls [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) to find out when the network providers will start (*nIndex* is set to WNNC\_START).</span></span> <span data-ttu-id="47a10-105">Le MPR attend ensuite le délai d’expiration le plus long spécifié par tous les fournisseurs de réseau avant de présenter le réseau consolidé à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="47a10-105">The MPR then waits for the longest time-out period specified by all network providers before it presents the consolidated network to the user.</span></span> <span data-ttu-id="47a10-106">Si l’un des fournisseurs de réseau ne sait pas au démarrage, MPR utilise un délai d’expiration par défaut de 60 secondes pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="47a10-106">If one of the network providers does not know when it will start, MPR uses a default time-out of 60 seconds for that provider.</span></span>

<span data-ttu-id="47a10-107">Si nécessaire, l’administrateur peut remplacer le délai d’expiration par défaut en créant le délai d’attente de Registre **\_ DWORD reg** suivant, où *n* est l’intervalle de délai d’attente en millisecondes :</span><span class="sxs-lookup"><span data-stu-id="47a10-107">If necessary, the administrator can override the default time-out by creating the following **REG\_DWORD** registry time-out, where *n* is the time-out interval in milliseconds:</span></span>

<span data-ttu-id="47a10-108">**HKEY \_ \_** Contrôle CurrentControlSet du système de l’ordinateur local \\  \\  \\  \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*</span><span class="sxs-lookup"><span data-stu-id="47a10-108">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**RestoreTimeout** = *n*</span></span>

<span data-ttu-id="47a10-109">Le pseudo-code suivant montre le déroulement logique complet pour la gestion du délai d’attente par le MPR.</span><span class="sxs-lookup"><span data-stu-id="47a10-109">The following pseudocode shows the complete logic flow for time-out handling by the MPR.</span></span>


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
