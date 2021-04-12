---
title: Indicateur Notify
description: Indicateur Notify
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- Indicateur de MCI_NOTIFY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381915"
---
# <a name="the-notify-flag"></a><span data-ttu-id="4e26a-104">Indicateur Notify</span><span class="sxs-lookup"><span data-stu-id="4e26a-104">The Notify Flag</span></span>

<span data-ttu-id="4e26a-105">L’indicateur « Notify » (MCI \_ Notify) indique à l’appareil de poster un message [**MCINOTIFY mm**](mm-mcinotify.md) lorsque l’appareil termine une action.</span><span class="sxs-lookup"><span data-stu-id="4e26a-105">The "notify" (MCI\_NOTIFY) flag directs the device to post an [**MM MCINOTIFY**](mm-mcinotify.md) message when the device completes an action.</span></span> <span data-ttu-id="4e26a-106">Votre application doit avoir une procédure de fenêtre pour traiter le \_ message mm MCINOTIFY pour que la notification ait un effet.</span><span class="sxs-lookup"><span data-stu-id="4e26a-106">Your application must have a window procedure to process the MM\_MCINOTIFY message for notification to have any effect.</span></span> <span data-ttu-id="4e26a-107">Un \_ message mm MCINOTIFY indique que le traitement d’une commande est terminé, mais il n’indique pas si la commande a été exécutée correctement, a échoué ou a été remplacée ou abandonnée.</span><span class="sxs-lookup"><span data-stu-id="4e26a-107">An MM\_MCINOTIFY message indicates that the processing of a command has completed, but it does not indicate whether the command was completed successfully, failed, or was superseded or aborted.</span></span>

<span data-ttu-id="4e26a-108">L’application spécifie le handle vers la fenêtre de destination pour le message lorsqu’il émet une commande.</span><span class="sxs-lookup"><span data-stu-id="4e26a-108">The application specifies the handle to the destination window for the message when it issues a command.</span></span> <span data-ttu-id="4e26a-109">Dans l’interface de chaîne de commande, ce descripteur est le dernier paramètre de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4e26a-109">In the command-string interface, this handle is the last parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="4e26a-110">Dans l’interface de message de commande, le descripteur est spécifié dans le mot de poids faible du membre **dwCallBack** de la structure envoyée avec le message de commande.</span><span class="sxs-lookup"><span data-stu-id="4e26a-110">In the command-message interface, the handle is specified in the low-order word of the **dwCallBack** member of the structure sent with the command message.</span></span> <span data-ttu-id="4e26a-111">(Chaque structure associée à un message de commande contient ce membre.)</span><span class="sxs-lookup"><span data-stu-id="4e26a-111">(Every structure associated with a command message contains this member.)</span></span>

 

 