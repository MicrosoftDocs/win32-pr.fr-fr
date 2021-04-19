---
description: Décrit les concepts d’e/s de base.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Concepts d’e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536851"
---
# <a name="io-concepts"></a><span data-ttu-id="78d64-103">Concepts d’e/s</span><span class="sxs-lookup"><span data-stu-id="78d64-103">I/O Concepts</span></span>

<span data-ttu-id="78d64-104">Les concepts d’e/s suivants sont décrits dans cette section.</span><span class="sxs-lookup"><span data-stu-id="78d64-104">The following I/O concepts are described in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="78d64-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="78d64-105">In this section</span></span>



| <span data-ttu-id="78d64-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="78d64-106">Topic</span></span>                                                                               | <span data-ttu-id="78d64-107">Description</span><span class="sxs-lookup"><span data-stu-id="78d64-107">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78d64-108">Mise en mémoire tampon des fichiers</span><span class="sxs-lookup"><span data-stu-id="78d64-108">File Buffering</span></span>](file-buffering.md)<br/>                                     | <span data-ttu-id="78d64-109">Décrit les éléments à prendre en considération pour le contrôle d’application de la mise en mémoire tampon des fichiers, également appelée entrée/sortie (e/s) de fichiers non mis en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="78d64-109">Describes considerations for application control of file buffering, also known as unbuffered file input/output (I/O).</span></span><br/>                                    |
| [<span data-ttu-id="78d64-110">Mise en cache des fichiers</span><span class="sxs-lookup"><span data-stu-id="78d64-110">File Caching</span></span>](file-caching.md)<br/>                                         | <span data-ttu-id="78d64-111">Windows met en cache les données de fichier qui sont lues à partir des disques et écrites sur les disques.</span><span class="sxs-lookup"><span data-stu-id="78d64-111">Windows caches file data that is read from disks and written to disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="78d64-112">E/s synchrones et asynchrones</span><span class="sxs-lookup"><span data-stu-id="78d64-112">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)<br/> | <span data-ttu-id="78d64-113">Il existe deux types de synchronisation d’entrée/sortie (e/s) : e/s synchrone et e/s asynchrones.</span><span class="sxs-lookup"><span data-stu-id="78d64-113">There are two types of input/output (I/O) synchronization: synchronous I/O and asynchronous I/O.</span></span> <span data-ttu-id="78d64-114">Les e/s asynchrones sont également appelées e/s avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="78d64-114">Asynchronous I/O is also referred to as overlapped I/O.</span></span><br/> |
| [<span data-ttu-id="78d64-115">Annulation d’opérations d’e/s en attente</span><span class="sxs-lookup"><span data-stu-id="78d64-115">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)<br/> | <span data-ttu-id="78d64-116">Le fait de permettre aux utilisateurs d’annuler les demandes d’e/s qui sont lentes ou bloquées peut améliorer la convivialité et la robustesse de votre application.</span><span class="sxs-lookup"><span data-stu-id="78d64-116">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span><br/>                             |
| [<span data-ttu-id="78d64-117">E/s alertables</span><span class="sxs-lookup"><span data-stu-id="78d64-117">Alertable I/O</span></span>](alertable-i-o.md)<br/>                                       | <span data-ttu-id="78d64-118">Les e/s alertables sont la méthode par laquelle les threads d’application traitent les demandes d’e/s asynchrones uniquement lorsqu’elles sont dans un État alerté.</span><span class="sxs-lookup"><span data-stu-id="78d64-118">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span><br/>                     |
| [<span data-ttu-id="78d64-119">Ports de terminaison d’e/s</span><span class="sxs-lookup"><span data-stu-id="78d64-119">I/O Completion Ports</span></span>](i-o-completion-ports.md)<br/>                         | <span data-ttu-id="78d64-120">Les ports de terminaison d’e/s fournissent un modèle de thread efficace pour traiter plusieurs demandes d’e/s asynchrones sur un système multiprocesseur.</span><span class="sxs-lookup"><span data-stu-id="78d64-120">I/O completion ports provide an efficient threading model for processing multiple asynchronous I/O requests on a multiprocessor system.</span></span><br/>                  |



 

 

 




