---
description: Les messages sont utilisés pour notifier l’application d’événements asynchrones. Tous ces messages sont envoyés à l’application via le mécanisme de notification de message que l’application a spécifiée dans lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Messages TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520077"
---
# <a name="tapi-messages"></a><span data-ttu-id="05c72-104">Messages TAPI</span><span class="sxs-lookup"><span data-stu-id="05c72-104">TAPI Messages</span></span>

<span data-ttu-id="05c72-105">Les messages sont utilisés pour notifier l’application d’événements asynchrones.</span><span class="sxs-lookup"><span data-stu-id="05c72-105">Messages are used to notify the application of asynchronous events.</span></span> <span data-ttu-id="05c72-106">Tous ces messages sont envoyés à l’application via le mécanisme de notification de message que l’application a spécifiée dans [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="05c72-106">All of these messages are sent to the application through the message notification mechanism that the application specified in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="05c72-107">Le message contient toujours un handle vers l’objet approprié (téléphone, ligne ou appel), que l’application peut utiliser pour déterminer le type de message.</span><span class="sxs-lookup"><span data-stu-id="05c72-107">The message always contains a handle to the relevant object (phone, line, or call), which the application can use to determine the message type.</span></span>

<span data-ttu-id="05c72-108">Certains messages sont utilisés pour notifier l’application d’une modification de l’état d’un objet.</span><span class="sxs-lookup"><span data-stu-id="05c72-108">Certain messages are used to notify the application about a change in an object's status.</span></span> <span data-ttu-id="05c72-109">Ces messages fournissent le descripteur d’objet et donnent une indication sur l’élément d’état modifié.</span><span class="sxs-lookup"><span data-stu-id="05c72-109">These messages provide the object handle and give an indication of which status item has changed.</span></span> <span data-ttu-id="05c72-110">L’application peut appeler la fonction « obtenir l’État » appropriée de l’objet pour obtenir l’état complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="05c72-110">The application can call the appropriate "get status" function of the object to obtain the object's full status.</span></span>

<span data-ttu-id="05c72-111">Lorsqu’un événement se produit, les messages peuvent être envoyés à zéro, une ou plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="05c72-111">When an event occurs, messages can be sent to zero, one, or more applications.</span></span> <span data-ttu-id="05c72-112">Les applications cibles pour un message sont déterminées par différents facteurs, notamment la signification du message, le privilège de l’application à l’objet, si l’application a initié ou non la demande pour laquelle le message est un résultat direct, et le masquage de message défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="05c72-112">The target applications for a message are determined by a number of different factors including the meaning of the message, the application's privilege to the object, whether or not the application initiated the request for which the message is a direct result, and the message masking that has been set by the application.</span></span> <span data-ttu-id="05c72-113">Notez les points suivants sur les messages :</span><span class="sxs-lookup"><span data-stu-id="05c72-113">Note the following points about messages:</span></span>

-   <span data-ttu-id="05c72-114">Les messages de réponse asynchrones sont envoyés à l’application à l’origine de la demande et ne peuvent pas être masqués.</span><span class="sxs-lookup"><span data-stu-id="05c72-114">Asynchronous reply messages are only sent to the application that originated the request and cannot be masked.</span></span>
-   <span data-ttu-id="05c72-115">Les messages qui signalent l’achèvement de la génération de chiffres ou de tonalités, ou la collecte de chiffres, sont envoyés uniquement à l’application qui a demandé la génération de chiffres ou de tonalités.</span><span class="sxs-lookup"><span data-stu-id="05c72-115">Messages that signal the completion of digit or tone generation or the gathering of digits are only sent to the application that requested the digit or tone generation.</span></span>
-   <span data-ttu-id="05c72-116">Les messages qui indiquent des changements d’état de ligne ou d’adresse sont envoyés à toutes les applications qui ont ouvert la ligne, tant que le message a été activé par le biais de [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="05c72-116">Messages that indicate line or address state changes are sent to all applications that have opened the line, so long as the message has been enabled through [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span>
-   <span data-ttu-id="05c72-117">Les messages qui indiquent l’état de l’appel et les modifications des informations d’appel sont envoyés à toutes les applications qui ont un handle vers l’appel.</span><span class="sxs-lookup"><span data-stu-id="05c72-117">Messages that indicate call state and call information changes are sent to all applications that have a handle to the call.</span></span>
-   <span data-ttu-id="05c72-118">Les messages signalant une détection de chiffres, une détection de tonalité ou une détection de type de média sont envoyés aux applications qui ont demandé la surveillance de cet événement.</span><span class="sxs-lookup"><span data-stu-id="05c72-118">Messages that signal a digit detection, tone detection, or media type detection are sent to the applications that requested monitoring of that event.</span></span>

<span data-ttu-id="05c72-119">Cette section contient des informations de référence sur les messages TAPI suivants :</span><span class="sxs-lookup"><span data-stu-id="05c72-119">This section contains the reference information for the following TAPI messages:</span></span>

-   [<span data-ttu-id="05c72-120">Messages de téléphonie assistés</span><span class="sxs-lookup"><span data-stu-id="05c72-120">Assisted Telephony Messages</span></span>](assisted-telephony-messages.md)
-   [<span data-ttu-id="05c72-121">Messages du centre d’appels</span><span class="sxs-lookup"><span data-stu-id="05c72-121">Call Center Messages</span></span>](call-center-messages.md)
-   [<span data-ttu-id="05c72-122">Messages d’erreur mis en forme</span><span class="sxs-lookup"><span data-stu-id="05c72-122">Formatted Error Messages</span></span>](formatted-error-messages.md)
-   [<span data-ttu-id="05c72-123">Messages du périphérique de ligne</span><span class="sxs-lookup"><span data-stu-id="05c72-123">Line Device Messages</span></span>](line-device-messages.md)
-   [<span data-ttu-id="05c72-124">Messages de l’appareil téléphonique</span><span class="sxs-lookup"><span data-stu-id="05c72-124">Phone Device Messages</span></span>](phone-device-messages.md)

 

 



