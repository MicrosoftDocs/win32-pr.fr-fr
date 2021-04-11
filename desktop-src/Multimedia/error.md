---
title: Error
description: Error
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- Fonctions de rappel AVICap, messages de notification d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f418f16ae2af15902e96927990d79a4ecac08b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029629"
---
# <a name="error"></a><span data-ttu-id="07b5e-104">Error</span><span class="sxs-lookup"><span data-stu-id="07b5e-104">Error</span></span>

<span data-ttu-id="07b5e-105">Une fenêtre de capture utilise des messages de notification d’erreur pour signaler à votre application des erreurs AVICap, telles que l’insuffisance de l’espace disque, la tentative d’écriture dans un fichier en lecture seule, l’échec de l’accès au matériel ou la suppression d’un trop grand nombre de frames.</span><span class="sxs-lookup"><span data-stu-id="07b5e-105">A capture window uses error notification messages to notify your application of AVICap errors, such as running out of disk space, attempting to write to a read-only file, failing to access hardware, or dropping too many frames.</span></span> <span data-ttu-id="07b5e-106">Le contenu d’une notification d’erreur comprend un identificateur de message et une chaîne de texte mise en forme prête à être affichée.</span><span class="sxs-lookup"><span data-stu-id="07b5e-106">The content of an error notification includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="07b5e-107">Votre application peut utiliser l’identificateur de message pour filtrer les notifications et limiter les messages à présenter à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="07b5e-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="07b5e-108">Un identificateur de message égal à zéro indique qu’une nouvelle opération démarre et que la fonction de rappel doit effacer tout message d’erreur affiché.</span><span class="sxs-lookup"><span data-stu-id="07b5e-108">A message identifier of zero indicates a new operation is starting and the callback function should clear any displayed error message.</span></span>

 

 




