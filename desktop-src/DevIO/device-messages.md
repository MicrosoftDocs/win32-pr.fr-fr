---
description: Les messages de l’appareil sont des messages système qui notifient les applications et d’autres fonctionnalités des événements de modification d’appareil.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Messages des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536950"
---
# <a name="device-messages"></a><span data-ttu-id="2022f-103">Messages des appareils</span><span class="sxs-lookup"><span data-stu-id="2022f-103">Device Messages</span></span>

<span data-ttu-id="2022f-104">Les messages de l’appareil sont des messages système qui notifient les applications et d’autres fonctionnalités des événements de modification d’appareil.</span><span class="sxs-lookup"><span data-stu-id="2022f-104">Device messages are system messages that notify applications and other features of device change events.</span></span> <span data-ttu-id="2022f-105">Ces événements se produisent lorsque le système détecte une modification apportée au matériel système, par exemple lorsque l’utilisateur ancre et déconnecte un ordinateur portable, ou insère ou supprime un appareil tel qu’une carte PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="2022f-105">These events occur whenever the system detects a change to the system hardware, such as when the user docks and undocks a laptop computer, or inserts or removes a device such as a PCMCIA card.</span></span> <span data-ttu-id="2022f-106">Les événements d’appareil peuvent se produire lorsque le système est en cours d’exécution ou lorsque le système reprend l’opération une fois temporairement suspendu.</span><span class="sxs-lookup"><span data-stu-id="2022f-106">Device events can occur while the system is running or when the system resumes operation after temporarily being suspended.</span></span>

<span data-ttu-id="2022f-107">Pour garantir que les applications ne perdent pas de données lorsque les appareils deviennent indisponibles, le système surveille la configuration matérielle et envoie des messages d’appareil aux applications pour les notifier des modifications et leur permet de préparer les modifications avant qu’elles ne se produisent.</span><span class="sxs-lookup"><span data-stu-id="2022f-107">To help ensure that applications do not lose data when devices become unavailable, the system monitors the hardware configuration and sends device messages to the applications to notify them of the changes and to give them the opportunity to prepare for the changes before they occur.</span></span>

<span data-ttu-id="2022f-108">Pour chaque événement d’appareil, le système diffuse un message [**WM \_ DEVICECHANGE**](wm-devicechange.md) à toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="2022f-108">For each device event, the system broadcasts a [**WM\_DEVICECHANGE**](wm-devicechange.md) message to all applications.</span></span> <span data-ttu-id="2022f-109">Dans ce message, le paramètre *wParam* identifie le [type d’événement](device-event-types.md) de l’appareil et le paramètre *lParam* est un pointeur vers des données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="2022f-109">In this message, the *wParam* parameter identifies the [device event type](device-event-types.md) and the *lParam* parameter is a pointer to event-specific data.</span></span>

 

 



