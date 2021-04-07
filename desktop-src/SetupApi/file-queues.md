---
description: Les fonctions d’installation incluent la fonctionnalité de file d’attente de fichiers.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Files d’attente de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952359"
---
# <a name="file-queues"></a><span data-ttu-id="06bb4-103">Files d’attente de fichiers</span><span class="sxs-lookup"><span data-stu-id="06bb4-103">File Queues</span></span>

<span data-ttu-id="06bb4-104">Les fonctions d’installation incluent la fonctionnalité de file d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="06bb4-104">The setup functions include file queue functionality.</span></span> <span data-ttu-id="06bb4-105">Une file d’attente de fichiers est une liste d’opérations de copie, de changement de nom et de suppression de fichiers.</span><span class="sxs-lookup"><span data-stu-id="06bb4-105">A file queue is a list of file copying, renaming, and deletion operations.</span></span> <span data-ttu-id="06bb4-106">Ces opérations peuvent être envoyées à la file d’attente dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="06bb4-106">These operations can be sent to the queue in any order.</span></span> <span data-ttu-id="06bb4-107">Lorsque la file d’attente est validée, ces opérations sont traitées comme un lot, dans l’ordre du type d’opération.</span><span class="sxs-lookup"><span data-stu-id="06bb4-107">When the queue is committed, these operations are processed as a batch, in order of the operation type.</span></span>

<span data-ttu-id="06bb4-108">Les sections suivantes expliquent ce qu’est une file d’attente et comment l’utiliser lors de la création d’une application d’installation.</span><span class="sxs-lookup"><span data-stu-id="06bb4-108">The following sections explain what a queue is and how to use it when creating a setup application.</span></span> <span data-ttu-id="06bb4-109">L’ordre dans lequel les opérations de fichiers en file d’attente sont traitées en tant que validations de file d’attente et les notifications envoyées par la file d’attente à une routine de rappel à chaque étape est également abordé.</span><span class="sxs-lookup"><span data-stu-id="06bb4-109">Also discussed is the order in which the enqueued file operations are processed as the queue commits and what notifications the queue sends to a callback routine at each stage.</span></span>

-   [<span data-ttu-id="06bb4-110">À propos des files d’attente de fichiers</span><span class="sxs-lookup"><span data-stu-id="06bb4-110">About File Queues</span></span>](about-file-queues.md)
-   [<span data-ttu-id="06bb4-111">Utilisation des files d’attente de fichiers</span><span class="sxs-lookup"><span data-stu-id="06bb4-111">Using File Queues</span></span>](using-file-queues.md)
-   [<span data-ttu-id="06bb4-112">Référence de file d’attente de fichiers</span><span class="sxs-lookup"><span data-stu-id="06bb4-112">File Queue Reference</span></span>](file-queue-reference.md)

 

 



