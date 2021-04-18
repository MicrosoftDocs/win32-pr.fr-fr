---
title: system_handle, attribut
description: L’attribut \ system_handle \ spécifie un type de handle défini par le système.
keywords:
- system_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106520236"
---
# <a name="system_handle-attribute"></a><span data-ttu-id="8c701-104">system_handle, attribut</span><span class="sxs-lookup"><span data-stu-id="8c701-104">system_handle attribute</span></span>

<span data-ttu-id="8c701-105">L' \[ attribut **system_handle** \] spécifie un type de handle défini par le système qui représente l’accès à un objet système.</span><span class="sxs-lookup"><span data-stu-id="8c701-105">The \[**system_handle**\] attribute specifies a system-defined handle type that represents access to a system object.</span></span>

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a><span data-ttu-id="8c701-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c701-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c701-107">*System-handle-type*</span><span class="sxs-lookup"><span data-stu-id="8c701-107">*system-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8c701-108">Spécifie l’une des options de type de handle du système.</span><span class="sxs-lookup"><span data-stu-id="8c701-108">Specifies one of the system handle type options.</span></span>

<span data-ttu-id="8c701-109">Les options valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c701-109">The valid options are:</span></span>
* <span data-ttu-id="8c701-110">[sh_composition](sh-composition.md) : handle de surface DirectComposition</span><span class="sxs-lookup"><span data-stu-id="8c701-110">[sh_composition](sh-composition.md) - A DirectComposition surface handle</span></span>
* <span data-ttu-id="8c701-111">[sh_event](sh-event.md) -objet d’événement nommé ou sans nom</span><span class="sxs-lookup"><span data-stu-id="8c701-111">[sh_event](sh-event.md) - A named or unnamed event object</span></span>
* <span data-ttu-id="8c701-112">[sh_file](sh-file.md) -un fichier ou un périphérique d’e/s</span><span class="sxs-lookup"><span data-stu-id="8c701-112">[sh_file](sh-file.md) - A file or I/O device</span></span>
* <span data-ttu-id="8c701-113">[sh_job](sh-job.md) -objet de traitement</span><span class="sxs-lookup"><span data-stu-id="8c701-113">[sh_job](sh-job.md) - A job object</span></span>
* <span data-ttu-id="8c701-114">[sh_mutex](sh-mutex.md) -un objet mutex nommé ou sans nom</span><span class="sxs-lookup"><span data-stu-id="8c701-114">[sh_mutex](sh-mutex.md) - A named or unnamed mutex object</span></span>
* <span data-ttu-id="8c701-115">[sh_pipe](sh-pipe.md) -objet canal nommé ou anonyme</span><span class="sxs-lookup"><span data-stu-id="8c701-115">[sh_pipe](sh-pipe.md) - An anonymous or named pipe object</span></span>
* <span data-ttu-id="8c701-116">[sh_process](sh-process.md) -un objet processus</span><span class="sxs-lookup"><span data-stu-id="8c701-116">[sh_process](sh-process.md) - A process object</span></span>
* <span data-ttu-id="8c701-117">[sh_reg_key](sh-reg-key.md) -une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="8c701-117">[sh_reg_key](sh-reg-key.md) - A registry key</span></span>
* <span data-ttu-id="8c701-118">[sh_section](sh-section.md) -une section de mémoire partagée</span><span class="sxs-lookup"><span data-stu-id="8c701-118">[sh_section](sh-section.md) - A shared memory section</span></span>
* <span data-ttu-id="8c701-119">[sh_semaphore](sh-semaphore.md) -objet sémaphore nommé ou sans nom</span><span class="sxs-lookup"><span data-stu-id="8c701-119">[sh_semaphore](sh-semaphore.md) - A named or unnamed semaphore object</span></span>
* <span data-ttu-id="8c701-120">[sh_socket](sh-socket.md) -objet de socket Winsock</span><span class="sxs-lookup"><span data-stu-id="8c701-120">[sh_socket](sh-socket.md) - A WinSock socket object</span></span>
* <span data-ttu-id="8c701-121">[sh_thread](sh-thread.md) -objet thread</span><span class="sxs-lookup"><span data-stu-id="8c701-121">[sh_thread](sh-thread.md) - A thread object</span></span>
* <span data-ttu-id="8c701-122">[sh_token](sh-token.md) -objet de jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="8c701-122">[sh_token](sh-token.md) - An access token object</span></span>

