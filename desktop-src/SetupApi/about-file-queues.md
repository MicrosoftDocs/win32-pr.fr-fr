---
description: Une file d’attente de fichiers est une liste d’opérations de fichiers qui sont traitées en même temps. Les opérations de fichier dans la file d’attente peuvent être des opérations de copie, de renommage ou de suppression. La file d’attente de fichiers organise les opérations de fichier par type, en créant des sous-files d’attente de copie, de renommage et de suppression.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: À propos des files d’attente de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513997"
---
# <a name="about-file-queues"></a><span data-ttu-id="f3806-105">À propos des files d’attente de fichiers</span><span class="sxs-lookup"><span data-stu-id="f3806-105">About File Queues</span></span>

<span data-ttu-id="f3806-106">Une file d’attente de fichiers est une liste d’opérations de fichiers qui sont traitées en même temps.</span><span class="sxs-lookup"><span data-stu-id="f3806-106">A file queue is a list of file operations that are processed at one time.</span></span> <span data-ttu-id="f3806-107">Les opérations de fichier dans la file d’attente peuvent être des opérations de copie, de renommage ou de suppression.</span><span class="sxs-lookup"><span data-stu-id="f3806-107">The file operations in the queue may be copy, rename, or delete operations.</span></span> <span data-ttu-id="f3806-108">La file d’attente de fichiers organise les opérations de fichier par type, en créant des sous-files d’attente de copie, de renommage et de suppression.</span><span class="sxs-lookup"><span data-stu-id="f3806-108">The file queue organizes file operations by type, creating copy, rename, and delete subqueues.</span></span>

<span data-ttu-id="f3806-109">Ces opérations peuvent être envoyées à la file d’attente dans n’importe quel ordre, et le processus de mise en file d’attente n’a pas besoin d’être contigu.</span><span class="sxs-lookup"><span data-stu-id="f3806-109">These operations may be sent to the queue in any order, and the enqueuing process need not be contiguous.</span></span> <span data-ttu-id="f3806-110">Lorsque la file d’attente est validée, la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) effectue des opérations sur les fichiers dans l’ordre du type d’opération.</span><span class="sxs-lookup"><span data-stu-id="f3806-110">When the queue is committed, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function performs file operations in order of the operation type.</span></span>

<span data-ttu-id="f3806-111">En règle générale, toutes les opérations de fichiers nécessaires pour une installation complète sont mises en file d’attente dans la file d’attente de fichiers, puis traitées dans un lot unique lorsque la file d’attente est validée.</span><span class="sxs-lookup"><span data-stu-id="f3806-111">Typically, all of the file operations necessary for an entire installation are queued to the file queue, and then processed in a single batch when the queue is committed.</span></span>

<span data-ttu-id="f3806-112">L’un des avantages de la mise en file d’attente des opérations de fichiers sur l’installation de fichiers à partir d’un fichier INF est que vous pouvez simplifier le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="f3806-112">One advantage of queuing file operations over installing files section-by-section from an INF file is that you can streamline the installation process.</span></span> <span data-ttu-id="f3806-113">Au lieu d’avoir à obtenir des informations de l’utilisateur pour chaque section à installer, vous pouvez obtenir des informations d’installation auprès de l’utilisateur pour tous les fichiers à installer lors de la création de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f3806-113">Instead of having to obtain information from the user for each section to be installed, you can obtain installation information from the user for all the files to be installed while building the queue.</span></span> <span data-ttu-id="f3806-114">Cela permet à l’utilisateur d’effectuer d’autres activités, tandis que les opérations de copie gourmandes en temps sont traitées par la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) .</span><span class="sxs-lookup"><span data-stu-id="f3806-114">This frees the user to pursue other activities while the time-intensive copy operations are processed by the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function.</span></span>

<span data-ttu-id="f3806-115">Un autre avantage des files d’attente de fichiers est que vous pouvez suivre la progression de l’installation dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="f3806-115">Another advantage of file queues is that you can track the progress of the installation as a whole.</span></span> <span data-ttu-id="f3806-116">Lors de l’installation de la section par section à partir d’un fichier INF, les indicateurs de progression tels que les barres de progression peuvent suivre uniquement la section INF actuelle.</span><span class="sxs-lookup"><span data-stu-id="f3806-116">When installing section-by-section from an INF file, progress indicators such as progress bars can track only the current INF section.</span></span> <span data-ttu-id="f3806-117">Lorsque la section suivante est installée, la barre de progression recommence.</span><span class="sxs-lookup"><span data-stu-id="f3806-117">When the next section is installed, the progress bar starts over.</span></span> <span data-ttu-id="f3806-118">Avec une file d’attente, le nombre total de fichiers à traiter pendant toute l’installation est connu avant la validation de la file d’attente, et par conséquent, une barre de progression peut être générée pour effectuer le suivi de l’ensemble de l’installation.</span><span class="sxs-lookup"><span data-stu-id="f3806-118">With a queue, the total number of files to be processed during the entire installation is known before the queue is committed, and thus, a progress bar can be generated to track the entire installation.</span></span>

<span data-ttu-id="f3806-119">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3806-119">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f3806-120">Ordre de validation des files d’attente</span><span class="sxs-lookup"><span data-stu-id="f3806-120">Order of Queue Commitment</span></span>](order-of-queue-commitment.md)
-   [<span data-ttu-id="f3806-121">Notifications de file d’attente</span><span class="sxs-lookup"><span data-stu-id="f3806-121">Queue Notifications</span></span>](queue-notifications.md)

 

 



