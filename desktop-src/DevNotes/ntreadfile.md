---
description: Lit les données d’un fichier ouvert.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Fonction NtReadFile (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523175"
---
# <a name="ntreadfile-function"></a><span data-ttu-id="804cb-103">NtReadFile fonction)</span><span class="sxs-lookup"><span data-stu-id="804cb-103">NtReadFile function</span></span>

<span data-ttu-id="804cb-104">Lit les données d’un fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="804cb-104">Reads data from an open file.</span></span>

<span data-ttu-id="804cb-105">Cette fonction est l’équivalent du mode utilisateur à la fonction [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) documentée dans le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="804cb-105">This function is the user-mode equivalent to the [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) function documented in the Windows Driver Kit (WDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="804cb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="804cb-106">Syntax</span></span>


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a><span data-ttu-id="804cb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="804cb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="804cb-108">*FileHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="804cb-108">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="804cb-109">Handle de l’objet de fichier.</span><span class="sxs-lookup"><span data-stu-id="804cb-109">Handle to the file object.</span></span> <span data-ttu-id="804cb-110">Ce handle est créé par un appel réussi à [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) ou [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span><span class="sxs-lookup"><span data-stu-id="804cb-110">This handle is created by a successful call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) or [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span></span>

</dd> <dt>

<span data-ttu-id="804cb-111">*Événement* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="804cb-111">*Event* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="804cb-112">Éventuellement, un handle vers un objet d’événement à affecter à l’état signalé une fois l’opération de lecture terminée.</span><span class="sxs-lookup"><span data-stu-id="804cb-112">Optionally, a handle to an event object to set to the signaled state after the read operation completes.</span></span> <span data-ttu-id="804cb-113">Les pilotes de périphériques et intermédiaires doivent définir ce paramètre sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="804cb-113">Device and intermediate drivers should set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="804cb-114">*ApcRoutine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="804cb-114">*ApcRoutine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="804cb-115">Ce paramètre est réservé.</span><span class="sxs-lookup"><span data-stu-id="804cb-115">This parameter is reserved.</span></span> <span data-ttu-id="804cb-116">Les pilotes de périphériques et intermédiaires doivent définir ce pointeur sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="804cb-116">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="804cb-117">*ApcContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="804cb-117">*ApcContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="804cb-118">Ce paramètre est réservé.</span><span class="sxs-lookup"><span data-stu-id="804cb-118">This parameter is reserved.</span></span> <span data-ttu-id="804cb-119">Les pilotes de périphériques et intermédiaires doivent définir ce pointeur sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="804cb-119">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="804cb-120">*IoStatusBlock* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="804cb-120">*IoStatusBlock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="804cb-121">Pointeur vers une structure de [**\_ \_ bloc d’état d’e/s**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) qui reçoit l’état d’achèvement final et des informations sur l’opération de lecture demandée.</span><span class="sxs-lookup"><span data-stu-id="804cb-121">Pointer to an [**IO\_STATUS\_BLOCK**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) structure that receives the final completion status and information about the requested read operation.</span></span> <span data-ttu-id="804cb-122">Le membre d' **informations** reçoit le nombre d’octets réellement lus à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="804cb-122">The **Information** member receives the number of bytes actually read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="804cb-123">*Mémoire tampon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="804cb-123">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="804cb-124">Pointeur vers une mémoire tampon allouée par l’appelant qui reçoit les données lues à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="804cb-124">Pointer to a caller-allocated buffer that receives the data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="804cb-125">*Longueur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="804cb-125">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="804cb-126">Taille, en octets, de la mémoire tampon vers laquelle pointe la *mémoire tampon*.</span><span class="sxs-lookup"><span data-stu-id="804cb-126">The size, in bytes, of the buffer pointed to by *Buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="804cb-127">*ByteOffset* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="804cb-127">*ByteOffset* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="804cb-128">Pointeur vers une variable qui spécifie l’offset d’octet de début dans le fichier où l’opération de lecture doit commencer.</span><span class="sxs-lookup"><span data-stu-id="804cb-128">Pointer to a variable that specifies the starting byte offset in the file where the read operation will begin.</span></span> <span data-ttu-id="804cb-129">En cas de tentative de lecture au-delà de la fin du fichier, **NtReadFile** retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="804cb-129">If an attempt is made to read beyond the end of the file, **NtReadFile** returns an error.</span></span>

<span data-ttu-id="804cb-130">Si l’appel à [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) a défini l’une des alertes d’e/s synchrones de fichier d’indicateurs *CreateOptions* ou de non-alerte d’e \_ \_ \_ \_ \_ /s synchrones \_ , le gestionnaire d’e/s conserve la position de fichier actuelle.</span><span class="sxs-lookup"><span data-stu-id="804cb-130">If the call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set either of the *CreateOptions* flags FILE\_SYNCHRONOUS\_IO\_ALERT or FILE\_SYNCHRONOUS\_IO\_NONALERT, the I/O Manager maintains the current file position.</span></span> <span data-ttu-id="804cb-131">Dans ce cas, l’appelant de **NtReadFile** peut spécifier que le décalage de position de fichier actuel soit utilisé à la place d’une valeur *ByteOffset* explicite.</span><span class="sxs-lookup"><span data-stu-id="804cb-131">If so, the caller of **NtReadFile** can specify that the current file position offset be used instead of an explicit *ByteOffset* value.</span></span> <span data-ttu-id="804cb-132">Cette spécification peut être effectuée à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="804cb-132">This specification can be made by using one of the following methods:</span></span>

-   <span data-ttu-id="804cb-133">Spécifiez un pointeur vers une valeur **\_ entière de type long** avec le membre **HighPart** défini sur-1 et le membre **LowPart** défini sur le fichier de valeurs défini par le système utiliser la position du \_ pointeur de \_ fichier \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="804cb-133">Specify a pointer to a **LARGE\_INTEGER** value with the **HighPart** member set to -1 and the **LowPart** member set to the system-defined value FILE\_USE\_FILE\_POINTER\_POSITION.</span></span>

-   <span data-ttu-id="804cb-134">Passer un pointeur **null** pour *ByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="804cb-134">Pass a **NULL** pointer for *ByteOffset*.</span></span>

<span data-ttu-id="804cb-135">**NtReadFile** met à jour la position de fichier actuelle en ajoutant le nombre d’octets lus lorsqu’il termine l’opération de lecture, s’il utilise la position de fichier actuelle gérée par le gestionnaire d’e/s.</span><span class="sxs-lookup"><span data-stu-id="804cb-135">**NtReadFile** updates the current file position by adding the number of bytes read when it completes the read operation, if it is using the current file position maintained by the I/O Manager.</span></span>

<span data-ttu-id="804cb-136">Même lorsque le gestionnaire d’e/s maintient la position de fichier actuelle, l’appelant peut réinitialiser cette position en passant une valeur *ByteOffset* explicite à **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="804cb-136">Even when the I/O Manager is maintaining the current file position, the caller can reset this position by passing an explicit *ByteOffset* value to **NtReadFile**.</span></span> <span data-ttu-id="804cb-137">Cette opération change automatiquement la position du fichier actuel en cette valeur *ByteOffset* , exécute l’opération de lecture, puis met à jour la position en fonction du nombre d’octets réellement lus.</span><span class="sxs-lookup"><span data-stu-id="804cb-137">Doing this automatically changes the current file position to that *ByteOffset* value, performs the read operation, and then updates the position according to the number of bytes actually read.</span></span> <span data-ttu-id="804cb-138">Cette technique permet au service de recherche et de lecture atomiques de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="804cb-138">This technique gives the caller atomic seek-and-read service.</span></span>

</dd> <dt>

<span data-ttu-id="804cb-139">*Clé* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="804cb-139">*Key* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="804cb-140">Les pilotes de périphériques et intermédiaires doivent définir ce pointeur sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="804cb-140">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="804cb-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="804cb-141">Return value</span></span>

<span data-ttu-id="804cb-142">**NtReadFile** retourne l’état \_ Success ou le code d’erreur NTSTATUS approprié.</span><span class="sxs-lookup"><span data-stu-id="804cb-142">**NtReadFile** returns either STATUS\_SUCCESS or the appropriate NTSTATUS error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="804cb-143">Notes</span><span class="sxs-lookup"><span data-stu-id="804cb-143">Remarks</span></span>

<span data-ttu-id="804cb-144">Les appelants de **NtReadFile** doivent avoir déjà appelé [**NTCREATEFILE**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) avec le fichier \_ Read \_ Data ou generic \_ value défini dans le paramètre *desiredAccess* .</span><span class="sxs-lookup"><span data-stu-id="804cb-144">Callers of **NtReadFile** must have already called [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) with the FILE\_READ\_DATA or GENERIC\_READ value set in the *DesiredAccess* parameter.</span></span>

<span data-ttu-id="804cb-145">Si l’appel précédent à [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) affecte au fichier \_ aucun \_ \_ indicateur de mise en mémoire tampon intermédiaire dans le paramètre *CreateOptions* la valeur **NtCreateFile**, les paramètres *Length* et *ByteOffset* à **NtReadFile** doivent être des multiples de la taille de secteur.</span><span class="sxs-lookup"><span data-stu-id="804cb-145">If the preceding call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set the FILE\_NO\_INTERMEDIATE\_BUFFERING flag in the *CreateOptions* parameter to **NtCreateFile**, the *Length* and *ByteOffset* parameters to **NtReadFile** must be multiples of the sector size.</span></span> <span data-ttu-id="804cb-146">Pour plus d’informations, consultez **NtCreateFile**.</span><span class="sxs-lookup"><span data-stu-id="804cb-146">For more information, see **NtCreateFile**.</span></span>

<span data-ttu-id="804cb-147">**NtReadFile** commence à lire à partir du *ByteOffset* donné ou à la position actuelle du fichier dans la *mémoire tampon* donnée.</span><span class="sxs-lookup"><span data-stu-id="804cb-147">**NtReadFile** begins reading from the given *ByteOffset* or the current file position into the given *Buffer*.</span></span> <span data-ttu-id="804cb-148">Elle met fin à l’opération de lecture dans l’une des conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="804cb-148">It terminates the read operation under one of the following conditions:</span></span>

-   <span data-ttu-id="804cb-149">La mémoire tampon est saturée, car le nombre d’octets spécifié par le paramètre de *longueur* a été lu.</span><span class="sxs-lookup"><span data-stu-id="804cb-149">The buffer is full because the number of bytes specified by the *Length* parameter has been read.</span></span> <span data-ttu-id="804cb-150">Par conséquent, aucune donnée ne peut être placée dans la mémoire tampon sans dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="804cb-150">Therefore, no more data can be placed into the buffer without an overflow.</span></span>

-   <span data-ttu-id="804cb-151">La fin du fichier est atteinte pendant l’opération de lecture, de sorte qu’il n’y a plus de données dans le fichier à transférer dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="804cb-151">The end of file is reached during the read operation, so there is no more data in the file to be transferred into the buffer.</span></span>

<span data-ttu-id="804cb-152">Si l’appelant a ouvert le fichier avec l’indicateur de synchronisation défini dans *desiredAccess*, le thread appelant peut se synchroniser avec l’achèvement de l’opération de lecture en attendant le handle de fichier, *FileHandle*.</span><span class="sxs-lookup"><span data-stu-id="804cb-152">If the caller opened the file with the SYNCHRONIZE flag set in *DesiredAccess*, the calling thread can synchronize to the completion of the read operation by waiting on the file handle, *FileHandle*.</span></span> <span data-ttu-id="804cb-153">Le descripteur est signalé chaque fois qu’une opération d’e/s émise sur le descripteur est terminée.</span><span class="sxs-lookup"><span data-stu-id="804cb-153">The handle is signaled each time that an I/O operation that was issued on the handle completes.</span></span> <span data-ttu-id="804cb-154">Toutefois, l’appelant ne doit pas attendre sur un handle qui a été ouvert pour l’accès synchrone aux fichiers (alerte e/s synchrone de fichier non- \_ \_ \_ alerte ou d' \_ \_ e/s synchrone de fichier \_ ).</span><span class="sxs-lookup"><span data-stu-id="804cb-154">However, the caller must not wait on a handle that was opened for synchronous file access (FILE\_SYNCHRONOUS\_IO\_NONALERT or FILE\_SYNCHRONOUS\_IO\_ALERT).</span></span> <span data-ttu-id="804cb-155">Dans ce cas, **NtReadFile** attend pour le compte de l’appelant et n’est pas retourné tant que l’opération de lecture n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="804cb-155">In this case, **NtReadFile** waits on behalf of the caller and does not return until the read operation is complete.</span></span> <span data-ttu-id="804cb-156">L’appelant peut attendre en toute sécurité le descripteur de fichier uniquement si les trois conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="804cb-156">The caller can safely wait on the file handle only if all three of the following conditions are met:</span></span>

-   <span data-ttu-id="804cb-157">Le descripteur a été ouvert pour un accès asynchrone (autrement dit, aucun \_ \_ indicateur d’e/s synchrone de fichier \_  n’a été spécifié).</span><span class="sxs-lookup"><span data-stu-id="804cb-157">The handle was opened for asynchronous access (that is, neither FILE\_SYNCHRONOUS\_IO\_*XXX* flag was specified).</span></span>

-   <span data-ttu-id="804cb-158">Le descripteur est utilisé pour une seule opération d’e/s à la fois.</span><span class="sxs-lookup"><span data-stu-id="804cb-158">The handle is being used for only one I/O operation at a time.</span></span>

-   <span data-ttu-id="804cb-159">**NtReadFile** a retourné l’état \_ en attente.</span><span class="sxs-lookup"><span data-stu-id="804cb-159">**NtReadFile** returned STATUS\_PENDING.</span></span>

<span data-ttu-id="804cb-160">Un pilote doit appeler **NtReadFile** dans le contexte du processus système si l’une des conditions suivantes est remplie :</span><span class="sxs-lookup"><span data-stu-id="804cb-160">A driver should call **NtReadFile** in the context of the system process if any of the following conditions exist:</span></span>

-   <span data-ttu-id="804cb-161">Le pilote a créé le descripteur de fichier qu’il transmet à **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="804cb-161">The driver created the file handle that it passes to **NtReadFile**.</span></span>

-   <span data-ttu-id="804cb-162">**NtReadFile** informe le pilote d’achèvement des e/s au moyen d’un événement que le pilote a créé.</span><span class="sxs-lookup"><span data-stu-id="804cb-162">**NtReadFile** will notify the driver of I/O completion by means of an event that the driver created.</span></span>

-   <span data-ttu-id="804cb-163">**NtReadFile** informe le pilote d’achèvement des e/s au moyen d’une routine de rappel APC que le pilote transmet à **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="804cb-163">**NtReadFile** will notify the driver of I/O completion by means of an APC callback routine that the driver passes to **NtReadFile**.</span></span>

<span data-ttu-id="804cb-164">Les handles de fichiers et d’événements ne sont valides que dans le contexte de processus où les descripteurs sont créés.</span><span class="sxs-lookup"><span data-stu-id="804cb-164">File and event handles are valid only in the process context where the handles are created.</span></span> <span data-ttu-id="804cb-165">Par conséquent, pour éviter les brèches de sécurité, le pilote doit créer tout handle de fichier ou d’événement qu’il transmet à **NtReadFile** dans le contexte du processus système plutôt que dans le contexte du processus dans lequel se trouve le pilote.</span><span class="sxs-lookup"><span data-stu-id="804cb-165">Therefore, to avoid security holes, the driver should create any file or event handle that it passes to **NtReadFile** in the context of the system process rather than the context of the process that the driver is in.</span></span>

<span data-ttu-id="804cb-166">De même, **NtReadFile** doit être appelé dans le contexte du processus système s’il notifie le pilote d’achèvement des e/s au moyen d’un APC, car les APC sont toujours déclenchés dans le contexte du thread qui émet la requête d’e/s.</span><span class="sxs-lookup"><span data-stu-id="804cb-166">Likewise, **NtReadFile** should be called in the context of the system process if it notifies the driver of I/O completion by means of an APC, because APCs are always fired in the context of the thread that issues the I/O request.</span></span> <span data-ttu-id="804cb-167">Si le pilote appelle **NtReadFile** dans le contexte d’un processus autre que celui du système, l’APC peut être retardé indéfiniment ou ne pas se déclencher du tout.</span><span class="sxs-lookup"><span data-stu-id="804cb-167">If the driver calls **NtReadFile** in the context of a process other than the system one, the APC could be delayed indefinitely, or it might not fire at all.</span></span>

<span data-ttu-id="804cb-168">Pour plus d’informations sur l’utilisation des fichiers, consultez [utilisation de fichiers dans un pilote](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span><span class="sxs-lookup"><span data-stu-id="804cb-168">For more information about working with files, see [Using Files in a Driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span></span>

<span data-ttu-id="804cb-169">Les appelants de **NtReadFile** doivent s’exécuter au niveau IRQL = passif \_ et les appels de fonction de [noyau spéciaux sont activés](/windows-hardware/drivers/kernel/disabling-apcs).</span><span class="sxs-lookup"><span data-stu-id="804cb-169">Callers of **NtReadFile** must be running at IRQL = PASSIVE\_LEVEL and [with special kernel APCs enabled](/windows-hardware/drivers/kernel/disabling-apcs).</span></span>

## <a name="requirements"></a><span data-ttu-id="804cb-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="804cb-170">Requirements</span></span>



| <span data-ttu-id="804cb-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="804cb-171">Requirement</span></span> | <span data-ttu-id="804cb-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="804cb-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="804cb-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="804cb-173">Minimum supported client</span></span><br/> | <span data-ttu-id="804cb-174">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="804cb-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="804cb-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="804cb-175">Minimum supported server</span></span><br/> | <span data-ttu-id="804cb-176">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="804cb-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="804cb-177">Plateforme cible</span><span class="sxs-lookup"><span data-stu-id="804cb-177">Target platform</span></span><br/>          | <dl> <span data-ttu-id="804cb-178"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="804cb-178"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="804cb-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="804cb-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="804cb-180"><dt>WDM. h (inclure WDM. h, Ntddk. h ou Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="804cb-180"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="804cb-181">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="804cb-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="804cb-182"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="804cb-182"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="804cb-183">DLL</span><span class="sxs-lookup"><span data-stu-id="804cb-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="804cb-184"><dt>Ntdll.dll (mode utilisateur)</dt></span><span class="sxs-lookup"><span data-stu-id="804cb-184"><dt>Ntdll.dll (user mode)</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="804cb-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="804cb-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804cb-186">**KeInitializeEvent**</span><span class="sxs-lookup"><span data-stu-id="804cb-186">**KeInitializeEvent**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[<span data-ttu-id="804cb-187">**NtCreateFile**</span><span class="sxs-lookup"><span data-stu-id="804cb-187">**NtCreateFile**</span></span>](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[<span data-ttu-id="804cb-188">**NtQueryInformationFile**</span><span class="sxs-lookup"><span data-stu-id="804cb-188">**NtQueryInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[<span data-ttu-id="804cb-189">**NtSetInformationFile**</span><span class="sxs-lookup"><span data-stu-id="804cb-189">**NtSetInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[<span data-ttu-id="804cb-190">**NtWriteFile**</span><span class="sxs-lookup"><span data-stu-id="804cb-190">**NtWriteFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
