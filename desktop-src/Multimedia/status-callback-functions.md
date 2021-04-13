---
title: Fonctions de rappel d’État
description: Fonctions de rappel d’État
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Fonctions de rappel AVICap, état
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379942"
---
# <a name="status-callback-functions"></a><span data-ttu-id="78552-104">Fonctions de rappel d’État</span><span class="sxs-lookup"><span data-stu-id="78552-104">Status Callback Functions</span></span>

<span data-ttu-id="78552-105">Une fenêtre de capture peut envoyer des messages à la fonction de rappel d’état lors de la capture de la vidéo sur le disque ou lors d’autres opérations de longue durée pour notifier votre application de la progression d’une opération.</span><span class="sxs-lookup"><span data-stu-id="78552-105">A capture window can send messages to the status callback function while capturing video to disk or during other lengthy operations to notify your application of the progress of an operation.</span></span> <span data-ttu-id="78552-106">Les informations d’État incluent un identificateur de message et une chaîne de texte mise en forme prête pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="78552-106">The status information includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="78552-107">Votre application peut utiliser l’identificateur de message pour filtrer les notifications et limiter les messages à présenter à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78552-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="78552-108">Pendant les opérations de capture, le premier message envoyé à la fonction de rappel est toujours IDS \_ Cap \_ Begin et le dernier est toujours ID \_ Cap \_ end.</span><span class="sxs-lookup"><span data-stu-id="78552-108">During capture operations, the first message sent to the callback function is always IDS\_CAP\_BEGIN and the last is always IDS\_CAP\_END.</span></span> <span data-ttu-id="78552-109">Un identificateur de message égal à zéro indique qu’une nouvelle opération démarre et que la fonction de rappel doit effacer l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="78552-109">A message identifier of zero indicates a new operation is starting and the callback function should clear the current status.</span></span>

 

 