</dd> <dt>

<span data-ttu-id="8c701-123">*masque d’accès facultatif*</span><span class="sxs-lookup"><span data-stu-id="8c701-123">*optional-access-mask*</span></span>
</dt> <dd>

<span data-ttu-id="8c701-124">Demande éventuellement des droits d’accès spécifiques appliqués au descripteur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="8c701-124">Optionally requests specific access rights applied to the duplicated handle.</span></span> <span data-ttu-id="8c701-125">Par défaut, lorsque ce paramètre n’est pas spécifié, le handle est dupliqué avec le même accès.</span><span class="sxs-lookup"><span data-stu-id="8c701-125">By default when this is unspecified, the handle will be duplicated with the same access.</span></span> 

<span data-ttu-id="8c701-126">Pour spécifier un niveau d’accès différent, utilisez les droits d’accès spécifiques à l’objet correspondant à l’objet système sous-jacent sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8c701-126">To specify a different level of access, use object specific access rights corresponding to the underlying system object selected.</span></span>

<span data-ttu-id="8c701-127">Pour plus d’informations sur la façon dont les droits d’accès sont propagés au cours de la duplication, consultez la documentation [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="8c701-127">More information on how access rights are propagated during duplication can be found on the [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) documentation.</span></span>

<span data-ttu-id="8c701-128">Des liens vers des listes de droits d’accès pour chaque type d’objet se trouvent dans la référence *DuplicateHandle* , ainsi que dans la page **Voir aussi** les en-têtes de chaque `sh_*` paramètre.</span><span class="sxs-lookup"><span data-stu-id="8c701-128">Links to lists of access rights for each type of object can be found in the *DuplicateHandle* reference as well as in the **See also** headings of each `sh_*` parameter page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c701-129">Notes</span><span class="sxs-lookup"><span data-stu-id="8c701-129">Remarks</span></span>

<span data-ttu-id="8c701-130">Pour pouvoir utiliser cet attribut, l' `-target` indicateur doit avoir la valeur `NT100` (ou une version ultérieure) lors de l’exécution de midl.exe.</span><span class="sxs-lookup"><span data-stu-id="8c701-130">In order to use this attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

<span data-ttu-id="8c701-131">Les handles du système sont des handles définis par le système d’exploitation pour fournir l’accès à une ressource système.</span><span class="sxs-lookup"><span data-stu-id="8c701-131">System handles are handles that are defined by the operating system to provide access to a system resource.</span></span> <span data-ttu-id="8c701-132">Le type spécifique de l’objet qui se trouve derrière le descripteur doit être spécifié lors de la déclaration de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="8c701-132">The specific type of the object behind the handle must be specified when declaring the attribute.</span></span>

<span data-ttu-id="8c701-133">Pour un handle marqué `[in]` , le descripteur est dupliqué dans la procédure distante et reste valide pour la durée de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="8c701-133">For a handle marked `[in]`, the handle will be duplicated into the remote procedure and remains valid for the duration of that procedure.</span></span> <span data-ttu-id="8c701-134">Au retour de la procédure distante, le handle dupliqué est libéré.</span><span class="sxs-lookup"><span data-stu-id="8c701-134">On return from the remote procedure, the duplicated handle is freed.</span></span> <span data-ttu-id="8c701-135">Pour conserver l’accès à l’objet sous-jacent, l’application distante doit dupliquer le handle dans son propre espace d’adressage.</span><span class="sxs-lookup"><span data-stu-id="8c701-135">To maintain access to the underlying object, the remote application must duplicate the handle into its own address space.</span></span>

<span data-ttu-id="8c701-136">En revanche, pour un handle marqué `[out]` , lorsqu’une procédure distante retourne un descripteur à partir d’un appel, la procédure distante perd la propriété de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="8c701-136">By contrast, for a handle marked `[out]`, when a remote procedure returns a handle from a call, the remote procedure will lose ownership of it.</span></span> <span data-ttu-id="8c701-137">Pour conserver l’accès à l’objet sous-jacent, la procédure distante doit dupliquer le handle et retourner le doublon.</span><span class="sxs-lookup"><span data-stu-id="8c701-137">To maintain access to the underlying object, the remote procedure should duplicate the handle and return the duplicate.</span></span> <span data-ttu-id="8c701-138">Le handle retourné est alors détenu par l’appelant qui assume la responsabilité de la fermer lorsqu’un accès à l’objet système sous-jacent n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8c701-138">The returned handle then becomes owned by the caller who assumes a responsibility to close it when access to the underlying system object is no longer necessary.</span></span>

<span data-ttu-id="8c701-139">Comme il s’agit d’un mécanisme de relais d’accès à un objet système, cet attribut s’applique uniquement aux appels entre les procédures sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8c701-139">As this is a mechanism for relaying access to a system object, this attribute is only applicable to calls between procedures on the same machine.</span></span>

<span data-ttu-id="8c701-140">Les paramètres de création et d’accès donnés à l’objet sous-jacent derrière le descripteur système de sa création déterminent s’il peut être correctement marshalé dans le contexte de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="8c701-140">The creation and access parameters given to the underlying object behind the system handle on its creation will dictate whether it can be successfully marshalled to the remote procedure context.</span></span>

<span data-ttu-id="8c701-141">Un tableau de `system_handle` peut être passé dans ou à l’aide de la syntaxe trouvée dans la documentation de l' [**attribut size_is**](size-is.md) .</span><span class="sxs-lookup"><span data-stu-id="8c701-141">An array of `system_handle` can be passed either in or out with the syntax found in the [**size_is attribute**](size-is.md) documentation.</span></span>

## <a name="examples"></a><span data-ttu-id="8c701-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="8c701-142">Examples</span></span>

<span data-ttu-id="8c701-143">Les exemples suivants utilisent plusieurs utilisations de `system_handle` .</span><span class="sxs-lookup"><span data-stu-id="8c701-143">The following examples several uses of `system_handle`.</span></span> <span data-ttu-id="8c701-144">Pour obtenir un exemple complet, consultez l’exemple [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) .</span><span class="sxs-lookup"><span data-stu-id="8c701-144">For a complete sample, see the [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) sample.</span></span>

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a><span data-ttu-id="8c701-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c701-145">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="8c701-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c701-146">Minimum supported client</span></span> | <span data-ttu-id="8c701-147">Mise à jour anniversaire Windows 10 (version 1607, Build 14393)</span><span class="sxs-lookup"><span data-stu-id="8c701-147">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="8c701-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c701-148">Minimum supported server</span></span> | <span data-ttu-id="8c701-149">Windows Server 2016 (Build 14393)</span><span class="sxs-lookup"><span data-stu-id="8c701-149">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="8c701-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c701-150">See also</span></span>

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[<span data-ttu-id="8c701-151">/target, commutateur</span><span class="sxs-lookup"><span data-stu-id="8c701-151">/target switch</span></span>](./-target.md)
</dt> <dt>

[<span data-ttu-id="8c701-152">Liaison et Handles</span><span class="sxs-lookup"><span data-stu-id="8c701-152">Binding and Handles</span></span>](../Rpc/binding-and-handles.md)
</dt> <dt>

[<span data-ttu-id="8c701-153">Handles et objets</span><span class="sxs-lookup"><span data-stu-id="8c701-153">Handles and Objects</span></span>](../sysinfo/handles-and-objects.md)
</dt> <dt>

[<span data-ttu-id="8c701-154">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="8c701-154">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="8c701-155">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="8c701-155">**DuplicateHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="8c701-156">Descripteurs de sécurité</span><span class="sxs-lookup"><span data-stu-id="8c701-156">Security Descriptors</span></span>](../secauthz/security-descriptors.md)
</dt></dl>
