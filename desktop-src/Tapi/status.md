---
description: La plupart des opérations d’extraction et de définition traitent uniquement un composant d’informations. La fonction phoneGetStatus renvoie des informations d’État complètes sur un appareil téléphonique à une application.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: État (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864998"
---
# <a name="status-telephony-api"></a><span data-ttu-id="693d7-104">État (API de téléphonie)</span><span class="sxs-lookup"><span data-stu-id="693d7-104">Status (Telephony API)</span></span>

<span data-ttu-id="693d7-105">La plupart des opérations d’extraction et de définition traitent uniquement un composant d’informations.</span><span class="sxs-lookup"><span data-stu-id="693d7-105">Most of the get and set operations deal with one component of information only.</span></span> <span data-ttu-id="693d7-106">La fonction [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) renvoie des informations d’État complètes sur un appareil téléphonique à une application.</span><span class="sxs-lookup"><span data-stu-id="693d7-106">The [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) function returns complete status information about a phone device to an application.</span></span>

<span data-ttu-id="693d7-107">Comme mentionné précédemment, chaque fois qu’un élément d’état change sur le périphérique téléphonique, un message d' [**\_ État de téléphone**](phone-state.md) est envoyé à la fonction d’application.</span><span class="sxs-lookup"><span data-stu-id="693d7-107">As mentioned earlier, whenever a status item changes on the phone device, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function.</span></span> <span data-ttu-id="693d7-108">Les paramètres de ce message incluent un handle vers l’appareil téléphonique et une indication de l’élément d’État qui a changé.</span><span class="sxs-lookup"><span data-stu-id="693d7-108">This message's parameters include a handle to the phone device and an indication of the status item that changed.</span></span>

<span data-ttu-id="693d7-109">Une application peut utiliser [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) pour sélectionner les modifications d’État spécifiques pour lesquelles elle souhaite être notifiée.</span><span class="sxs-lookup"><span data-stu-id="693d7-109">An application can use [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) to select the specific status changes for which it wants to be notified.</span></span> <span data-ttu-id="693d7-110">En conséquence, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) retourne les modifications d’État pour lesquelles l’application souhaite être notifiée.</span><span class="sxs-lookup"><span data-stu-id="693d7-110">Correspondingly, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) returns the status changes for which the application wants to be notified.</span></span>

 

 



