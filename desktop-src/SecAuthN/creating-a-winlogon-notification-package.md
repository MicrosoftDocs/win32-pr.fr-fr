---
description: Un package de notification Winlogon est une DLL qui exporte les fonctions qui gèrent les événements Winlogon. Par exemple, lorsqu’un utilisateur se connecte au système, Winlogon appelle la fonction de gestionnaire d’événements Logon du package de notification pour fournir des informations sur l’événement.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Création d’un package de notifications Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520557"
---
# <a name="creating-a-winlogon-notification-package"></a><span data-ttu-id="ed5ec-104">Création d’un package de notifications Winlogon</span><span class="sxs-lookup"><span data-stu-id="ed5ec-104">Creating a Winlogon Notification Package</span></span>

<span data-ttu-id="ed5ec-105">Un package de notification [*Winlogon*](/windows/desktop/SecGloss/w-gly) est une dll qui exporte les fonctions qui gèrent les événements Winlogon.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-105">A [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="ed5ec-106">Par exemple, lorsqu’un utilisateur se connecte au système, Winlogon appelle la fonction de gestionnaire d’événements Logon du package de notification pour fournir des informations sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-106">For example, when a user logs onto the system, Winlogon calls each notification package's logon event handler function to provide information about the event.</span></span>

<span data-ttu-id="ed5ec-107">Les noms des fonctions de gestionnaire d’événements implémentées dans un package de notification sont laissés au développeur. Winlogon vérifie le registre pour obtenir les noms des fonctions de gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-107">The names of the event handler functions implemented in a notification package are left up to the developer; Winlogon checks the registry to obtain the names of the event handler functions.</span></span> <span data-ttu-id="ed5ec-108">Par exemple, un package de notification peut implémenter la fonction de gestionnaire d’événements LOGON, `WLEventLogon` tandis qu’un autre peut utiliser `HandleLogonEvent` .</span><span class="sxs-lookup"><span data-stu-id="ed5ec-108">For example, one notification package might implement the logon event handler function as `WLEventLogon` whereas another might use `HandleLogonEvent`.</span></span>

<span data-ttu-id="ed5ec-109">Vous n’avez pas à implémenter et à inscrire des gestionnaires d’événements pour chaque événement Winlogon, uniquement pour les événements qui sont utiles à votre application.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-109">You do not have to implement and register event handlers for every Winlogon event, only for events that are useful to your application.</span></span> <span data-ttu-id="ed5ec-110">Chaque fonction de gestionnaire d’événements doit utiliser le prototype de fonction décrit dans [prototype de fonction du gestionnaire d’événements](event-handler-function-prototype.md).</span><span class="sxs-lookup"><span data-stu-id="ed5ec-110">Each event handler function must use the function prototype described in [Event Handler Function Prototype](event-handler-function-prototype.md).</span></span> <span data-ttu-id="ed5ec-111">Ce prototype a un seul paramètre : une structure d' [**\_ \_ informations de notification wlx**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) qui contient des détails sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-111">This prototype has a single parameter: a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains details about the event.</span></span>

<span data-ttu-id="ed5ec-112">Winlogon ignore la sortie des fonctions de gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-112">Winlogon ignores the output of event handler functions.</span></span> <span data-ttu-id="ed5ec-113">Si la gestion d’un événement nécessite l’interaction avec Winlogon, utilisez les [fonctions de prise en charge de Winlogon](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ed5ec-113">If handling an event requires interacting with Winlogon, use the [Winlogon Support Functions](authentication-functions.md).</span></span>

<span data-ttu-id="ed5ec-114">Pour utiliser votre package de notification Winlogon, la DLL doit être copiée dans le dossier% SystemRoot% \\ system32, et une mise à jour du registre doit être effectuée pour le package de notification.</span><span class="sxs-lookup"><span data-stu-id="ed5ec-114">To use your Winlogon notification package, the DLL must be copied to the %SystemRoot%\\system32 folder, and a registry update must be made for the notification package.</span></span> <span data-ttu-id="ed5ec-115">Pour plus d’informations sur la mise à jour du Registre, consultez [inscription d’un package de notification Winlogon](registering-a-winlogon-notification-package.md).</span><span class="sxs-lookup"><span data-stu-id="ed5ec-115">For information about the registry update, see [Registering a Winlogon Notification Package](registering-a-winlogon-notification-package.md).</span></span>

 

 
