---
description: L’infrastructure homologue ne garantit pas l’ordre de réception et de traitement des enregistrements.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Dépendances d’enregistrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529838"
---
# <a name="record-dependencies"></a><span data-ttu-id="faad8-103">Dépendances d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="faad8-103">Record Dependencies</span></span>

<span data-ttu-id="faad8-104">L’infrastructure homologue ne garantit pas l’ordre de réception et de traitement des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="faad8-104">The Peer Infrastructure does not guarantee the order for receiving and processing records.</span></span> <span data-ttu-id="faad8-105">Si votre application a des dépendances d’enregistrement, ce qui signifie que le traitement ou la validation d’un enregistrement repose sur un autre enregistrement, votre application doit être en mesure de gérer les situations où les enregistrements peuvent être reçus dans un ordre arbitraire et imprévisible.</span><span class="sxs-lookup"><span data-stu-id="faad8-105">If your application has record dependencies, which means that the processing or validation of one record relies on another record, then your application must be able to handle situations when records might be received in an arbitrary and unpredictable order.</span></span> <span data-ttu-id="faad8-106">Par exemple, une application de conversation peut avoir deux types d’enregistrements : un enregistrement qui contient des informations sur un utilisateur spécifique et un enregistrement qui contient un message de conversation qui fait référence à l’enregistrement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="faad8-106">For example, a chat application may have two types of records: a record that contains information about a specific user, and a record that contains a chat message that refers to the user record.</span></span>

<span data-ttu-id="faad8-107">Une application doit être en mesure de gérer la situation lorsqu’un enregistrement de message de conversation est reçu avant l’enregistrement de l’utilisateur pour le message de conversation.</span><span class="sxs-lookup"><span data-stu-id="faad8-107">An application must be able to handle the situation when a chat message record is received before the user record for the chat message.</span></span> <span data-ttu-id="faad8-108">Une manière de gérer la situation consiste à attendre l’enregistrement de l’utilisateur à l’aide d’une liste de mise **en veille**, ou d’un cache et d’un minuteur.</span><span class="sxs-lookup"><span data-stu-id="faad8-108">One way to handle the situation is to wait for the user record by using a **stand-by list**, or a cache and timer.</span></span> <span data-ttu-id="faad8-109">L’application peut examiner périodiquement chaque enregistrement de la liste ou du cache, puis gérer la situation lors de la réception de l’enregistrement utilisateur requis.</span><span class="sxs-lookup"><span data-stu-id="faad8-109">The application can periodically examine each record in the list or cache, and then handle the situation when the required user record is received.</span></span>

<span data-ttu-id="faad8-110">Pour gérer les dépendances d’enregistrement, une application bien conçue se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="faad8-110">To handle record dependencies, a well-designed application consists of the following:</span></span>

-   <span data-ttu-id="faad8-111">Recherche toujours les dépendances d’enregistrement avant d’effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="faad8-111">Always checks for record dependencies before performing an action.</span></span>
-   <span data-ttu-id="faad8-112">Anticipe les conditions qui peuvent se produire lorsque des enregistrements sont reçus dans un ordre inattendu, puis gère la situation.</span><span class="sxs-lookup"><span data-stu-id="faad8-112">Anticipates conditions that might occur when records are received in an unexpected order, and then handles the situation.</span></span>

 

 



