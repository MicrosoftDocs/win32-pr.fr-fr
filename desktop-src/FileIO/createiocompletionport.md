---
description: Crée un port de terminaison d’entrée/sortie (e/s) et l’associe à un handle de fichier spécifié, ou crée un port de terminaison d’e/s qui n’est pas encore associé à un descripteur de fichier, ce qui permet une association à un moment ultérieur.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Fonction CreateIoCompletionPort (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518506"
---
# <a name="createiocompletionport-function"></a><span data-ttu-id="05550-103">CreateIoCompletionPort, fonction</span><span class="sxs-lookup"><span data-stu-id="05550-103">CreateIoCompletionPort function</span></span>

<span data-ttu-id="05550-104">Crée un port de terminaison d’entrée/sortie (e/s) et l’associe à un handle de fichier spécifié, ou crée un port de terminaison d’e/s qui n’est pas encore associé à un descripteur de fichier, ce qui permet une association à un moment ultérieur.</span><span class="sxs-lookup"><span data-stu-id="05550-104">Creates an input/output (I/O) completion port and associates it with a specified file handle, or creates an I/O completion port that is not yet associated with a file handle, allowing association at a later time.</span></span>

<span data-ttu-id="05550-105">L’Association d’une instance d’un descripteur de fichier ouvert à un port de terminaison d’e/s permet à un processus de recevoir une notification de la fin des opérations d’e/s asynchrones impliquant ce descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="05550-105">Associating an instance of an opened file handle with an I/O completion port allows a process to receive notification of the completion of asynchronous I/O operations involving that file handle.</span></span>

> [!Note]
>
> <span data-ttu-id="05550-106">Le terme *descripteur de fichier* utilisé ici fait référence à une abstraction système qui représente un point de terminaison d’e/s avec chevauchement, et non un fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="05550-106">The term *file handle* as used here refers to a system abstraction that represents an overlapped I/O endpoint, not only a file on disk.</span></span> <span data-ttu-id="05550-107">Tout objet système qui prend en charge les e/s avec chevauchement, telles que les points de terminaison réseau, les sockets TCP, les canaux nommés et les emplacements de messagerie, peut être utilisé comme descripteurs de fichiers.</span><span class="sxs-lookup"><span data-stu-id="05550-107">Any system objects that support overlapped I/O such as network endpoints, TCP sockets, named pipes, and mail slots can be used as file handles.</span></span> <span data-ttu-id="05550-108">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="05550-108">For additional information, see the Remarks section.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="05550-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05550-109">Syntax</span></span>


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a><span data-ttu-id="05550-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05550-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05550-111">*FileHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05550-111">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05550-112">Descripteur de fichier ouvert ou **\_ \_ valeur de handle non valide**.</span><span class="sxs-lookup"><span data-stu-id="05550-112">An open file handle or **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="05550-113">Le handle doit être un objet qui prend en charge les e/s avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="05550-113">The handle must be to an object that supports overlapped I/O.</span></span>

<span data-ttu-id="05550-114">Si un handle est fourni, il doit avoir été ouvert pour une exécution d’e/s avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="05550-114">If a handle is provided, it has to have been opened for overlapped I/O completion.</span></span> <span data-ttu-id="05550-115">Par exemple, vous devez spécifier l’indicateur de **\_ \_ chevauchement** de l’indicateur de fichier lors de l’utilisation de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour obtenir le descripteur.</span><span class="sxs-lookup"><span data-stu-id="05550-115">For example, you must specify the **FILE\_FLAG\_OVERLAPPED** flag when using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function to obtain the handle.</span></span>

<span data-ttu-id="05550-116">Si **une \_ \_ valeur de handle non valide** est spécifiée, la fonction crée un port de terminaison d’e/s sans l’associer à un descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="05550-116">If **INVALID\_HANDLE\_VALUE** is specified, the function creates an I/O completion port without associating it with a file handle.</span></span> <span data-ttu-id="05550-117">Dans ce cas, le paramètre *ExistingCompletionPort* doit avoir la **valeur null** et le paramètre *CompletionKey* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="05550-117">In this case, the *ExistingCompletionPort* parameter must be **NULL** and the *CompletionKey* parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="05550-118">*ExistingCompletionPort* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="05550-118">*ExistingCompletionPort* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="05550-119">Handle vers un port de terminaison d’e/s existant ou **null**.</span><span class="sxs-lookup"><span data-stu-id="05550-119">A handle to an existing I/O completion port or **NULL**.</span></span>

<span data-ttu-id="05550-120">Si ce paramètre spécifie un port de terminaison d’e/s existant, la fonction l’associe au handle spécifié par le paramètre *FileHandle* .</span><span class="sxs-lookup"><span data-stu-id="05550-120">If this parameter specifies an existing I/O completion port, the function associates it with the handle specified by the *FileHandle* parameter.</span></span> <span data-ttu-id="05550-121">La fonction retourne le handle du port de terminaison d’e/s existant en cas de réussite ; il ne crée pas de nouveau port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="05550-121">The function returns the handle of the existing I/O completion port if successful; it does not create a new I/O completion port.</span></span>

<span data-ttu-id="05550-122">Si ce paramètre a la **valeur null**, la fonction crée un nouveau port de terminaison d’e/s et, si le paramètre *FileHandle* est valide, l’associe au nouveau port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="05550-122">If this parameter is **NULL**, the function creates a new I/O completion port and, if the *FileHandle* parameter is valid, associates it with the new I/O completion port.</span></span> <span data-ttu-id="05550-123">Sinon, aucune association de handles de fichiers ne se produit.</span><span class="sxs-lookup"><span data-stu-id="05550-123">Otherwise no file handle association occurs.</span></span> <span data-ttu-id="05550-124">En cas de réussite, la fonction retourne le handle au nouveau port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="05550-124">The function returns the handle to the new I/O completion port if successful.</span></span>

</dd> <dt>

<span data-ttu-id="05550-125">*CompletionKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05550-125">*CompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05550-126">Clé de fin définie par l’utilisateur par handle qui est incluse dans chaque paquet d’achèvement d’e/s pour le handle de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="05550-126">The per-handle user-defined completion key that is included in every I/O completion packet for the specified file handle.</span></span> <span data-ttu-id="05550-127">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="05550-127">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="05550-128">*NumberOfConcurrentThreads* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05550-128">*NumberOfConcurrentThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05550-129">Nombre maximal de threads que le système d’exploitation peut autoriser à traiter simultanément les paquets de fin d’exécution d’e/s pour le port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="05550-129">The maximum number of threads that the operating system can allow to concurrently process I/O completion packets for the I/O completion port.</span></span> <span data-ttu-id="05550-130">Ce paramètre est ignoré si le paramètre *ExistingCompletionPort* n’a pas la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="05550-130">This parameter is ignored if the *ExistingCompletionPort* parameter is not **NULL**.</span></span>

<span data-ttu-id="05550-131">Si ce paramètre est égal à zéro, le système autorise le nombre de threads en cours d’exécution simultanément, car il y a des processeurs dans le système.</span><span class="sxs-lookup"><span data-stu-id="05550-131">If this parameter is zero, the system allows as many concurrently running threads as there are processors in the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05550-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05550-132">Return value</span></span>

<span data-ttu-id="05550-133">Si la fonction aboutit, la valeur de retour est le descripteur d’un port de terminaison d’e/s :</span><span class="sxs-lookup"><span data-stu-id="05550-133">If the function succeeds, the return value is the handle to an I/O completion port:</span></span>

-   <span data-ttu-id="05550-134">Si le paramètre *ExistingCompletionPort* a la valeur **null**, la valeur de retour est un nouveau handle.</span><span class="sxs-lookup"><span data-stu-id="05550-134">If the *ExistingCompletionPort* parameter was **NULL**, the return value is a new handle.</span></span>

-   <span data-ttu-id="05550-135">Si le paramètre *ExistingCompletionPort* était un handle de port de terminaison d’e/s valide, la valeur de retour est le même handle.</span><span class="sxs-lookup"><span data-stu-id="05550-135">If the *ExistingCompletionPort* parameter was a valid I/O completion port handle, the return value is that same handle.</span></span>

-   <span data-ttu-id="05550-136">Si le paramètre *FileHandle* était un handle valide, ce descripteur de fichier est désormais associé au port de terminaison d’e/s retourné.</span><span class="sxs-lookup"><span data-stu-id="05550-136">If the *FileHandle* parameter was a valid handle, that file handle is now associated with the returned I/O completion port.</span></span>

<span data-ttu-id="05550-137">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="05550-137">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="05550-138">Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="05550-138">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="05550-139">Notes</span><span class="sxs-lookup"><span data-stu-id="05550-139">Remarks</span></span>

<span data-ttu-id="05550-140">Le système d’e/s peut être invité à envoyer des paquets de notification de fin d’exécution d’e/s aux ports de terminaison d’e/s, où ils sont mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="05550-140">The I/O system can be instructed to send I/O completion notification packets to I/O completion ports, where they are queued.</span></span> <span data-ttu-id="05550-141">La fonction **CreateIoCompletionPort** fournit cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="05550-141">The **CreateIoCompletionPort** function provides this functionality.</span></span>

<span data-ttu-id="05550-142">Un port de terminaison d’e/s et son descripteur sont associés au processus qui l’a créé et ne peuvent pas être partagés entre les processus.</span><span class="sxs-lookup"><span data-stu-id="05550-142">An I/O completion port and its handle are associated with the process that created it and is not sharable between processes.</span></span> <span data-ttu-id="05550-143">Toutefois, un seul descripteur peut être partagé entre les threads du même processus.</span><span class="sxs-lookup"><span data-stu-id="05550-143">However, a single handle is sharable between threads in the same process.</span></span>

<span data-ttu-id="05550-144">**CreateIoCompletionPort** peut être utilisé dans trois modes distincts :</span><span class="sxs-lookup"><span data-stu-id="05550-144">**CreateIoCompletionPort** can be used in three distinct modes:</span></span>

-   <span data-ttu-id="05550-145">Créez uniquement un port de terminaison d’e/s sans l’associer à un descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="05550-145">Create only an I/O completion port without associating it with a file handle.</span></span>
-   <span data-ttu-id="05550-146">Associer un port de terminaison d’e/s existant à un descripteur de fichier.</span><span class="sxs-lookup"><span data-stu-id="05550-146">Associate an existing I/O completion port with a file handle.</span></span>
-   <span data-ttu-id="05550-147">Effectuez la création et l’Association en un seul appel.</span><span class="sxs-lookup"><span data-stu-id="05550-147">Perform both creation and association in a single call.</span></span>

<span data-ttu-id="05550-148">Pour créer un port de terminaison d’e/s sans l’associer, définissez le paramètre *FileHandle* sur **\_ \_ valeur de handle non valide**, le paramètre *ExistingCompletionPort* sur **null** et le paramètre *CompletionKey* sur zéro (ce qui est ignoré dans ce cas).</span><span class="sxs-lookup"><span data-stu-id="05550-148">To create an I/O completion port without associating it, set the *FileHandle* parameter to **INVALID\_HANDLE\_VALUE**, the *ExistingCompletionPort* parameter to **NULL**, and the *CompletionKey* parameter to zero (which is ignored in this case).</span></span> <span data-ttu-id="05550-149">Définissez le paramètre *NumberOfConcurrentThreads* sur la valeur de concurrence souhaitée pour le nouveau port de terminaison d’e/s, ou sur zéro pour la valeur par défaut (le nombre de processeurs dans le système).</span><span class="sxs-lookup"><span data-stu-id="05550-149">Set the *NumberOfConcurrentThreads* parameter to the desired concurrency value for the new I/O completion port, or zero for the default (the number of processors in the system).</span></span>

<span data-ttu-id="05550-150">Le descripteur passé dans le paramètre *FileHandle* peut être n’importe quel handle qui prend en charge les e/s avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="05550-150">The handle passed in the *FileHandle* parameter can be any handle that supports overlapped I/O.</span></span> <span data-ttu-id="05550-151">Le plus souvent, il s’agit d’un handle ouvert par la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) à l’aide de l’indicateur de fichier avec indicateur de **\_ \_ chevauchement** (par exemple, fichiers, emplacements de messagerie et canaux).</span><span class="sxs-lookup"><span data-stu-id="05550-151">Most commonly, this is a handle opened by the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function using the **FILE\_FLAG\_OVERLAPPED** flag (for example, files, mail slots, and pipes).</span></span> <span data-ttu-id="05550-152">Les objets créés par d’autres fonctions, tels que [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) , peuvent également être associés à un port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="05550-152">Objects created by other functions such as [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) can also be associated with an I/O completion port.</span></span> <span data-ttu-id="05550-153">Pour obtenir un exemple d’utilisation de sockets, consultez la rubrique [**accepted**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span><span class="sxs-lookup"><span data-stu-id="05550-153">For an example using sockets, see [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span></span> <span data-ttu-id="05550-154">Un descripteur peut être associé à un seul port de terminaison d’e/s et, une fois l’association établie, le handle reste associé à ce port de terminaison d’e/s jusqu’à ce qu’il soit fermé.</span><span class="sxs-lookup"><span data-stu-id="05550-154">A handle can be associated with only one I/O completion port, and after the association is made, the handle remains associated with that I/O completion port until it is closed.</span></span>

<span data-ttu-id="05550-155">Pour plus d’informations sur la théorie, l’utilisation et les fonctions associées du port de terminaison d’e/s, consultez [ports de terminaison d’e/s](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="05550-155">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="05550-156">Plusieurs descripteurs de fichiers peuvent être associés à un seul port de terminaison d’e/s en appelant **CreateIoCompletionPort** plusieurs fois avec le même handle de port de terminaison d’e/s dans le paramètre *ExistingCompletionPort* et un autre descripteur de fichier dans le paramètre *FileHandle* à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="05550-156">Multiple file handles can be associated with a single I/O completion port by calling **CreateIoCompletionPort** multiple times with the same I/O completion port handle in the *ExistingCompletionPort* parameter and a different file handle in the *FileHandle* parameter each time.</span></span>

<span data-ttu-id="05550-157">Utilisez le paramètre *CompletionKey* pour aider votre application à effectuer le suivi des opérations d’e/s terminées.</span><span class="sxs-lookup"><span data-stu-id="05550-157">Use the *CompletionKey* parameter to help your application track which I/O operations have completed.</span></span> <span data-ttu-id="05550-158">Cette valeur n’est pas utilisée par **CreateIoCompletionPort** pour le contrôle fonctionnel ; au lieu de cela, il est attaché au descripteur de fichier spécifié dans le paramètre *FileHandle* au moment de l’association avec un port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="05550-158">This value is not used by **CreateIoCompletionPort** for functional control; rather, it is attached to the file handle specified in the *FileHandle* parameter at the time of association with an I/O completion port.</span></span> <span data-ttu-id="05550-159">Cette clé de fin doit être unique pour chaque descripteur de fichier et elle accompagne le descripteur de fichier tout au long du processus de mise en file d’attente d’achèvement interne.</span><span class="sxs-lookup"><span data-stu-id="05550-159">This completion key should be unique for each file handle, and it accompanies the file handle throughout the internal completion queuing process.</span></span> <span data-ttu-id="05550-160">Elle est retournée dans l’appel de fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) lorsqu’un paquet de saisie semi-automatique arrive.</span><span class="sxs-lookup"><span data-stu-id="05550-160">It is returned in the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function call when a completion packet arrives.</span></span> <span data-ttu-id="05550-161">Le paramètre *CompletionKey* est également utilisé par la fonction [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) pour la mise en file d’attente de vos propres paquets d’achèvement à usage spécifique.</span><span class="sxs-lookup"><span data-stu-id="05550-161">The *CompletionKey* parameter is also used by the [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) function to queue your own special-purpose completion packets.</span></span>

<span data-ttu-id="05550-162">Une fois qu’une instance d’un handle ouvert est associée à un port de terminaison d’e/s, elle ne peut pas être utilisée dans la fonction [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) ou [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) , car ces fonctions ont leurs propres mécanismes d’e/s asynchrones.</span><span class="sxs-lookup"><span data-stu-id="05550-162">After an instance of an open handle is associated with an I/O completion port, it cannot be used in the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function because these functions have their own asynchronous I/O mechanisms.</span></span>

<span data-ttu-id="05550-163">Il est préférable de ne pas partager un descripteur de fichier associé à un port de terminaison d’e/s en utilisant l’héritage des handles ou un appel à la fonction [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="05550-163">It is best not to share a file handle associated with an I/O completion port by using either handle inheritance or a call to the [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) function.</span></span> <span data-ttu-id="05550-164">Les opérations effectuées avec ces handles en double génèrent des notifications de fin d’exécution.</span><span class="sxs-lookup"><span data-stu-id="05550-164">Operations performed with such duplicate handles generate completion notifications.</span></span> <span data-ttu-id="05550-165">Une attention particulière est conseillée.</span><span class="sxs-lookup"><span data-stu-id="05550-165">Careful consideration is advised.</span></span>

<span data-ttu-id="05550-166">Le descripteur de port de terminaison d’e/s et chaque descripteur de fichier associé à ce port de terminaison d’e/s particulier sont appelés *références au port de terminaison d’e/s*.</span><span class="sxs-lookup"><span data-stu-id="05550-166">The I/O completion port handle and every file handle associated with that particular I/O completion port are known as *references to the I/O completion port*.</span></span> <span data-ttu-id="05550-167">Le port de terminaison d’e/s est libéré lorsqu’il n’y a plus de références à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="05550-167">The I/O completion port is released when there are no more references to it.</span></span> <span data-ttu-id="05550-168">Par conséquent, tous ces handles doivent être correctement fermés pour libérer le port de terminaison d’e/s et les ressources système qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="05550-168">Therefore, all of these handles must be properly closed to release the I/O completion port and its associated system resources.</span></span> <span data-ttu-id="05550-169">Une fois ces conditions satisfaites, fermez le handle de port de terminaison d’e/s en appelant la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="05550-169">After these conditions are satisfied, close the I/O completion port handle by calling the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="05550-170">Dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.</span><span class="sxs-lookup"><span data-stu-id="05550-170">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="05550-171">Technology</span><span class="sxs-lookup"><span data-stu-id="05550-171">Technology</span></span>                                           | <span data-ttu-id="05550-172">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="05550-172">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="05550-173">Protocole SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="05550-173">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="05550-174">Oui</span><span class="sxs-lookup"><span data-stu-id="05550-174">Yes</span></span><br/> |
| <span data-ttu-id="05550-175">Basculement transparent SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="05550-175">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="05550-176">Oui</span><span class="sxs-lookup"><span data-stu-id="05550-176">Yes</span></span><br/> |
| <span data-ttu-id="05550-177">SMB 3,0 avec des partages de fichiers avec montée en puissance parallèle (SO)</span><span class="sxs-lookup"><span data-stu-id="05550-177">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="05550-178">Oui</span><span class="sxs-lookup"><span data-stu-id="05550-178">Yes</span></span><br/> |
| <span data-ttu-id="05550-179">Système de fichiers Volume partagé de cluster (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="05550-179">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="05550-180">Oui</span><span class="sxs-lookup"><span data-stu-id="05550-180">Yes</span></span><br/> |
| <span data-ttu-id="05550-181">Système de fichiers résilient (ReFS)</span><span class="sxs-lookup"><span data-stu-id="05550-181">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="05550-182">Oui</span><span class="sxs-lookup"><span data-stu-id="05550-182">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05550-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05550-183">Requirements</span></span>



| <span data-ttu-id="05550-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05550-184">Requirement</span></span> | <span data-ttu-id="05550-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="05550-185">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05550-186">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05550-186">Minimum supported client</span></span><br/> | <span data-ttu-id="05550-187">Applications de bureau Windows XP- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="05550-187">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="05550-188">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05550-188">Minimum supported server</span></span><br/> | <span data-ttu-id="05550-189">Applications de bureau Windows Server 2003 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="05550-189">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="05550-190">En-tête</span><span class="sxs-lookup"><span data-stu-id="05550-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="05550-191"><dt>IoAPI. h (inclure Windows. h); </dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP (incluant Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05550-191"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="05550-192">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05550-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="05550-193"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="05550-193"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="05550-194">DLL</span><span class="sxs-lookup"><span data-stu-id="05550-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05550-195"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05550-195"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="05550-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05550-196">See also</span></span>

<dl> <dt>

<span data-ttu-id="05550-197">**Rubriques de présentation**</span><span class="sxs-lookup"><span data-stu-id="05550-197">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="05550-198">Fonctions de gestion de fichiers</span><span class="sxs-lookup"><span data-stu-id="05550-198">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="05550-199">Ports de terminaison d’e/s</span><span class="sxs-lookup"><span data-stu-id="05550-199">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="05550-200">Utilisation des en-têtes Windows</span><span class="sxs-lookup"><span data-stu-id="05550-200">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[<span data-ttu-id="05550-201">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="05550-201">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

<span data-ttu-id="05550-202">**Fonctions**</span><span class="sxs-lookup"><span data-stu-id="05550-202">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="05550-203">**Accepte**</span><span class="sxs-lookup"><span data-stu-id="05550-203">**AcceptEx**</span></span>](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[<span data-ttu-id="05550-204">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="05550-204">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="05550-205">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="05550-205">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="05550-206">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="05550-206">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="05550-207">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="05550-207">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="05550-208">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="05550-208">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="05550-209">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="05550-209">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="05550-210">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="05550-210">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

