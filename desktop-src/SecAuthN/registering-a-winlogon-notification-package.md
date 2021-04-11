---
description: Les informations sur les packages de notification Winlogon sont stockées dans le registre. Les entrées de Registre spécifient le nom du package de notification, le nom de la DLL qui implémente le package et les noms des fonctions qui gèrent les événements Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Inscription d’un package de notifications Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202718"
---
# <a name="registering-a-winlogon-notification-package"></a><span data-ttu-id="f445f-104">Inscription d’un package de notifications Winlogon</span><span class="sxs-lookup"><span data-stu-id="f445f-104">Registering a Winlogon Notification Package</span></span>

<span data-ttu-id="f445f-105">Les informations sur les packages de notification [*Winlogon*](../secgloss/w-gly.md) sont stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f445f-105">Information about [*Winlogon*](../secgloss/w-gly.md) notification packages is stored in the registry.</span></span> <span data-ttu-id="f445f-106">Les entrées de Registre spécifient le nom du package de notification, le nom de la DLL qui implémente le package et les noms des fonctions qui gèrent les événements Winlogon.</span><span class="sxs-lookup"><span data-stu-id="f445f-106">Registry entries specify the name of the notification package, the name of the DLL that implements the package, and the names of the functions that handle Winlogon events.</span></span>

<span data-ttu-id="f445f-107">Lorsque Winlogon démarre, il vérifie le registre et charge tous les packages de notification inscrits.</span><span class="sxs-lookup"><span data-stu-id="f445f-107">When Winlogon starts, it checks the registry and loads any registered notification packages.</span></span> <span data-ttu-id="f445f-108">Lorsqu’un événement se produit, Winlogon appelle la fonction de gestionnaire d’événements désignée pour chaque package.</span><span class="sxs-lookup"><span data-stu-id="f445f-108">When an event occurs, Winlogon calls the designated event handler function for each package.</span></span> <span data-ttu-id="f445f-109">Plusieurs packages de notification d’événements peuvent être inscrits sur un système.</span><span class="sxs-lookup"><span data-stu-id="f445f-109">Multiple event notification packages may be registered on a system.</span></span>

<span data-ttu-id="f445f-110">Pour inscrire votre package de notification, créez une clé de Registre nommée **Notify** en tant que sous-clé de la clé de Registre suivante et ajoutez les valeurs détaillées dans les [entrées de registre](registry-entries.md).</span><span class="sxs-lookup"><span data-stu-id="f445f-110">To register your notification package, create a registry key named **Notify** as a subkey of the following registry key and add the values detailed in [Registry Entries](registry-entries.md).</span></span>

<span data-ttu-id="f445f-111">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**</span><span class="sxs-lookup"><span data-stu-id="f445f-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Winlogon**</span></span>

 

 
