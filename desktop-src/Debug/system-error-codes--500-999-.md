---
description: Décrit les codes d’erreur 500-999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Codes d’erreur système (500-999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201063"
---
# <a name="system-error-codes-500-999"></a><span data-ttu-id="0bac2-103">Codes d’erreur système (500-999)</span><span class="sxs-lookup"><span data-stu-id="0bac2-103">System Error Codes (500-999)</span></span>

> [!NOTE]
> <span data-ttu-id="0bac2-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="0bac2-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0bac2-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="0bac2-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs 500 à 999).</span><span class="sxs-lookup"><span data-stu-id="0bac2-106">The following list describes [system error codes](system-error-codes.md) (errors 500 to 999).</span></span> <span data-ttu-id="0bac2-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="0bac2-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="0bac2-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="0bac2-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERREUR \_ de \_ chargement du profil utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR\_USER\_PROFILE\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-110">500 (0x1F4)</span><span class="sxs-lookup"><span data-stu-id="0bac2-110">500 (0x1F4)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-111">Impossible de charger le profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0bac2-111">User profile cannot be loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**\_dépassement arithmétique de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**ERROR\_ARITHMETIC\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-113">534 (0x216)</span><span class="sxs-lookup"><span data-stu-id="0bac2-113">534 (0x216)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-114">Le résultat arithmétique a dépassé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0bac2-114">Arithmetic result exceeded 32 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**canal d’erreur \_ \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="0bac2-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**ERROR\_PIPE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-116">535 (0x217)</span><span class="sxs-lookup"><span data-stu-id="0bac2-116">535 (0x217)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-117">Il existe un processus à l’autre extrémité du canal.</span><span class="sxs-lookup"><span data-stu-id="0bac2-117">There is a process on other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**\_écoute du canal d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**ERROR\_PIPE\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-119">536 (0x218)</span><span class="sxs-lookup"><span data-stu-id="0bac2-119">536 (0x218)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-120">En attente d’un processus pour ouvrir l’autre extrémité du canal.</span><span class="sxs-lookup"><span data-stu-id="0bac2-120">Waiting for a process to open the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**arrêt du vérificateur d’erreurs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**ERROR\_VERIFIER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-122">537 (0x219)</span><span class="sxs-lookup"><span data-stu-id="0bac2-122">537 (0x219)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-123">Le vérificateur d’applications a rencontré une erreur dans le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="0bac2-123">Application verifier has found an error in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**erreur \_ ABIOS \_ erreur**</span><span class="sxs-lookup"><span data-stu-id="0bac2-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**ERROR\_ABIOS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-125">538 (0x21A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-125">538 (0x21A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-126">Une erreur s’est produite dans le sous-système ABIOS.</span><span class="sxs-lookup"><span data-stu-id="0bac2-126">An error occurred in the ABIOS subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**\_Avertissement WX86 d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR\_WX86\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-128">539 (0x21B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-128">539 (0x21B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-129">Un avertissement s’est produit dans le sous-système WX86.</span><span class="sxs-lookup"><span data-stu-id="0bac2-129">A warning occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Erreur \_ WX86 \_ erreur**</span><span class="sxs-lookup"><span data-stu-id="0bac2-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**ERROR\_WX86\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-131">540 (0x21C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-131">540 (0x21C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-132">Une erreur s’est produite dans le sous-système WX86.</span><span class="sxs-lookup"><span data-stu-id="0bac2-132">An error occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**\_minuteur d’erreur \_ non \_ annulé**</span><span class="sxs-lookup"><span data-stu-id="0bac2-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**ERROR\_TIMER\_NOT\_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-134">541 (0x21D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-134">541 (0x21D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-135">Une tentative a été effectuée pour annuler ou définir un minuteur associé à un APC et le thread d’objet n’est pas le thread qui a défini à l’origine le minuteur avec une routine APC associée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-135">An attempt was made to cancel or set a timer that has an associated APC and the subject thread is not the thread that originally set the timer with an associated APC routine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERREUR lors du \_ déroulement**</span><span class="sxs-lookup"><span data-stu-id="0bac2-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERROR\_UNWIND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-137">542 (0x21E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-137">542 (0x21E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-138">Code d’exception de déroulement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-138">Unwind exception code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERREUR \_ pile incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERROR\_BAD\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-140">543 (0x21F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-140">543 (0x21F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-141">Une pile non valide ou non alignée a été rencontrée lors d’une opération de déroulement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-141">An invalid or unaligned stack was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERREUR d’une \_ cible de déroulement non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR\_INVALID\_UNWIND\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-143">544 (0x220)</span><span class="sxs-lookup"><span data-stu-id="0bac2-143">544 (0x220)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-144">Une cible de déroulement non valide a été rencontrée pendant une opération de déroulement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-144">An invalid unwind target was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**\_attributs de \_ port non valides d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR\_INVALID\_PORT\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-146">545 (0x221)</span><span class="sxs-lookup"><span data-stu-id="0bac2-146">545 (0x221)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-147">Attributs d’objet non valides spécifiés pour NtCreatePort ou les attributs de port non valides spécifiés à NtConnectPort</span><span class="sxs-lookup"><span data-stu-id="0bac2-147">Invalid Object Attributes specified to NtCreatePort or invalid Port Attributes specified to NtConnectPort</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**MESSAGE de port d’erreur \_ \_ \_ trop \_ long**</span><span class="sxs-lookup"><span data-stu-id="0bac2-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**ERROR\_PORT\_MESSAGE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-149">546 (0x222)</span><span class="sxs-lookup"><span data-stu-id="0bac2-149">546 (0x222)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-150">La longueur du message transmis à NtRequestPort ou NtRequestWaitReplyPort était plus longue que le message maximal autorisé par le port.</span><span class="sxs-lookup"><span data-stu-id="0bac2-150">Length of message passed to NtRequestPort or NtRequestWaitReplyPort was longer than the maximum message allowed by the port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERREUR \_ de \_ quota non valide \_ inférieure**</span><span class="sxs-lookup"><span data-stu-id="0bac2-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR\_INVALID\_QUOTA\_LOWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-152">547 (0x223)</span><span class="sxs-lookup"><span data-stu-id="0bac2-152">547 (0x223)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-153">Une tentative a été effectuée pour réduire une limite de quota au-dessous de l’utilisation actuelle.</span><span class="sxs-lookup"><span data-stu-id="0bac2-153">An attempt was made to lower a quota limit below the current usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**périphérique d’erreur \_ \_ déjà \_ attaché**</span><span class="sxs-lookup"><span data-stu-id="0bac2-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**ERROR\_DEVICE\_ALREADY\_ATTACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-155">548 (0x224)</span><span class="sxs-lookup"><span data-stu-id="0bac2-155">548 (0x224)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-156">Une tentative d’attachement à un appareil déjà attaché à un autre périphérique a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-156">An attempt was made to attach to a device that was already attached to another device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ALIGNEMENT incorrect de l’instruction d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR\_INSTRUCTION\_MISALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-158">549 (0x225)</span><span class="sxs-lookup"><span data-stu-id="0bac2-158">549 (0x225)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-159">Une tentative a été effectuée pour exécuter une instruction à une adresse non alignée et le système hôte ne prend pas en charge les références d’instruction non alignées.</span><span class="sxs-lookup"><span data-stu-id="0bac2-159">An attempt was made to execute an instruction at an unaligned address and the host system does not support unaligned instruction references.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**le \_ profilage des erreurs \_ n' \_ a pas démarré**</span><span class="sxs-lookup"><span data-stu-id="0bac2-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERROR\_PROFILING\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-161">550 (0x226)</span><span class="sxs-lookup"><span data-stu-id="0bac2-161">550 (0x226)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-162">Le profilage n’a pas démarré.</span><span class="sxs-lookup"><span data-stu-id="0bac2-162">Profiling not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERREUR de \_ profilage \_ non \_ arrêté**</span><span class="sxs-lookup"><span data-stu-id="0bac2-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERROR\_PROFILING\_NOT\_STOPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-164">551 (0x227)</span><span class="sxs-lookup"><span data-stu-id="0bac2-164">551 (0x227)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-165">Le profilage n’est pas arrêté.</span><span class="sxs-lookup"><span data-stu-id="0bac2-165">Profiling not stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**l’erreur \_ n’a \_ pas pu être \_ interprétée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR\_COULD\_NOT\_INTERPRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-167">552 (0x228)</span><span class="sxs-lookup"><span data-stu-id="0bac2-167">552 (0x228)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-168">La liste de contrôle d’accès passée ne contenait pas les informations minimales requises.</span><span class="sxs-lookup"><span data-stu-id="0bac2-168">The passed ACL did not contain the minimum required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERREUR \_ de profilage \_ à la \_ limite**</span><span class="sxs-lookup"><span data-stu-id="0bac2-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERROR\_PROFILING\_AT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-170">553 (0x229)</span><span class="sxs-lookup"><span data-stu-id="0bac2-170">553 (0x229)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-171">Le nombre d’objets de profilage actifs est au maximum et il n’est plus possible de démarrer.</span><span class="sxs-lookup"><span data-stu-id="0bac2-171">The number of active profiling objects is at the maximum and no more may be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERREUR \_ Impossible d' \_ attendre**</span><span class="sxs-lookup"><span data-stu-id="0bac2-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR\_CANT\_WAIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-173">554 (0x22A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-173">554 (0x22A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-174">Permet d’indiquer qu’une opération ne peut pas continuer sans blocage pour les e/s.</span><span class="sxs-lookup"><span data-stu-id="0bac2-174">Used to indicate that an operation cannot continue without blocking for I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERREUR \_ Impossible de \_ se terminer \_ automatiquement**</span><span class="sxs-lookup"><span data-stu-id="0bac2-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR\_CANT\_TERMINATE\_SELF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-176">555 (0x22B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-176">555 (0x22B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-177">Indique qu’un thread a tenté de se terminer lui-même par défaut (appelé NtTerminateThread avec **null**) et qu’il s’agissait du dernier thread du processus en cours.</span><span class="sxs-lookup"><span data-stu-id="0bac2-177">Indicates that a thread attempted to terminate itself by default (called NtTerminateThread with **NULL**) and it was the last thread in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERREUR \_ \_ mm inattendu \_ créer \_ Err**</span><span class="sxs-lookup"><span data-stu-id="0bac2-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR\_UNEXPECTED\_MM\_CREATE\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-179">556 (0x22C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-179">556 (0x22C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-180">Si une erreur MM non définie dans le filtre standard FsRtl est renvoyée, elle est convertie en l’une des erreurs suivantes, qui est garantie comme étant dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="0bac2-180">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="0bac2-181">Dans ce cas, les informations sont perdues, mais le filtre gère correctement l’exception.</span><span class="sxs-lookup"><span data-stu-id="0bac2-181">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**erreur \_ de \_ carte mm inattendue \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**ERROR\_UNEXPECTED\_MM\_MAP\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-183">557 (0x22D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-183">557 (0x22D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-184">Si une erreur MM non définie dans le filtre standard FsRtl est renvoyée, elle est convertie en l’une des erreurs suivantes, qui est garantie comme étant dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="0bac2-184">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="0bac2-185">Dans ce cas, les informations sont perdues, mais le filtre gère correctement l’exception.</span><span class="sxs-lookup"><span data-stu-id="0bac2-185">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERREUR de l' \_ \_ \_ extension mm inattendu \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR\_UNEXPECTED\_MM\_EXTEND\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-187">558 (0x22E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-187">558 (0x22E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-188">Si une erreur MM non définie dans le filtre standard FsRtl est renvoyée, elle est convertie en l’une des erreurs suivantes, qui est garantie comme étant dans le filtre.</span><span class="sxs-lookup"><span data-stu-id="0bac2-188">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="0bac2-189">Dans ce cas, les informations sont perdues, mais le filtre gère correctement l’exception.</span><span class="sxs-lookup"><span data-stu-id="0bac2-189">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERREUR \_ de \_ table de fonction incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR\_BAD\_FUNCTION\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-191">559 (0x22F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-191">559 (0x22F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-192">Une table de fonctions incorrecte a été rencontrée lors d’une opération de déroulement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-192">A malformed function table was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERREUR \_ aucune \_ traduction de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR\_NO\_GUID\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-194">560 (0X230)</span><span class="sxs-lookup"><span data-stu-id="0bac2-194">560 (0x230)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-195">Indique qu’une tentative d’attribution d’une protection à un répertoire ou à un fichier du système de fichiers a été effectuée et que l’un des SID du descripteur de sécurité n’a pas pu être traduit dans un GUID pouvant être stocké par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0bac2-195">Indicates that an attempt was made to assign protection to a file system file or directory and one of the SIDs in the security descriptor could not be translated into a GUID that could be stored by the file system.</span></span> <span data-ttu-id="0bac2-196">Cela provoque l’échec de la tentative de protection, ce qui peut entraîner l’échec d’une tentative de création de fichier.</span><span class="sxs-lookup"><span data-stu-id="0bac2-196">This causes the protection attempt to fail, which may cause a file creation attempt to fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERREUR \_ de \_ taille de LDT non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR\_INVALID\_LDT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-198">561 (0x231)</span><span class="sxs-lookup"><span data-stu-id="0bac2-198">561 (0x231)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-199">Indique qu’une tentative a été effectuée pour augmenter une LDT en définissant sa taille, ou que la taille n’est pas un nombre pair de sélecteurs.</span><span class="sxs-lookup"><span data-stu-id="0bac2-199">Indicates that an attempt was made to grow an LDT by setting its size, or that the size was not an even number of selectors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERREUR \_ de \_ décalage de LDT non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR\_INVALID\_LDT\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-201">563 (0x233)</span><span class="sxs-lookup"><span data-stu-id="0bac2-201">563 (0x233)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-202">Indique que la valeur de départ des informations LDT n’était pas un multiple entier de la taille du sélecteur.</span><span class="sxs-lookup"><span data-stu-id="0bac2-202">Indicates that the starting value for the LDT information was not an integral multiple of the selector size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERREUR \_ de \_ \_ descripteur LDT non valide**</span><span class="sxs-lookup"><span data-stu-id="0bac2-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR\_INVALID\_LDT\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-204">564 (0x234)</span><span class="sxs-lookup"><span data-stu-id="0bac2-204">564 (0x234)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-205">Indique que l’utilisateur a fourni un descripteur non valide lors de la tentative de configuration des descripteurs LDT.</span><span class="sxs-lookup"><span data-stu-id="0bac2-205">Indicates that the user supplied an invalid descriptor when trying to set up Ldt descriptors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERREUR \_ trop \_ grand nombre de \_ threads**</span><span class="sxs-lookup"><span data-stu-id="0bac2-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR\_TOO\_MANY\_THREADS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-207">565 (0x235)</span><span class="sxs-lookup"><span data-stu-id="0bac2-207">565 (0x235)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-208">Indique qu’un processus dispose d’un trop grand nombre de threads pour exécuter l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-208">Indicates a process has too many threads to perform the requested action.</span></span> <span data-ttu-id="0bac2-209">Par exemple, l’assignation d’un jeton principal ne peut être effectuée que lorsqu’un processus a zéro ou un thread.</span><span class="sxs-lookup"><span data-stu-id="0bac2-209">For example, assignment of a primary token may only be performed when a process has zero or one threads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**\_thread \_ d’erreur non dans le \_ \_ processus**</span><span class="sxs-lookup"><span data-stu-id="0bac2-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**ERROR\_THREAD\_NOT\_IN\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-211">566 (0x236)</span><span class="sxs-lookup"><span data-stu-id="0bac2-211">566 (0x236)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-212">Une tentative a été effectuée pour fonctionner sur un thread dans un processus spécifique, mais le thread spécifié n’est pas dans le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="0bac2-212">An attempt was made to operate on a thread within a specific process, but the thread specified is not in the process specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERREUR \_ de \_ dépassement du quota du fichier d’échange \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERROR\_PAGEFILE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-214">567 (0x237)</span><span class="sxs-lookup"><span data-stu-id="0bac2-214">567 (0x237)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-215">Le quota du fichier d’échange a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-215">Page file quota was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERREUR \_ de \_ conflit de serveur d’ouverture de session \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERROR\_LOGON\_SERVER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-217">568 (0x238)</span><span class="sxs-lookup"><span data-stu-id="0bac2-217">568 (0x238)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-218">Le service Netlogon ne peut pas démarrer, car un autre service Netlogon en cours d’exécution dans le domaine est en conflit avec le rôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="0bac2-218">The Netlogon service cannot start because another Netlogon service running in the domain conflicts with the specified role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**synchronisation des erreurs \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="0bac2-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**ERROR\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-220">569 (0x239)</span><span class="sxs-lookup"><span data-stu-id="0bac2-220">569 (0x239)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-221">La base de données SAM sur un serveur Windows n’est pas très synchronisée avec la copie sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="0bac2-221">The SAM database on a Windows Server is significantly out of synchronization with the copy on the Domain Controller.</span></span> <span data-ttu-id="0bac2-222">Une synchronisation complète est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0bac2-222">A complete synchronization is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERREUR \_ NET \_ Open \_ échec**</span><span class="sxs-lookup"><span data-stu-id="0bac2-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR\_NET\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-224">570 (0x23A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-224">570 (0x23A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-225">Échec de l’API NtCreateFile.</span><span class="sxs-lookup"><span data-stu-id="0bac2-225">The NtCreateFile API failed.</span></span> <span data-ttu-id="0bac2-226">Cette erreur ne doit jamais être renvoyée à une application, il s’agit d’un espace réservé pour le redirecteur Windows LAN Manager à utiliser dans ses routines de mappage des erreurs internes.</span><span class="sxs-lookup"><span data-stu-id="0bac2-226">This error should never be returned to an application, it is a place holder for the Windows Lan Manager Redirector to use in its internal error mapping routines.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERREUR \_ d' \_ échec du privilège d’e/s \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR\_IO\_PRIVILEGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-228">571 (0x23B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-228">571 (0x23B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-229">{Échec du privilège} Les autorisations d’e/s pour le processus n’ont pas pu être modifiées.</span><span class="sxs-lookup"><span data-stu-id="0bac2-229">{Privilege Failed} The I/O permissions for the process could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**contrôle d’erreur \_ \_ C \_ Exit**</span><span class="sxs-lookup"><span data-stu-id="0bac2-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR\_CONTROL\_C\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-231">572 (0x23C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-231">572 (0x23C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-232">{Quitter l’application par CTRL + C} L’application s’est arrêtée à la suite d’un CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="0bac2-232">{Application Exit by CTRL+C} The application terminated as a result of a CTRL+C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERREUR \_ manquant \_ SYSTEMFILE**</span><span class="sxs-lookup"><span data-stu-id="0bac2-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR\_MISSING\_SYSTEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-234">573 (0x23D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-234">573 (0x23D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-235">{Fichier système manquant} Le fichier système requis% HS est incorrect ou manquant.</span><span class="sxs-lookup"><span data-stu-id="0bac2-235">{Missing System File} The required system file %hs is bad or missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERREUR d' \_ exception non gérée \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERROR\_UNHANDLED\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-237">574 (0x23E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-237">574 (0x23E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-238">{Erreur d’application} L’exception% s (0x% 08lX) s’est produite dans l’application à l’emplacement 0x% 08lX.</span><span class="sxs-lookup"><span data-stu-id="0bac2-238">{Application Error} The exception %s (0x%08lx) occurred in the application at location 0x%08lx.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**échec de l’initialisation de l’application d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR\_APP\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-240">575 (0x23F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-240">575 (0x23F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-241">{Erreur d’application} L’application n’a pas pu démarrer correctement (0x% LX).</span><span class="sxs-lookup"><span data-stu-id="0bac2-241">{Application Error} The application was unable to start correctly (0x%lx).</span></span> <span data-ttu-id="0bac2-242">Cliquez sur OK pour fermer l’application.</span><span class="sxs-lookup"><span data-stu-id="0bac2-242">Click OK to close the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERREUR lors de la \_ création du fichier d’échange \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR\_PAGEFILE\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-244">576 (0x240)</span><span class="sxs-lookup"><span data-stu-id="0bac2-244">576 (0x240)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-245">{Impossible de créer le fichier d’échange} Échec de la création du fichier d’échange% HS (% LX).</span><span class="sxs-lookup"><span data-stu-id="0bac2-245">{Unable to Create Paging File} The creation of the paging file %hs failed (%lx).</span></span> <span data-ttu-id="0bac2-246">La taille demandée était de% LD.</span><span class="sxs-lookup"><span data-stu-id="0bac2-246">The requested size was %ld.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERREUR \_ de \_ hachage d’image non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR\_INVALID\_IMAGE\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-248">577 (0x241)</span><span class="sxs-lookup"><span data-stu-id="0bac2-248">577 (0x241)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-249">Windows ne peut pas vérifier la signature numérique de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="0bac2-249">Windows cannot verify the digital signature for this file.</span></span> <span data-ttu-id="0bac2-250">Une modification récente du matériel ou des logiciels a peut-être installé un fichier qui est signé de manière incorrecte ou endommagée, ou qui peut être un logiciel malveillant provenant d’une source inconnue.</span><span class="sxs-lookup"><span data-stu-id="0bac2-250">A recent hardware or software change might have installed a file that is signed incorrectly or damaged, or that might be malicious software from an unknown source.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERREUR \_ aucun \_ fichier d’échange**</span><span class="sxs-lookup"><span data-stu-id="0bac2-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR\_NO\_PAGEFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-252">578 (0x242)</span><span class="sxs-lookup"><span data-stu-id="0bac2-252">578 (0x242)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-253">{Aucun fichier d’échange spécifié} Aucun fichier d’échange n’a été spécifié dans la configuration du système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-253">{No Paging File Specified} No paging file was specified in the system configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERREUR \_ de \_ contexte flottant non conforme \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERROR\_ILLEGAL\_FLOAT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-255">579 (0x243)</span><span class="sxs-lookup"><span data-stu-id="0bac2-255">579 (0x243)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-256">TITRE Une application en mode réel a émis une instruction à virgule flottante et un matériel à virgule flottante n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="0bac2-256">{EXCEPTION} A real-mode application issued a floating-point instruction and floating-point hardware is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERREUR \_ aucune \_ paire d’événements \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERROR\_NO\_EVENT\_PAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-258">580 (0x244)</span><span class="sxs-lookup"><span data-stu-id="0bac2-258">580 (0x244)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-259">Une opération de synchronisation de paire d’événements a été effectuée à l’aide de l’objet de paire d’événements client/serveur spécifique au thread, mais aucun objet de paire d’événements n’a été associé au thread.</span><span class="sxs-lookup"><span data-stu-id="0bac2-259">An event pair synchronization operation was performed using the thread specific client/server event pair object, but no event pair object was associated with the thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**\_erreur de \_ configuration du \_ domaine d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**ERROR\_DOMAIN\_CTRLR\_CONFIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-261">581 (0x245)</span><span class="sxs-lookup"><span data-stu-id="0bac2-261">581 (0x245)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-262">La configuration d’un serveur Windows est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="0bac2-262">A Windows Server has an incorrect configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERREUR \_ \_ caractère illégal**</span><span class="sxs-lookup"><span data-stu-id="0bac2-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERROR\_ILLEGAL\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-264">582 (0x246)</span><span class="sxs-lookup"><span data-stu-id="0bac2-264">582 (0x246)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-265">Un caractère non conforme a été rencontré.</span><span class="sxs-lookup"><span data-stu-id="0bac2-265">An illegal character was encountered.</span></span> <span data-ttu-id="0bac2-266">Pour un jeu de caractères multioctets, cela comprend un octet de tête sans l’octet de fin suivant.</span><span class="sxs-lookup"><span data-stu-id="0bac2-266">For a multi-byte character set this includes a lead byte without a succeeding trail byte.</span></span> <span data-ttu-id="0bac2-267">Pour le jeu de caractères Unicode, cela comprend les caractères 0xFFFF et 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="0bac2-267">For the Unicode character set this includes the characters 0xFFFF and 0xFFFE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**\_caractère non défini d' \_ erreur**</span><span class="sxs-lookup"><span data-stu-id="0bac2-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERROR\_UNDEFINED\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-269">583 (0x247)</span><span class="sxs-lookup"><span data-stu-id="0bac2-269">583 (0x247)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-270">Le caractère Unicode n’est pas défini dans le jeu de caractères Unicode installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-270">The Unicode character is not defined in the Unicode character set installed on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**\_volume de disquette d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**ERROR\_FLOPPY\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-272">584 (0x248)</span><span class="sxs-lookup"><span data-stu-id="0bac2-272">584 (0x248)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-273">Le fichier d’échange ne peut pas être créé sur une disquette.</span><span class="sxs-lookup"><span data-stu-id="0bac2-273">The paging file cannot be created on a floppy diskette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**erreur \_ lors \_ \_ de la \_ connexion de l' \_ interruption par le BIOS**</span><span class="sxs-lookup"><span data-stu-id="0bac2-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR\_BIOS\_FAILED\_TO\_CONNECT\_INTERRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-275">585 (0x249)</span><span class="sxs-lookup"><span data-stu-id="0bac2-275">585 (0x249)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-276">Le BIOS du système n’a pas pu connecter une interruption système à l’appareil ou au bus pour lequel l’appareil est connecté.</span><span class="sxs-lookup"><span data-stu-id="0bac2-276">The system BIOS failed to connect a system interrupt to the device or bus for which the device is connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERREUR \_ de \_ contrôleur de sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="0bac2-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERROR\_BACKUP\_CONTROLLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-278">586 (0x24A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-278">586 (0x24A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-279">Cette opération est autorisée uniquement pour le contrôleur de domaine principal du domaine.</span><span class="sxs-lookup"><span data-stu-id="0bac2-279">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERREUR \_ de \_ limite de mutant \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERROR\_MUTANT\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-281">587 (0x24B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-281">587 (0x24B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-282">Une tentative a été effectuée pour acquérir un mutant de telle sorte que son nombre maximal aurait été dépassé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-282">An attempt was made to acquire a mutant such that its maximum count would have been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**pilote d’erreur \_ FS \_ \_ requis**</span><span class="sxs-lookup"><span data-stu-id="0bac2-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR\_FS\_DRIVER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-284">588 (0x24C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-284">588 (0x24C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-285">Un volume a fait l’accès à un pilote de système de fichiers qui n’a pas encore été chargé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-285">A volume has been accessed for which a file system driver is required that has not yet been loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERREUR \_ Impossible de \_ charger le \_ fichier de Registre \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR\_CANNOT\_LOAD\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-287">589 (0x24D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-287">589 (0x24D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-288">{Échec du fichier du Registre} Le registre ne peut pas charger la ruche (fichier) :% HS ou son journal ou un autre fichier journal.</span><span class="sxs-lookup"><span data-stu-id="0bac2-288">{Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate.</span></span> <span data-ttu-id="0bac2-289">Elle est endommagée, absente ou non accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="0bac2-289">It is corrupt, absent, or not writable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERREUR \_ échec du débogage de l' \_ attachement \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR\_DEBUG\_ATTACH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-291">590 (0x24E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-291">590 (0x24E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-292">{Défaillance inattendue dans [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Une erreur inattendue s’est produite lors du traitement d’une demande d’API **DebugActiveProcess** .</span><span class="sxs-lookup"><span data-stu-id="0bac2-292">{Unexpected Failure in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} An unexpected failure occurred while processing a **DebugActiveProcess** API request.</span></span> <span data-ttu-id="0bac2-293">Vous pouvez choisir OK pour mettre fin au processus ou annuler pour ignorer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0bac2-293">You may choose OK to terminate the process, or Cancel to ignore the error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERREUR \_ de \_ processus système \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="0bac2-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERROR\_SYSTEM\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-295">591 (0x24F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-295">591 (0x24F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-296">{Erreur système irrécupérable} Le processus système% HS s’est arrêté de façon inattendue avec l’état 0x% 08X (0x% 08X 0x% 08X).</span><span class="sxs-lookup"><span data-stu-id="0bac2-296">{Fatal System Error} The %hs system process terminated unexpectedly with a status of 0x%08x (0x%08x 0x%08x).</span></span> <span data-ttu-id="0bac2-297">Le système a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="0bac2-297">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**données d’erreur \_ \_ non \_ acceptées**</span><span class="sxs-lookup"><span data-stu-id="0bac2-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**ERROR\_DATA\_NOT\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-299">592 (0x250)</span><span class="sxs-lookup"><span data-stu-id="0bac2-299">592 (0x250)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-300">{Données non acceptées} Le client TDI n’a pas pu traiter les données reçues pendant une indication.</span><span class="sxs-lookup"><span data-stu-id="0bac2-300">{Data Not Accepted} The TDI client could not handle the data received during an indication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERREUR de matériel d’erreur \_ VDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERROR\_VDM\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-302">593 (0x251)</span><span class="sxs-lookup"><span data-stu-id="0bac2-302">593 (0x251)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-303">NTVDM a rencontré une erreur matérielle.</span><span class="sxs-lookup"><span data-stu-id="0bac2-303">NTVDM encountered a hard error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**\_ \_ \_ délai d’annulation du pilote d’erreur**</span><span class="sxs-lookup"><span data-stu-id="0bac2-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**ERROR\_DRIVER\_CANCEL\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-305">594 (0x252)</span><span class="sxs-lookup"><span data-stu-id="0bac2-305">594 (0x252)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-306">{Cancel Timeout} Le pilote% HS n’a pas pu terminer une requête d’e/s annulée dans le délai imparti.</span><span class="sxs-lookup"><span data-stu-id="0bac2-306">{Cancel Timeout} The driver %hs failed to complete a cancelled I/O request in the allotted time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**incompatibilité de message de réponse d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR\_REPLY\_MESSAGE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-308">595 (0x253)</span><span class="sxs-lookup"><span data-stu-id="0bac2-308">595 (0x253)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-309">{Concordance des messages de réponse} Une tentative de réponse à un message LPC a été effectuée, mais le thread spécifié par l’ID client dans le message n’attendait pas ce message.</span><span class="sxs-lookup"><span data-stu-id="0bac2-309">{Reply Message Mismatch} An attempt was made to reply to an LPC message, but the thread specified by the client ID in the message was not waiting on that message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERREUR de \_ perte de \_ \_ données WRITEBEHIND**</span><span class="sxs-lookup"><span data-stu-id="0bac2-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-311">596 (0x254)</span><span class="sxs-lookup"><span data-stu-id="0bac2-311">596 (0x254)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-312">{Échec de l’écriture différée} Windows n’a pas pu enregistrer toutes les données du fichier% HS.</span><span class="sxs-lookup"><span data-stu-id="0bac2-312">{Delayed Write Failed} Windows was unable to save all the data for the file %hs.</span></span> <span data-ttu-id="0bac2-313">Les données ont été perdues.</span><span class="sxs-lookup"><span data-stu-id="0bac2-313">The data has been lost.</span></span> <span data-ttu-id="0bac2-314">Cette erreur peut être due à une défaillance du matériel de votre ordinateur ou de la connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="0bac2-314">This error may be caused by a failure of your computer hardware or network connection.</span></span> <span data-ttu-id="0bac2-315">Essayez d’enregistrer ce fichier ailleurs.</span><span class="sxs-lookup"><span data-stu-id="0bac2-315">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERREUR \_ de \_ paramètres du serveur client \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="0bac2-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR\_CLIENT\_SERVER\_PARAMETERS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-317">597 (0x255)</span><span class="sxs-lookup"><span data-stu-id="0bac2-317">597 (0x255)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-318">Le ou les paramètres transmis au serveur dans la fenêtre de mémoire partagée client/serveur ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="0bac2-318">The parameter(s) passed to the server in the client/server shared memory window were invalid.</span></span> <span data-ttu-id="0bac2-319">Une trop grande quantité de données a peut-être été placée dans la fenêtre mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-319">Too much data may have been put in the shared memory window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERREUR \_ de \_ flux non Tiny \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR\_NOT\_TINY\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-321">598 (0x256)</span><span class="sxs-lookup"><span data-stu-id="0bac2-321">598 (0x256)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-322">Le flux n’est pas un flux minuscule.</span><span class="sxs-lookup"><span data-stu-id="0bac2-322">The stream is not a tiny stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**dépassement de la pile des erreurs \_ \_ \_ en lecture**</span><span class="sxs-lookup"><span data-stu-id="0bac2-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR\_STACK\_OVERFLOW\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-324">599 (0x257)</span><span class="sxs-lookup"><span data-stu-id="0bac2-324">599 (0x257)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-325">La requête doit être gérée par le code de dépassement de capacité de la pile.</span><span class="sxs-lookup"><span data-stu-id="0bac2-325">The request must be handled by the stack overflow code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERREUR \_ \_ de conversion en \_ grande**</span><span class="sxs-lookup"><span data-stu-id="0bac2-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR\_CONVERT\_TO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-327">600 (0x258)</span><span class="sxs-lookup"><span data-stu-id="0bac2-327">600 (0x258)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-328">Codes d’État OFS internes indiquant comment une opération d’allocation est gérée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-328">Internal OFS status codes indicating how an allocation operation is handled.</span></span> <span data-ttu-id="0bac2-329">Soit une nouvelle tentative est effectuée après le déplacement du onode conteneur, soit le flux d’étendue est converti en un flux volumineux.</span><span class="sxs-lookup"><span data-stu-id="0bac2-329">Either it is retried after the containing onode is moved or the extent stream is converted to a large stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERREUR \_ trouvée \_ hors \_ de l' \_ étendue**</span><span class="sxs-lookup"><span data-stu-id="0bac2-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR\_FOUND\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-331">601 (0x259)</span><span class="sxs-lookup"><span data-stu-id="0bac2-331">601 (0x259)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-332">La tentative de recherche de l’objet a trouvé un objet correspondant à l’ID sur le volume, mais il n’est pas dans l’étendue du descripteur utilisé pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="0bac2-332">The attempt to find the object found an object matching by ID on the volume but it is out of the scope of the handle used for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERREUR d' \_ allocation du \_ compartiment**</span><span class="sxs-lookup"><span data-stu-id="0bac2-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR\_ALLOCATE\_BUCKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-334">602 (0x25A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-334">602 (0x25A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-335">Le tableau de compartiments doit être augmenté.</span><span class="sxs-lookup"><span data-stu-id="0bac2-335">The bucket array must be grown.</span></span> <span data-ttu-id="0bac2-336">Nouvelle tentative de transaction.</span><span class="sxs-lookup"><span data-stu-id="0bac2-336">Retry transaction after doing so.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERREUR de \_ marshaling de \_ dépassement**</span><span class="sxs-lookup"><span data-stu-id="0bac2-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERROR\_MARSHALL\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-338">603 (0x25B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-338">603 (0x25B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-339">La mémoire tampon de marshaling utilisateur/noyau a débordé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-339">The user/kernel marshalling buffer has overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERREUR \_ Variant non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR\_INVALID\_VARIANT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-341">604 (0x25C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-341">604 (0x25C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-342">La structure de variante fournie contient des données non valides.</span><span class="sxs-lookup"><span data-stu-id="0bac2-342">The supplied variant structure contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERREUR \_ de \_ mémoire tampon de compression incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR\_BAD\_COMPRESSION\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-344">605 (0x25D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-344">605 (0x25D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-345">La mémoire tampon spécifiée contient des données incorrectes.</span><span class="sxs-lookup"><span data-stu-id="0bac2-345">The specified buffer contains ill-formed data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**\_échec de l’audit d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR\_AUDIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-347">606 (0x25E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-347">606 (0x25E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-348">{Échec de l’audit} Une tentative de génération d’un audit de sécurité a échoué.</span><span class="sxs-lookup"><span data-stu-id="0bac2-348">{Audit Failed} An attempt to generate a security audit failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**résolution de l’horloge d’erreur \_ \_ \_ non \_ définie**</span><span class="sxs-lookup"><span data-stu-id="0bac2-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**ERROR\_TIMER\_RESOLUTION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-350">607 (0x25F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-350">607 (0x25F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-351">La résolution de la minuterie n’a pas été définie précédemment par le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="0bac2-351">The timer resolution was not previously set by the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERREUR \_ \_ d’informations d’ouverture de session insuffisantes \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR\_INSUFFICIENT\_LOGON\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-353">608 (0x260)</span><span class="sxs-lookup"><span data-stu-id="0bac2-353">608 (0x260)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-354">Les informations de compte sont insuffisantes pour vous connecter.</span><span class="sxs-lookup"><span data-stu-id="0bac2-354">There is insufficient account information to log you on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERREUR \_ de \_ point d’entrée de dll erroné \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR\_BAD\_DLL\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-356">609 (0x261)</span><span class="sxs-lookup"><span data-stu-id="0bac2-356">609 (0x261)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-357">{EntryPoint DLL non valide} La bibliothèque de liens dynamiques% HS n’est pas écrite correctement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-357">{Invalid DLL Entrypoint} The dynamic link library %hs is not written correctly.</span></span> <span data-ttu-id="0bac2-358">Le pointeur de pile a été laissé dans un état incohérent.</span><span class="sxs-lookup"><span data-stu-id="0bac2-358">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="0bac2-359">Le point d’entrée doit être déclaré en tant que WINAPI ou STDCALL.</span><span class="sxs-lookup"><span data-stu-id="0bac2-359">The entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="0bac2-360">Sélectionnez Oui pour faire échouer le chargement de la DLL.</span><span class="sxs-lookup"><span data-stu-id="0bac2-360">Select YES to fail the DLL load.</span></span> <span data-ttu-id="0bac2-361">Sélectionnez non pour poursuivre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0bac2-361">Select NO to continue execution.</span></span> <span data-ttu-id="0bac2-362">La sélection de l’option non peut entraîner un fonctionnement incorrect de l’application.</span><span class="sxs-lookup"><span data-stu-id="0bac2-362">Selecting NO may cause the application to operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERREUR \_ de \_ point d’entrée de service incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR\_BAD\_SERVICE\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-364">610 (0x262)</span><span class="sxs-lookup"><span data-stu-id="0bac2-364">610 (0x262)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-365">{Point d’entrée de rappel de service non valide} Le service% HS n’est pas écrit correctement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-365">{Invalid Service Callback Entrypoint} The %hs service is not written correctly.</span></span> <span data-ttu-id="0bac2-366">Le pointeur de pile a été laissé dans un état incohérent.</span><span class="sxs-lookup"><span data-stu-id="0bac2-366">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="0bac2-367">Le point d’entrée de rappel doit être déclaré en tant que WINAPI ou STDCALL.</span><span class="sxs-lookup"><span data-stu-id="0bac2-367">The callback entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="0bac2-368">Si vous sélectionnez OK, le service continue de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="0bac2-368">Selecting OK will cause the service to continue operation.</span></span> <span data-ttu-id="0bac2-369">Toutefois, le processus de service peut ne pas fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-369">However, the service process may operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERREUR \_ d' \_ adresse IP \_ CONFLICT1**</span><span class="sxs-lookup"><span data-stu-id="0bac2-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR\_IP\_ADDRESS\_CONFLICT1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-371">611 (0x263)</span><span class="sxs-lookup"><span data-stu-id="0bac2-371">611 (0x263)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-372">Il existe un conflit d’adresse IP avec un autre système sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="0bac2-372">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERREUR \_ d' \_ adresse IP \_ CONFLICT2**</span><span class="sxs-lookup"><span data-stu-id="0bac2-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR\_IP\_ADDRESS\_CONFLICT2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-374">612 (0x264)</span><span class="sxs-lookup"><span data-stu-id="0bac2-374">612 (0x264)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-375">Il existe un conflit d’adresse IP avec un autre système sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="0bac2-375">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_limite de \_ quota du registre des erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**ERROR\_REGISTRY\_QUOTA\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-377">613 (0x265)</span><span class="sxs-lookup"><span data-stu-id="0bac2-377">613 (0x265)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-378">{Espace du Registre insuffisant} Le système a atteint la taille maximale autorisée pour la partie système du Registre.</span><span class="sxs-lookup"><span data-stu-id="0bac2-378">{Low On Registry Space} The system has reached the maximum size allowed for the system part of the registry.</span></span> <span data-ttu-id="0bac2-379">Les demandes de stockage supplémentaires seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="0bac2-379">Additional storage requests will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERREUR \_ aucun \_ rappel \_ actif**</span><span class="sxs-lookup"><span data-stu-id="0bac2-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR\_NO\_CALLBACK\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-381">614 (0x266)</span><span class="sxs-lookup"><span data-stu-id="0bac2-381">614 (0x266)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-382">Impossible d’exécuter un service système de retour de rappel quand aucun rappel n’est actif.</span><span class="sxs-lookup"><span data-stu-id="0bac2-382">A callback return system service cannot be executed when no callback is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERREUR \_ Pwd \_ trop \_ brève**</span><span class="sxs-lookup"><span data-stu-id="0bac2-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR\_PWD\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-384">615 (0x267)</span><span class="sxs-lookup"><span data-stu-id="0bac2-384">615 (0x267)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-385">Le mot de passe fourni est trop petit pour respecter la stratégie de votre compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0bac2-385">The password provided is too short to meet the policy of your user account.</span></span> <span data-ttu-id="0bac2-386">Veuillez choisir un mot de passe plus long.</span><span class="sxs-lookup"><span data-stu-id="0bac2-386">Please choose a longer password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERREUR \_ Pwd \_ trop \_ récente**</span><span class="sxs-lookup"><span data-stu-id="0bac2-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR\_PWD\_TOO\_RECENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-388">616 (0x268)</span><span class="sxs-lookup"><span data-stu-id="0bac2-388">616 (0x268)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-389">La stratégie de votre compte d’utilisateur ne vous permet pas de modifier les mots de passe trop fréquemment.</span><span class="sxs-lookup"><span data-stu-id="0bac2-389">The policy of your user account does not allow you to change passwords too frequently.</span></span> <span data-ttu-id="0bac2-390">Cela permet d’empêcher les utilisateurs de revenir à un mot de passe connu, mais potentiellement découvert.</span><span class="sxs-lookup"><span data-stu-id="0bac2-390">This is done to prevent users from changing back to a familiar, but potentially discovered, password.</span></span> <span data-ttu-id="0bac2-391">Si vous pensez que votre mot de passe a été compromis, contactez immédiatement votre administrateur pour lui attribuer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="0bac2-391">If you feel your password has been compromised then please contact your administrator immediately to have a new one assigned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERREUR \_ de \_ conflit historique pwd \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERROR\_PWD\_HISTORY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-393">617 (0x269)</span><span class="sxs-lookup"><span data-stu-id="0bac2-393">617 (0x269)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-394">Vous avez tenté de remplacer votre mot de passe par un mot de passe que vous avez utilisé par le passé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-394">You have attempted to change your password to one that you have used in the past.</span></span> <span data-ttu-id="0bac2-395">La stratégie de votre compte d’utilisateur ne l’autorise pas.</span><span class="sxs-lookup"><span data-stu-id="0bac2-395">The policy of your user account does not allow this.</span></span> <span data-ttu-id="0bac2-396">Veuillez sélectionner un mot de passe que vous n’avez pas utilisé précédemment.</span><span class="sxs-lookup"><span data-stu-id="0bac2-396">Please select a password that you have not previously used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERREUR de \_ compression non prise en charge \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR\_UNSUPPORTED\_COMPRESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-398">618 (0x26A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-398">618 (0x26A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-399">Le format de compression spécifié n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0bac2-399">The specified compression format is unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERREUR \_ \_ Profil matériel non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR\_INVALID\_HW\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-401">619 (0x26B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-401">619 (0x26B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-402">La configuration du profil matériel spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0bac2-402">The specified hardware profile configuration is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERREUR de chemin de l' \_ \_ appareil PLUGPLAY non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR\_INVALID\_PLUGPLAY\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-404">620 (0x26C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-404">620 (0x26C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-405">Le chemin d’accès de l’appareil du Registre Plug-and-Play spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0bac2-405">The specified Plug and Play registry device path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**Liste des quotas d’erreurs \_ \_ \_ incohérente**</span><span class="sxs-lookup"><span data-stu-id="0bac2-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**ERROR\_QUOTA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-407">621 (0x26D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-407">621 (0x26D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-408">La liste de quotas spécifiée est incohérente en interne avec son descripteur.</span><span class="sxs-lookup"><span data-stu-id="0bac2-408">The specified quota list is internally inconsistent with its descriptor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**EXPIRATION de l’évaluation de l’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**ERROR\_EVALUATION\_EXPIRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-410">622 (0x26E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-410">622 (0x26E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-411">{Notification d’évaluation Windows} La période d’évaluation de cette installation de Windows a expiré.</span><span class="sxs-lookup"><span data-stu-id="0bac2-411">{Windows Evaluation Notification} The evaluation period for this installation of Windows has expired.</span></span> <span data-ttu-id="0bac2-412">Ce système s’arrêtera dans 1 heure.</span><span class="sxs-lookup"><span data-stu-id="0bac2-412">This system will shutdown in 1 hour.</span></span> <span data-ttu-id="0bac2-413">Pour restaurer l’accès à cette installation de Windows, mettez à niveau cette installation à l’aide d’une distribution sous licence de ce produit.</span><span class="sxs-lookup"><span data-stu-id="0bac2-413">To restore access to this installation of Windows, please upgrade this installation using a licensed distribution of this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERREUR \_ de \_ réadressage de dll non conforme \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR\_ILLEGAL\_DLL\_RELOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-415">623 (0x26F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-415">623 (0x26F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-416">{Réadressage de DLL système non conforme} La DLL système% HS a été déplacée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="0bac2-416">{Illegal System DLL Relocation} The system DLL %hs was relocated in memory.</span></span> <span data-ttu-id="0bac2-417">L’application ne s’exécutera pas correctement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-417">The application will not run properly.</span></span> <span data-ttu-id="0bac2-418">Le réadressage s’est produit parce que la DLL% HS occupait une plage d’adresses réservée aux DLL système Windows.</span><span class="sxs-lookup"><span data-stu-id="0bac2-418">The relocation occurred because the DLL %hs occupied an address range reserved for Windows system DLLs.</span></span> <span data-ttu-id="0bac2-419">Le fournisseur qui fournit la DLL doit être contacté pour obtenir une nouvelle DLL.</span><span class="sxs-lookup"><span data-stu-id="0bac2-419">The vendor supplying the DLL should be contacted for a new DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**échec de l’initialisation de la dll d’erreur \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR\_DLL\_INIT\_FAILED\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-421">624 (0x270)</span><span class="sxs-lookup"><span data-stu-id="0bac2-421">624 (0x270)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-422">{Échec de l’initialisation de la DLL} L’application n’a pas pu s’initialiser en raison de l’arrêt de la station Windows.</span><span class="sxs-lookup"><span data-stu-id="0bac2-422">{DLL Initialization Failed} The application failed to initialize because the window station is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERREUR de validation de la \_ \_ poursuite**</span><span class="sxs-lookup"><span data-stu-id="0bac2-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR\_VALIDATE\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-424">625 (0x271)</span><span class="sxs-lookup"><span data-stu-id="0bac2-424">625 (0x271)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-425">Le processus de validation doit passer à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="0bac2-425">The validation process needs to continue on to the next step.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERREUR \_ \_ plus aucune \_ correspondance**</span><span class="sxs-lookup"><span data-stu-id="0bac2-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR\_NO\_MORE\_MATCHES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-427">626 (0x272)</span><span class="sxs-lookup"><span data-stu-id="0bac2-427">626 (0x272)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-428">Il n’y a plus de correspondances pour l’énumération d’index actuelle.</span><span class="sxs-lookup"><span data-stu-id="0bac2-428">There are no more matches for the current index enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_conflit de \_ liste de plages d’erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**ERROR\_RANGE\_LIST\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-430">627 (0x273)</span><span class="sxs-lookup"><span data-stu-id="0bac2-430">627 (0x273)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-431">La plage n’a pas pu être ajoutée à la liste de plages en raison d’un conflit.</span><span class="sxs-lookup"><span data-stu-id="0bac2-431">The range could not be added to the range list because of a conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**incompatibilité de SID de serveur d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR\_SERVER\_SID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-433">628 (0x274)</span><span class="sxs-lookup"><span data-stu-id="0bac2-433">628 (0x274)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-434">Le processus serveur s’exécute sous un SID différent de celui requis par le client.</span><span class="sxs-lookup"><span data-stu-id="0bac2-434">The server process is running under a SID different than that required by client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERREUR \_ Impossible d' \_ activer \_ Deny \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="0bac2-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR\_CANT\_ENABLE\_DENY\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-436">629 (0x275)</span><span class="sxs-lookup"><span data-stu-id="0bac2-436">629 (0x275)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-437">Il n’est pas possible d’activer un groupe marqué utiliser pour un refus uniquement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-437">A group marked use for deny only cannot be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERREUR \_ - \_ plusieurs \_ Erreurs flottantes**</span><span class="sxs-lookup"><span data-stu-id="0bac2-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR\_FLOAT\_MULTIPLE\_FAULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-439">630 (0x276)</span><span class="sxs-lookup"><span data-stu-id="0bac2-439">630 (0x276)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-440">TITRE Erreurs à virgule flottante multiples.</span><span class="sxs-lookup"><span data-stu-id="0bac2-440">{EXCEPTION} Multiple floating point faults.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERREUR \_ flottant \_ plusieurs \_ interruptions**</span><span class="sxs-lookup"><span data-stu-id="0bac2-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR\_FLOAT\_MULTIPLE\_TRAPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-442">631 (0x277)</span><span class="sxs-lookup"><span data-stu-id="0bac2-442">631 (0x277)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-443">TITRE Interruptions multiples à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="0bac2-443">{EXCEPTION} Multiple floating point traps.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERREUR \_ NOinterface**</span><span class="sxs-lookup"><span data-stu-id="0bac2-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR\_NOINTERFACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-445">632 (0x278)</span><span class="sxs-lookup"><span data-stu-id="0bac2-445">632 (0x278)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-446">L’interface demandée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0bac2-446">The requested interface is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**échec de la mise en veille du pilote d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR\_DRIVER\_FAILED\_SLEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-448">633 (0x279)</span><span class="sxs-lookup"><span data-stu-id="0bac2-448">633 (0x279)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-449">{Échec du système de mise en veille} Le pilote% HS ne prend pas en charge le mode veille.</span><span class="sxs-lookup"><span data-stu-id="0bac2-449">{System Standby Failed} The driver %hs does not support standby mode.</span></span> <span data-ttu-id="0bac2-450">La mise à jour de ce pilote peut permettre au système de passer en mode veille.</span><span class="sxs-lookup"><span data-stu-id="0bac2-450">Updating this driver may allow the system to go to standby mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERREUR \_ de \_ fichier système endommagé \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR\_CORRUPT\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-452">634 (0x27A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-452">634 (0x27A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-453">Le fichier système %1 est devenu endommagé et a été remplacé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-453">The system file %1 has become corrupt and has been replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**ERREUR d' \_ engagement \_ minimum**</span><span class="sxs-lookup"><span data-stu-id="0bac2-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**ERROR\_COMMITMENT\_MINIMUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-455">635 (0x27B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-455">635 (0x27B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-456">{Mémoire virtuelle minimale trop faible} La mémoire virtuelle de votre système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="0bac2-456">{Virtual Memory Minimum Too Low} Your system is low on virtual memory.</span></span> <span data-ttu-id="0bac2-457">Windows est l’extension de la taille de votre fichier d’échange de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0bac2-457">Windows is increasing the size of your virtual memory paging file.</span></span> <span data-ttu-id="0bac2-458">Pendant ce processus, les demandes de mémoire pour certaines applications peuvent être refusées.</span><span class="sxs-lookup"><span data-stu-id="0bac2-458">During this process, memory requests for some applications may be denied.</span></span> <span data-ttu-id="0bac2-459">Pour plus d’informations, consultez l’aide de.</span><span class="sxs-lookup"><span data-stu-id="0bac2-459">For more information, see Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERREUR \_ d' \_ énumération du redémarrage PNP \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR\_PNP\_RESTART\_ENUMERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-461">636 (0x27C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-461">636 (0x27C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-462">Un appareil a été supprimé. l’énumération doit donc être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-462">A device was removed so enumeration must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERREUR \_ de \_ \_ signature incorrecte de l’image système \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERROR\_SYSTEM\_IMAGE\_BAD\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-464">637 (0x27D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-464">637 (0x27D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-465">{Erreur système irrécupérable} L’image système% s n’est pas correctement signée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-465">{Fatal System Error} The system image %s is not properly signed.</span></span> <span data-ttu-id="0bac2-466">Le fichier a été remplacé par le fichier signé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-466">The file has been replaced with the signed file.</span></span> <span data-ttu-id="0bac2-467">Le système a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="0bac2-467">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERREUR \_ de \_ redémarrage PNP \_ requis**</span><span class="sxs-lookup"><span data-stu-id="0bac2-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR\_PNP\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-469">638 (0x27E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-469">638 (0x27E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-470">L’appareil ne démarre pas sans redémarrage.</span><span class="sxs-lookup"><span data-stu-id="0bac2-470">Device will not start without a reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERREUR \_ d’alimentation insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR\_INSUFFICIENT\_POWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-472">639 (0x27F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-472">639 (0x27F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-473">Il n’y a pas suffisamment de puissance pour terminer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-473">There is not enough power to complete the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERREUR \_ - \_ violation de plusieurs erreurs \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR\_MULTIPLE\_FAULT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-475">640 (0x280)</span><span class="sxs-lookup"><span data-stu-id="0bac2-475">640 (0x280)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-476">ERREUR \_ - \_ violation de plusieurs erreurs \_</span><span class="sxs-lookup"><span data-stu-id="0bac2-476">ERROR\_MULTIPLE\_FAULT\_VIOLATION</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERREUR lors de l' \_ arrêt du système \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-478">641 (0x281)</span><span class="sxs-lookup"><span data-stu-id="0bac2-478">641 (0x281)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-479">Le système est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="0bac2-479">The system is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**PORT d’erreur \_ \_ non \_ défini**</span><span class="sxs-lookup"><span data-stu-id="0bac2-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**ERROR\_PORT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-481">642 (0x282)</span><span class="sxs-lookup"><span data-stu-id="0bac2-481">642 (0x282)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-482">Une tentative de suppression d’un processus a été effectuée, mais aucun port n’est déjà associé au processus.</span><span class="sxs-lookup"><span data-stu-id="0bac2-482">An attempt to remove a processes DebugPort was made, but a port was not already associated with the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERREUR de vérification de la \_ version du service d’annuaire \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR\_DS\_VERSION\_CHECK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-484">643 (0x283)</span><span class="sxs-lookup"><span data-stu-id="0bac2-484">643 (0x283)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-485">Cette version de Windows n’est pas compatible avec la version de comportement de la forêt de l’annuaire, du domaine ou du contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="0bac2-485">This version of Windows is not compatible with the behavior version of directory forest, domain or domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_plage d' \_ Erreurs \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="0bac2-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**ERROR\_RANGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-487">644 (0x284)</span><span class="sxs-lookup"><span data-stu-id="0bac2-487">644 (0x284)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-488">La plage spécifiée est introuvable dans la liste des plages.</span><span class="sxs-lookup"><span data-stu-id="0bac2-488">The specified range could not be found in the range list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERREUR de \_ non- \_ \_ pilote en mode sans échec \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR\_NOT\_SAFE\_MODE\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-490">646 (0x286)</span><span class="sxs-lookup"><span data-stu-id="0bac2-490">646 (0x286)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-491">Le pilote n’a pas été chargé, car le système démarre en mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="0bac2-491">The driver was not loaded because the system is booting into safe mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERREUR lors de l' \_ \_ entrée du pilote \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR\_FAILED\_DRIVER\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-493">647 (0x287)</span><span class="sxs-lookup"><span data-stu-id="0bac2-493">647 (0x287)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-494">Le pilote n’a pas été chargé car son appel d’initialisation a échoué.</span><span class="sxs-lookup"><span data-stu-id="0bac2-494">The driver was not loaded because it failed its initialization call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**erreur \_ d' \_ énumération des périphériques d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**ERROR\_DEVICE\_ENUMERATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-496">648 (0x288)</span><span class="sxs-lookup"><span data-stu-id="0bac2-496">648 (0x288)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-497">« % HS » a rencontré une erreur lors de l’application de la puissance ou de la lecture de la configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0bac2-497">The "%hs" encountered an error while applying power or reading the device configuration.</span></span> <span data-ttu-id="0bac2-498">Cela peut être dû à une défaillance de votre matériel ou à une mauvaise connexion.</span><span class="sxs-lookup"><span data-stu-id="0bac2-498">This may be caused by a failure of your hardware or by a poor connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**POINT de montage d’erreur \_ \_ \_ non \_ résolu**</span><span class="sxs-lookup"><span data-stu-id="0bac2-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**ERROR\_MOUNT\_POINT\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-500">649 (0x289)</span><span class="sxs-lookup"><span data-stu-id="0bac2-500">649 (0x289)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-501">L’opération de création a échoué, car le nom contenait au moins un point de montage qui correspond à un volume auquel l’objet périphérique spécifié n’est pas attaché.</span><span class="sxs-lookup"><span data-stu-id="0bac2-501">The create operation failed because the name contained at least one mount point which resolves to a volume to which the specified device object is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERREUR \_ de \_ \_ paramètre d’objet appareil non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR\_INVALID\_DEVICE\_OBJECT\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-503">650 (0x28A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-503">650 (0x28A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-504">Le paramètre d’objet d’appareil n’est pas un objet d’appareil valide ou n’est pas attaché au volume spécifié par le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="0bac2-504">The device object parameter is either not a valid device object or is not attached to the volume specified by the file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**une erreur MCA s’est \_ \_ produite**</span><span class="sxs-lookup"><span data-stu-id="0bac2-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR\_MCA\_OCCURED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-506">651 (0x28B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-506">651 (0x28B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-507">Une erreur de vérification de l’ordinateur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0bac2-507">A Machine Check Error has occurred.</span></span> <span data-ttu-id="0bac2-508">Pour plus d’informations, consultez le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-508">Please check the system eventlog for additional information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**erreur \_ \_ de base de données du pilote d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**ERROR\_DRIVER\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-510">652 (0x28C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-510">652 (0x28C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-511">Une erreur %2 s’est produite pendant \[ \] le traitement de la base de données du pilote.</span><span class="sxs-lookup"><span data-stu-id="0bac2-511">There was error \[%2\] processing the driver database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ruche du système d’erreur \_ \_ \_ trop \_ grande**</span><span class="sxs-lookup"><span data-stu-id="0bac2-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ERROR\_SYSTEM\_HIVE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-513">653 (0x28D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-513">653 (0x28D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-514">La taille de la ruche système a dépassé sa limite.</span><span class="sxs-lookup"><span data-stu-id="0bac2-514">System hive size has exceeded its limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**\_échec du \_ \_ \_ déchargement préalable du pilote d’erreur**</span><span class="sxs-lookup"><span data-stu-id="0bac2-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR\_DRIVER\_FAILED\_PRIOR\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-516">654 (0x28E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-516">654 (0x28E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-517">Le pilote n’a pas pu être chargé car une version précédente du pilote est toujours en mémoire.</span><span class="sxs-lookup"><span data-stu-id="0bac2-517">The driver could not be loaded because a previous version of the driver is still in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERREUR \_ VOLSNAP \_ préparer la \_ mise en veille prolongée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR\_VOLSNAP\_PREPARE\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-519">655 (0x28F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-519">655 (0x28F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-520">{Service VSS} Veuillez patienter pendant que le Service VSS prépare le volume% HS pour la mise en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-520">{Volume Shadow Copy Service} Please wait while the Volume Shadow Copy Service prepares volume %hs for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERREUR de \_ mise en veille prolongée \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR\_HIBERNATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-522">656 (0x290)</span><span class="sxs-lookup"><span data-stu-id="0bac2-522">656 (0x290)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-523">Le système n’a pas pu se mettre en veille prolongée (le code d’erreur est% HS).</span><span class="sxs-lookup"><span data-stu-id="0bac2-523">The system has failed to hibernate (The error code is %hs).</span></span> <span data-ttu-id="0bac2-524">La mise en veille prolongée est désactivée jusqu’au redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-524">Hibernation will be disabled until the system is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERREUR \_ Pwd \_ trop \_ longue**</span><span class="sxs-lookup"><span data-stu-id="0bac2-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR\_PWD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-526">657 (0x291)</span><span class="sxs-lookup"><span data-stu-id="0bac2-526">657 (0x291)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-527">Le mot de passe fourni est trop long pour respecter la stratégie de votre compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0bac2-527">The password provided is too long to meet the policy of your user account.</span></span> <span data-ttu-id="0bac2-528">Veuillez choisir un mot de passe plus petit.</span><span class="sxs-lookup"><span data-stu-id="0bac2-528">Please choose a shorter password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_limitation du \_ système de fichiers d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**ERROR\_FILE\_SYSTEM\_LIMITATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-530">665 (0x299)</span><span class="sxs-lookup"><span data-stu-id="0bac2-530">665 (0x299)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-531">Impossible de terminer l’opération demandée du fait d’une limitation du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0bac2-531">The requested operation could not be completed due to a file system limitation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**\_échec d’assertion d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERROR\_ASSERTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-533">668 (0x29C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-533">668 (0x29C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-534">Un échec d’assertion s’est produit.</span><span class="sxs-lookup"><span data-stu-id="0bac2-534">An assertion failure has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**erreur \_ ACPI \_ erreur**</span><span class="sxs-lookup"><span data-stu-id="0bac2-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**ERROR\_ACPI\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-536">669 (0x29D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-536">669 (0x29D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-537">Une erreur s’est produite dans le sous-système ACPI.</span><span class="sxs-lookup"><span data-stu-id="0bac2-537">An error occurred in the ACPI subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERREUR \_ d' \_ assertion WOW**</span><span class="sxs-lookup"><span data-stu-id="0bac2-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERROR\_WOW\_ASSERTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-539">670 (0x29E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-539">670 (0x29E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-540">Erreur d’assertion WOW.</span><span class="sxs-lookup"><span data-stu-id="0bac2-540">WOW Assertion Error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERREUR \_ PNP \_ \_ table MPS incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR\_PNP\_BAD\_MPS\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-542">671 (0x29F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-542">671 (0x29F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-543">Il manque un appareil dans la table MPS du BIOS système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-543">A device is missing in the system BIOS MPS table.</span></span> <span data-ttu-id="0bac2-544">Ce périphérique ne sera pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-544">This device will not be used.</span></span> <span data-ttu-id="0bac2-545">Contactez le fournisseur de votre système pour obtenir la mise à jour du BIOS système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-545">Please contact your system vendor for system BIOS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERREUR \_ échec de la \_ traduction PNP \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR\_PNP\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-547">672 (0x2A0)</span><span class="sxs-lookup"><span data-stu-id="0bac2-547">672 (0x2A0)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-548">Un traducteur n’a pas réussi à traduire les ressources.</span><span class="sxs-lookup"><span data-stu-id="0bac2-548">A translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERREUR \_ échec de la \_ traduction IRQ PNP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR\_PNP\_IRQ\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-550">673 (0x2A1)</span><span class="sxs-lookup"><span data-stu-id="0bac2-550">673 (0x2A1)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-551">Un traducteur d’IRQ n’a pas pu traduire les ressources.</span><span class="sxs-lookup"><span data-stu-id="0bac2-551">A IRQ translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERREUR \_ PNP \_ ID non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR\_PNP\_INVALID\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-553">674 (0x2A2)</span><span class="sxs-lookup"><span data-stu-id="0bac2-553">674 (0x2A2)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-554">Le pilote %2 a retourné un ID non valide pour un appareil enfant (%3).</span><span class="sxs-lookup"><span data-stu-id="0bac2-554">Driver %2 returned invalid ID for a child device (%3).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERREUR de \_ sortie du \_ \_ débogueur système**</span><span class="sxs-lookup"><span data-stu-id="0bac2-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERROR\_WAKE\_SYSTEM\_DEBUGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-556">675 (0x2A3)</span><span class="sxs-lookup"><span data-stu-id="0bac2-556">675 (0x2A3)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-557">{Le débogueur du noyau est réveillé} le débogueur système a été réveillé par une interruption.</span><span class="sxs-lookup"><span data-stu-id="0bac2-557">{Kernel Debugger Awakened} the system debugger was awakened by an interrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**\_Handles d’erreur \_ fermés**</span><span class="sxs-lookup"><span data-stu-id="0bac2-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**ERROR\_HANDLES\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-559">676 (0x2A4)</span><span class="sxs-lookup"><span data-stu-id="0bac2-559">676 (0x2A4)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-560">{Handles fermés} Les handles des objets ont été fermés automatiquement à la suite de l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-560">{Handles Closed} Handles to objects have been automatically closed as a result of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**ERREUR \_ informations superflues \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**ERROR\_EXTRANEOUS\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-562">677 (0x2A5)</span><span class="sxs-lookup"><span data-stu-id="0bac2-562">677 (0x2A5)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-563">{Trop d’informations} La liste de contrôle d’accès (ACL) spécifiée contient plus d’informations que prévu.</span><span class="sxs-lookup"><span data-stu-id="0bac2-563">{Too Much Information} The specified access control list (ACL) contained more information than was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERREUR \_ RXACT \_ validation \_ nécessaire**</span><span class="sxs-lookup"><span data-stu-id="0bac2-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR\_RXACT\_COMMIT\_NECESSARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-565">678 (0x2A6)</span><span class="sxs-lookup"><span data-stu-id="0bac2-565">678 (0x2A6)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-566">Cet état de niveau d’avertissement indique que l’état de transaction existe déjà pour la sous-arborescence du Registre, mais qu’une validation de transaction a été abandonnée précédemment.</span><span class="sxs-lookup"><span data-stu-id="0bac2-566">This warning level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="0bac2-567">La validation n’a pas été effectuée, mais elle n’a pas été annulée (par conséquent, elle peut toujours être validée si vous le souhaitez).</span><span class="sxs-lookup"><span data-stu-id="0bac2-567">The commit has NOT been completed, but has not been rolled back either (so it may still be committed if desired).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_vérification du support d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**ERROR\_MEDIA\_CHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-569">679 (0x2A7)</span><span class="sxs-lookup"><span data-stu-id="0bac2-569">679 (0x2A7)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-570">{Media Changed} Le support a peut-être changé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-570">{Media Changed} The media may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**substitution du GUID d’erreur \_ \_ \_ effectuée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**ERROR\_GUID\_SUBSTITUTION\_MADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-572">680 (0x2A8)</span><span class="sxs-lookup"><span data-stu-id="0bac2-572">680 (0x2A8)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-573">{Substitution de GUID} Lors de la traduction d’un identificateur global (GUID) vers un ID de sécurité Windows (SID), aucun préfixe GUID défini administrativement n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-573">{GUID Substitution} During the translation of a global identifier (GUID) to a Windows security ID (SID), no administratively-defined GUID prefix was found.</span></span> <span data-ttu-id="0bac2-574">Un préfixe de remplacement a été utilisé, ce qui ne compromettra pas la sécurité du système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-574">A substitute prefix was used, which will not compromise system security.</span></span> <span data-ttu-id="0bac2-575">Toutefois, cela peut fournir un accès plus restrictif que prévu.</span><span class="sxs-lookup"><span data-stu-id="0bac2-575">However, this may provide a more restrictive access than intended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERREUR \_ arrêtée \_ sur le \_ lien symbolique**</span><span class="sxs-lookup"><span data-stu-id="0bac2-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR\_STOPPED\_ON\_SYMLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-577">681 (0x2A9)</span><span class="sxs-lookup"><span data-stu-id="0bac2-577">681 (0x2A9)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-578">L’opération de création s’est arrêtée après avoir atteint un lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="0bac2-578">The create operation stopped after reaching a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERREUR \_ LONGJUMP**</span><span class="sxs-lookup"><span data-stu-id="0bac2-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR\_LONGJUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-580">682 (0x2AA)</span><span class="sxs-lookup"><span data-stu-id="0bac2-580">682 (0x2AA)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-581">Un saut long a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="0bac2-581">A long jump has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERREUR \_ de \_ requête PLUGPLAY \_ refusée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR\_PLUGPLAY\_QUERY\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-583">683 (0x2AB)</span><span class="sxs-lookup"><span data-stu-id="0bac2-583">683 (0x2AB)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-584">L’opération de requête de Plug-and-Play a échoué.</span><span class="sxs-lookup"><span data-stu-id="0bac2-584">The Plug and Play query operation was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERREUR lors du déroulement de la \_ \_ consolidation**</span><span class="sxs-lookup"><span data-stu-id="0bac2-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERROR\_UNWIND\_CONSOLIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-586">684 (0x2AC)</span><span class="sxs-lookup"><span data-stu-id="0bac2-586">684 (0x2AC)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-587">Une consolidation de frame a été exécutée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-587">A frame consolidation has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERREUR de récupération de la \_ ruche du Registre \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERROR\_REGISTRY\_HIVE\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-589">685 (0x2AD)</span><span class="sxs-lookup"><span data-stu-id="0bac2-589">685 (0x2AD)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-590">{Ruche du Registre Récupérée} La ruche du Registre (fichier) :% HS a été endommagée et a été récupérée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-590">{Registry Hive Recovered} Registry hive (file): %hs was corrupted and it has been recovered.</span></span> <span data-ttu-id="0bac2-591">Certaines données ont peut-être été perdues.</span><span class="sxs-lookup"><span data-stu-id="0bac2-591">Some data might have been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**la \_ dll d’erreur \_ est peut- \_ être \_ non sécurisée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**ERROR\_DLL\_MIGHT\_BE\_INSECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-593">686 (0x2AE)</span><span class="sxs-lookup"><span data-stu-id="0bac2-593">686 (0x2AE)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-594">L’application tente d’exécuter du code exécutable à partir du module% HS.</span><span class="sxs-lookup"><span data-stu-id="0bac2-594">The application is attempting to run executable code from the module %hs.</span></span> <span data-ttu-id="0bac2-595">Cela peut être non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-595">This may be insecure.</span></span> <span data-ttu-id="0bac2-596">Une alternative,% HS, est disponible.</span><span class="sxs-lookup"><span data-stu-id="0bac2-596">An alternative, %hs, is available.</span></span> <span data-ttu-id="0bac2-597">L’application doit-elle utiliser le module sécurisé% HS ?</span><span class="sxs-lookup"><span data-stu-id="0bac2-597">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**la \_ dll d’erreur \_ est peut- \_ être \_ incompatible**</span><span class="sxs-lookup"><span data-stu-id="0bac2-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**ERROR\_DLL\_MIGHT\_BE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-599">687 (0x2AF)</span><span class="sxs-lookup"><span data-stu-id="0bac2-599">687 (0x2AF)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-600">L’application charge le code exécutable à partir du module% HS.</span><span class="sxs-lookup"><span data-stu-id="0bac2-600">The application is loading executable code from the module %hs.</span></span> <span data-ttu-id="0bac2-601">Cela est sécurisé, mais peut être incompatible avec les versions précédentes du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0bac2-601">This is secure, but may be incompatible with previous releases of the operating system.</span></span> <span data-ttu-id="0bac2-602">Une alternative,% HS, est disponible.</span><span class="sxs-lookup"><span data-stu-id="0bac2-602">An alternative, %hs, is available.</span></span> <span data-ttu-id="0bac2-603">L’application doit-elle utiliser le module sécurisé% HS ?</span><span class="sxs-lookup"><span data-stu-id="0bac2-603">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERREUR de l' \_ \_ exception dbg \_ non \_ gérée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR\_DBG\_EXCEPTION\_NOT\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-605">688 (0x2B0)</span><span class="sxs-lookup"><span data-stu-id="0bac2-605">688 (0x2B0)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-606">Le débogueur n’a pas géré l’exception.</span><span class="sxs-lookup"><span data-stu-id="0bac2-606">Debugger did not handle the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERREUR \_ dbg \_ répondre \_ plus tard**</span><span class="sxs-lookup"><span data-stu-id="0bac2-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR\_DBG\_REPLY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-608">689 (0x2B1)</span><span class="sxs-lookup"><span data-stu-id="0bac2-608">689 (0x2B1)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-609">Le débogueur répondra plus tard.</span><span class="sxs-lookup"><span data-stu-id="0bac2-609">Debugger will reply later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERREUR \_ dbg \_ Impossible \_ de \_ fournir le \_ descripteur**</span><span class="sxs-lookup"><span data-stu-id="0bac2-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR\_DBG\_UNABLE\_TO\_PROVIDE\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-611">690 (0x2B2)</span><span class="sxs-lookup"><span data-stu-id="0bac2-611">690 (0x2B2)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-612">Le débogueur ne peut pas fournir de handle.</span><span class="sxs-lookup"><span data-stu-id="0bac2-612">Debugger cannot provide handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERREUR \_ dbg de \_ fin de \_ thread**</span><span class="sxs-lookup"><span data-stu-id="0bac2-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR\_DBG\_TERMINATE\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-614">691 (0x2B3)</span><span class="sxs-lookup"><span data-stu-id="0bac2-614">691 (0x2B3)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-615">Thread du débogueur terminé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-615">Debugger terminated thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERREUR \_ du \_ processus de fin de dbg \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR\_DBG\_TERMINATE\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-617">692 (0x2B4)</span><span class="sxs-lookup"><span data-stu-id="0bac2-617">692 (0x2B4)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-618">Le débogueur a terminé le processus.</span><span class="sxs-lookup"><span data-stu-id="0bac2-618">Debugger terminated process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERREUR \_ dbg dans \_ le contrôle \_ C**</span><span class="sxs-lookup"><span data-stu-id="0bac2-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR\_DBG\_CONTROL\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-620">693 (0x2B5)</span><span class="sxs-lookup"><span data-stu-id="0bac2-620">693 (0x2B5)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-621">Le débogueur a obtenu le contrôle C.</span><span class="sxs-lookup"><span data-stu-id="0bac2-621">Debugger got control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERREUR \_ dbg \_ PRINTEXCEPTION \_ C**</span><span class="sxs-lookup"><span data-stu-id="0bac2-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR\_DBG\_PRINTEXCEPTION\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-623">694 (0x2B6)</span><span class="sxs-lookup"><span data-stu-id="0bac2-623">694 (0x2B6)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-624">Exception imprimée du débogueur sur le contrôle C.</span><span class="sxs-lookup"><span data-stu-id="0bac2-624">Debugger printed exception on control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERREUR \_ dbg \_ RIPEXCEPTION**</span><span class="sxs-lookup"><span data-stu-id="0bac2-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR\_DBG\_RIPEXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-626">695 (0x2B7)</span><span class="sxs-lookup"><span data-stu-id="0bac2-626">695 (0x2B7)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-627">Le débogueur a reçu une exception RIP.</span><span class="sxs-lookup"><span data-stu-id="0bac2-627">Debugger received RIP exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERREUR \_ de \_ saut de contrôle dbg \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR\_DBG\_CONTROL\_BREAK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-629">696 (0x2B8)</span><span class="sxs-lookup"><span data-stu-id="0bac2-629">696 (0x2B8)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-630">Le débogueur a reçu un arrêt de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0bac2-630">Debugger received control break.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERREUR \_ de \_ commande \_ dbg**</span><span class="sxs-lookup"><span data-stu-id="0bac2-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR\_DBG\_COMMAND\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-632">697 (0x2B9)</span><span class="sxs-lookup"><span data-stu-id="0bac2-632">697 (0x2B9)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-633">Exception de communication de commande du débogueur.</span><span class="sxs-lookup"><span data-stu-id="0bac2-633">Debugger command communication exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**le nom de l’objet d’erreur \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="0bac2-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**ERROR\_OBJECT\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-635">698 (0x2BA)</span><span class="sxs-lookup"><span data-stu-id="0bac2-635">698 (0x2BA)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-636">{Object Exists} Une tentative de création d’un objet a été effectuée et le nom de l’objet existait déjà.</span><span class="sxs-lookup"><span data-stu-id="0bac2-636">{Object Exists} An attempt was made to create an object and the object name already existed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**le \_ thread d’erreur \_ a été \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="0bac2-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**ERROR\_THREAD\_WAS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-638">699 (0x2BB)</span><span class="sxs-lookup"><span data-stu-id="0bac2-638">699 (0x2BB)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-639">{Thread suspendu} Une interruption de thread s’est produite pendant l’interruption du thread.</span><span class="sxs-lookup"><span data-stu-id="0bac2-639">{Thread Suspended} A thread termination occurred while the thread was suspended.</span></span> <span data-ttu-id="0bac2-640">Le thread a été repris et l’arrêt s’est poursuivi.</span><span class="sxs-lookup"><span data-stu-id="0bac2-640">The thread was resumed, and termination proceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**IMAGE d’erreur \_ \_ non \_ au niveau de la \_ base**</span><span class="sxs-lookup"><span data-stu-id="0bac2-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**ERROR\_IMAGE\_NOT\_AT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-642">700 (0x2BC)</span><span class="sxs-lookup"><span data-stu-id="0bac2-642">700 (0x2BC)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-643">{Image relocalisée} Un fichier image n’a pas pu être mappé à l’adresse spécifiée dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="0bac2-643">{Image Relocated} An image file could not be mapped at the address specified in the image file.</span></span> <span data-ttu-id="0bac2-644">Les corrections locales doivent être effectuées sur cette image.</span><span class="sxs-lookup"><span data-stu-id="0bac2-644">Local fixups must be performed on this image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERREUR \_ d' \_ État RXACT \_ créé**</span><span class="sxs-lookup"><span data-stu-id="0bac2-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR\_RXACT\_STATE\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-646">701 (0x2BD)</span><span class="sxs-lookup"><span data-stu-id="0bac2-646">701 (0x2BD)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-647">Cet état de niveau d’information indique qu’un état de transaction de sous-arborescence de Registre spécifié n’existait pas encore et devait être créé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-647">This informational level status indicates that a specified registry sub-tree transaction state did not yet exist and had to be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_notification de segment d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**ERROR\_SEGMENT\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-649">702 (0x2BE)</span><span class="sxs-lookup"><span data-stu-id="0bac2-649">702 (0x2BE)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-650">{Chargement de segment} Une machine virtuelle DOS (VDM) charge, décharge ou déplace une image de segment de programme MS-DOS ou Win16.</span><span class="sxs-lookup"><span data-stu-id="0bac2-650">{Segment Load} A virtual DOS machine (VDM) is loading, unloading, or moving an MS-DOS or Win16 program segment image.</span></span> <span data-ttu-id="0bac2-651">Une exception est déclenchée pour qu’un débogueur puisse charger, décharger ou suivre des symboles et des points d’arrêt dans ces segments 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0bac2-651">An exception is raised so a debugger can load, unload or track symbols and breakpoints within these 16-bit segments.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERREUR \_ de \_ répertoire actif incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR\_BAD\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-653">703 (0x2BF)</span><span class="sxs-lookup"><span data-stu-id="0bac2-653">703 (0x2BF)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-654">{Répertoire actif non valide} Le processus ne peut pas basculer vers le répertoire de démarrage% HS.</span><span class="sxs-lookup"><span data-stu-id="0bac2-654">{Invalid Current Directory} The process cannot switch to the startup current directory %hs.</span></span> <span data-ttu-id="0bac2-655">Sélectionnez OK pour définir le répertoire actif à% HS, ou cliquez sur Annuler pour quitter.</span><span class="sxs-lookup"><span data-stu-id="0bac2-655">Select OK to set current directory to %hs, or select CANCEL to exit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERREUR \_ ft \_ \_ de lecture de la récupération \_ à partir d’une \_ sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="0bac2-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR\_FT\_READ\_RECOVERY\_FROM\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-657">704 (0x2C0)</span><span class="sxs-lookup"><span data-stu-id="0bac2-657">704 (0x2C0)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-658">{Lecture redondante} Pour répondre à une demande de lecture, le système de fichiers à tolérance de panne NT lit correctement les données demandées à partir d’une copie redondante.</span><span class="sxs-lookup"><span data-stu-id="0bac2-658">{Redundant Read} To satisfy a read request, the NT fault-tolerant file system successfully read the requested data from a redundant copy.</span></span> <span data-ttu-id="0bac2-659">Cela est dû au fait que le système de fichiers a rencontré une défaillance sur un membre du volume à tolérance de panne, mais qu’il n’a pas pu réaffecter la zone défaillante de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0bac2-659">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was unable to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERREUR \_ de \_ récupération en écriture ft \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR\_FT\_WRITE\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-661">705 (0x2C1)</span><span class="sxs-lookup"><span data-stu-id="0bac2-661">705 (0x2C1)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-662">{Écriture redondante} Pour répondre à une demande d’écriture, le système de fichiers à tolérance de panne NT a écrit avec succès une copie redondante des informations.</span><span class="sxs-lookup"><span data-stu-id="0bac2-662">{Redundant Write} To satisfy a write request, the NT fault-tolerant file system successfully wrote a redundant copy of the information.</span></span> <span data-ttu-id="0bac2-663">Cela est dû au fait que le système de fichiers a rencontré une défaillance sur un membre du volume à tolérance de panne, mais qu’il n’a pas été en mesure de réassigner la zone défaillante de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0bac2-663">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was not able to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de type d’ordinateur d’image \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-665">706 (0x2C2)</span><span class="sxs-lookup"><span data-stu-id="0bac2-665">706 (0x2C2)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-666">{Incompatibilité de type d’ordinateur} Le fichier image% HS est valide, mais il est destiné à un type d’ordinateur autre que l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="0bac2-666">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span> <span data-ttu-id="0bac2-667">Sélectionnez OK pour continuer ou annuler pour faire échouer le chargement de la DLL.</span><span class="sxs-lookup"><span data-stu-id="0bac2-667">Select OK to continue, or CANCEL to fail the DLL load.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERREUR de \_ réception \_ partielle**</span><span class="sxs-lookup"><span data-stu-id="0bac2-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR\_RECEIVE\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-669">707 (0x2C3)</span><span class="sxs-lookup"><span data-stu-id="0bac2-669">707 (0x2C3)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-670">{Données partielles reçues} Le transport réseau a renvoyé des données partielles à son client.</span><span class="sxs-lookup"><span data-stu-id="0bac2-670">{Partial Data Received} The network transport returned partial data to its client.</span></span> <span data-ttu-id="0bac2-671">Les données restantes seront envoyées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-671">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**réception d’erreur \_ envoyée \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR\_RECEIVE\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-673">708 (0x2C4)</span><span class="sxs-lookup"><span data-stu-id="0bac2-673">708 (0x2C4)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-674">{Données expédiées reçues} Le transport réseau a renvoyé à son client des données qui ont été marquées comme expédiées par le système distant.</span><span class="sxs-lookup"><span data-stu-id="0bac2-674">{Expedited Data Received} The network transport returned data to its client that was marked as expedited by the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERREUR de \_ réception \_ partielle \_ expédiée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR\_RECEIVE\_PARTIAL\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-676">709 (0x2C5)</span><span class="sxs-lookup"><span data-stu-id="0bac2-676">709 (0x2C5)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-677">{Données expédiées partielles reçues} Le transport réseau a renvoyé des données partielles à son client et ces données ont été marquées comme expédiées par le système distant.</span><span class="sxs-lookup"><span data-stu-id="0bac2-677">{Partial Expedited Data Received} The network transport returned partial data to its client and this data was marked as expedited by the remote system.</span></span> <span data-ttu-id="0bac2-678">Les données restantes seront envoyées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0bac2-678">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**événement d’erreur \_ \_ effectué**</span><span class="sxs-lookup"><span data-stu-id="0bac2-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**ERROR\_EVENT\_DONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-680">710 (0x2C6)</span><span class="sxs-lookup"><span data-stu-id="0bac2-680">710 (0x2C6)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-681">{Événement TDI effectué} L’indication TDI s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0bac2-681">{TDI Event Done} The TDI indication has completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**événement d’erreur \_ \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="0bac2-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**ERROR\_EVENT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-683">711 (0x2C7)</span><span class="sxs-lookup"><span data-stu-id="0bac2-683">711 (0x2C7)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-684">{Événement TDI en attente} L’indication TDI est passée à l’État en attente.</span><span class="sxs-lookup"><span data-stu-id="0bac2-684">{TDI Event Pending} The TDI indication has entered the pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERREUR lors de la \_ vérification du \_ système de fichiers \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR\_CHECKING\_FILE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-686">712 (0x2C8)</span><span class="sxs-lookup"><span data-stu-id="0bac2-686">712 (0x2C8)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-687">Vérification du système de fichiers sur% wZ.</span><span class="sxs-lookup"><span data-stu-id="0bac2-687">Checking file system on %wZ.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERREUR de sortie de l' \_ \_ application irrécupérable \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR\_FATAL\_APP\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-689">713 (0x2C9)</span><span class="sxs-lookup"><span data-stu-id="0bac2-689">713 (0x2C9)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-690">{Sortie d’application irrécupérable}% hs.</span><span class="sxs-lookup"><span data-stu-id="0bac2-690">{Fatal Application Exit} %hs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**\_handle prédéfini d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**ERROR\_PREDEFINED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-692">714 (0x2CA)</span><span class="sxs-lookup"><span data-stu-id="0bac2-692">714 (0x2CA)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-693">La clé de Registre spécifiée est référencée par un handle prédéfini.</span><span class="sxs-lookup"><span data-stu-id="0bac2-693">The specified registry key is referenced by a predefined handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**l’erreur \_ a été \_ déverrouillée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR\_WAS\_UNLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-695">715 (0x2CB)</span><span class="sxs-lookup"><span data-stu-id="0bac2-695">715 (0x2CB)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-696">{Page déverrouillé} La protection de page d’une page verrouillée a été remplacée par « aucun accès » et la page a été déverrouillée de la mémoire et du processus.</span><span class="sxs-lookup"><span data-stu-id="0bac2-696">{Page Unlocked} The page protection of a locked page was changed to 'No Access' and the page was unlocked from memory and from the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_notification de service d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**ERROR\_SERVICE\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-698">716 (0x2CC)</span><span class="sxs-lookup"><span data-stu-id="0bac2-698">716 (0x2CC)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-699">% HS</span><span class="sxs-lookup"><span data-stu-id="0bac2-699">%hs</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**l’erreur \_ a été \_ verrouillée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR\_WAS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-701">717 (0x2CD)</span><span class="sxs-lookup"><span data-stu-id="0bac2-701">717 (0x2CD)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-702">{Page verrouillée} L’une des pages à verrouiller a déjà été verrouillée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-702">{Page Locked} One of the pages to lock was already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**erreur \_ matérielle du journal des erreurs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**ERROR\_LOG\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-704">718 (0x2CE)</span><span class="sxs-lookup"><span data-stu-id="0bac2-704">718 (0x2CE)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-705">Fenêtre contextuelle de l’application : %1 : %2</span><span class="sxs-lookup"><span data-stu-id="0bac2-705">Application popup: %1 : %2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERREUR \_ déjà \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="0bac2-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR\_ALREADY\_WIN32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-707">719 (0x2CF)</span><span class="sxs-lookup"><span data-stu-id="0bac2-707">719 (0x2CF)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-708">ERREUR \_ déjà \_ Win32</span><span class="sxs-lookup"><span data-stu-id="0bac2-708">ERROR\_ALREADY\_WIN32</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERREUR \_ d' \_ incompatibilité de type d’ordinateur d’image \_ \_ \_ exe**</span><span class="sxs-lookup"><span data-stu-id="0bac2-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-710">720 (0x2D0)</span><span class="sxs-lookup"><span data-stu-id="0bac2-710">720 (0x2D0)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-711">{Incompatibilité de type d’ordinateur} Le fichier image% HS est valide, mais il est destiné à un type d’ordinateur autre que l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="0bac2-711">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERREUR \_ aucun \_ rendement \_ effectué**</span><span class="sxs-lookup"><span data-stu-id="0bac2-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR\_NO\_YIELD\_PERFORMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-713">721 (0x2D1)</span><span class="sxs-lookup"><span data-stu-id="0bac2-713">721 (0x2D1)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-714">Une exécution de rendement a été effectuée et aucun thread n’était disponible pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0bac2-714">A yield execution was performed and no thread was available to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**\_reprise du minuteur d’erreur \_ \_ ignorée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**ERROR\_TIMER\_RESUME\_IGNORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-716">722 (0x2D2)</span><span class="sxs-lookup"><span data-stu-id="0bac2-716">722 (0x2D2)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-717">L’indicateur pouvant être repris sur une API de minuteur a été ignoré.</span><span class="sxs-lookup"><span data-stu-id="0bac2-717">The resumable flag to a timer API was ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**arbitrage d’erreur \_ \_ non géré**</span><span class="sxs-lookup"><span data-stu-id="0bac2-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERROR\_ARBITRATION\_UNHANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-719">723 (0x2D3)</span><span class="sxs-lookup"><span data-stu-id="0bac2-719">723 (0x2D3)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-720">L’arbitre a différé l’arbitrage de ces ressources à son parent.</span><span class="sxs-lookup"><span data-stu-id="0bac2-720">The arbiter has deferred arbitration of these resources to its parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERREUR \_ CardBus \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="0bac2-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR\_CARDBUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-722">724 (0x2D4)</span><span class="sxs-lookup"><span data-stu-id="0bac2-722">724 (0x2D4)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-723">Impossible de démarrer l’appareil CardBus inséré en raison d’une erreur de configuration sur « % HS ».</span><span class="sxs-lookup"><span data-stu-id="0bac2-723">The inserted CardBus device cannot be started because of a configuration error on "%hs".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERREUR \_ d' \_ incompatibilité de processeur MP \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR\_MP\_PROCESSOR\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-725">725 (0x2D5)</span><span class="sxs-lookup"><span data-stu-id="0bac2-725">725 (0x2D5)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-726">Les processeurs de ce système multiprocesseur ne sont pas tous du même niveau de révision.</span><span class="sxs-lookup"><span data-stu-id="0bac2-726">The CPUs in this multiprocessor system are not all the same revision level.</span></span> <span data-ttu-id="0bac2-727">Pour utiliser tous les processeurs, le système d’exploitation se limite aux fonctionnalités du processeur le moins performant du système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-727">To use all processors the operating system restricts itself to the features of the least capable processor in the system.</span></span> <span data-ttu-id="0bac2-728">Si des problèmes se produisent avec ce système, contactez le fabricant du processeur pour déterminer si cette combinaison de processeurs est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0bac2-728">Should problems occur with this system, contact the CPU manufacturer to see if this mix of processors is supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERREUR de \_ mise en veille prolongée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR\_HIBERNATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-730">726 (0x2D6)</span><span class="sxs-lookup"><span data-stu-id="0bac2-730">726 (0x2D6)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-731">Le système a été mis en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-731">The system was put into hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERREUR de reprise de la \_ \_ mise en veille prolongée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR\_RESUME\_HIBERNATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-733">727 (0x2D7)</span><span class="sxs-lookup"><span data-stu-id="0bac2-733">727 (0x2D7)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-734">Le système a repris de la mise en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-734">The system was resumed from hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**microprogramme d’erreur \_ \_ mis à jour**</span><span class="sxs-lookup"><span data-stu-id="0bac2-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**ERROR\_FIRMWARE\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-736">728 (0x2D8)</span><span class="sxs-lookup"><span data-stu-id="0bac2-736">728 (0x2D8)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-737">Windows a détecté que le microprogramme système (BIOS) a été mis à jour la \[ date du microprogramme précédent = %2, date du microprogramme actuel %3 \] .</span><span class="sxs-lookup"><span data-stu-id="0bac2-737">Windows has detected that the system firmware (BIOS) was updated \[previous firmware date = %2, current firmware date %3\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**pilotes d’erreur avec \_ \_ fuite de \_ pages verrouillées \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**ERROR\_DRIVERS\_LEAKING\_LOCKED\_PAGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-739">729 (0x2D9)</span><span class="sxs-lookup"><span data-stu-id="0bac2-739">729 (0x2D9)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-740">Un pilote de périphérique perd des pages d’e/s verrouillées, provoquant une dégradation du système.</span><span class="sxs-lookup"><span data-stu-id="0bac2-740">A device driver is leaking locked I/O pages causing system degradation.</span></span> <span data-ttu-id="0bac2-741">Le système a automatiquement activé le code de suivi afin d’essayer d’intercepter le coupable.</span><span class="sxs-lookup"><span data-stu-id="0bac2-741">The system has automatically enabled tracking code in order to try and catch the culprit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERREUR de \_ réveil du \_ système**</span><span class="sxs-lookup"><span data-stu-id="0bac2-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERROR\_WAKE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-743">730 (0x2DA)</span><span class="sxs-lookup"><span data-stu-id="0bac2-743">730 (0x2DA)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-744">Le système a activé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-744">The system has awoken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERREUR d' \_ attente \_ 1**</span><span class="sxs-lookup"><span data-stu-id="0bac2-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR\_WAIT\_1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-746">731 (0x2DB)</span><span class="sxs-lookup"><span data-stu-id="0bac2-746">731 (0x2DB)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-747">ERREUR d' \_ attente \_ 1</span><span class="sxs-lookup"><span data-stu-id="0bac2-747">ERROR\_WAIT\_1</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERREUR d' \_ attente \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0bac2-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERROR\_WAIT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-749">732 (0x2DC)</span><span class="sxs-lookup"><span data-stu-id="0bac2-749">732 (0x2DC)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-750">ERREUR d' \_ attente \_ 2</span><span class="sxs-lookup"><span data-stu-id="0bac2-750">ERROR\_WAIT\_2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERREUR d' \_ attente \_ 3**</span><span class="sxs-lookup"><span data-stu-id="0bac2-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR\_WAIT\_3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-752">733 (0x2DD)</span><span class="sxs-lookup"><span data-stu-id="0bac2-752">733 (0x2DD)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-753">ERREUR d' \_ attente \_ 3</span><span class="sxs-lookup"><span data-stu-id="0bac2-753">ERROR\_WAIT\_3</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERREUR d' \_ attente \_ 63**</span><span class="sxs-lookup"><span data-stu-id="0bac2-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-755">734 (0x2DE)</span><span class="sxs-lookup"><span data-stu-id="0bac2-755">734 (0x2DE)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-756">ERREUR d' \_ attente \_ 63</span><span class="sxs-lookup"><span data-stu-id="0bac2-756">ERROR\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERREUR \_ d' \_ attente abandonnée \_ 0**</span><span class="sxs-lookup"><span data-stu-id="0bac2-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR\_ABANDONED\_WAIT\_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-758">735 (0x2DF)</span><span class="sxs-lookup"><span data-stu-id="0bac2-758">735 (0x2DF)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-759">ERREUR \_ d' \_ attente abandonnée \_ 0</span><span class="sxs-lookup"><span data-stu-id="0bac2-759">ERROR\_ABANDONED\_WAIT\_0</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERREUR \_ d' \_ attente abandonnée \_ 63**</span><span class="sxs-lookup"><span data-stu-id="0bac2-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR\_ABANDONED\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-761">736 (0x2E0)</span><span class="sxs-lookup"><span data-stu-id="0bac2-761">736 (0x2E0)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-762">ERREUR \_ d' \_ attente abandonnée \_ 63</span><span class="sxs-lookup"><span data-stu-id="0bac2-762">ERROR\_ABANDONED\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERREUR de l' \_ utilisateur \_ APC**</span><span class="sxs-lookup"><span data-stu-id="0bac2-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR\_USER\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-764">737 (0x2E1)</span><span class="sxs-lookup"><span data-stu-id="0bac2-764">737 (0x2E1)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-765">ERREUR de l' \_ utilisateur \_ APC</span><span class="sxs-lookup"><span data-stu-id="0bac2-765">ERROR\_USER\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERREUR de \_ noyau \_ APC**</span><span class="sxs-lookup"><span data-stu-id="0bac2-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR\_KERNEL\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-767">738 (0x2E2)</span><span class="sxs-lookup"><span data-stu-id="0bac2-767">738 (0x2E2)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-768">ERREUR de \_ noyau \_ APC</span><span class="sxs-lookup"><span data-stu-id="0bac2-768">ERROR\_KERNEL\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERREUR \_ signalée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR\_ALERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-770">739 (0x2E3)</span><span class="sxs-lookup"><span data-stu-id="0bac2-770">739 (0x2E3)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-771">ERREUR \_ signalée</span><span class="sxs-lookup"><span data-stu-id="0bac2-771">ERROR\_ALERTED</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**élévation d’erreur \_ \_ requise**</span><span class="sxs-lookup"><span data-stu-id="0bac2-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**ERROR\_ELEVATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-773">740 (0x2E4)</span><span class="sxs-lookup"><span data-stu-id="0bac2-773">740 (0x2E4)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-774">L’opération demandée requiert une élévation.</span><span class="sxs-lookup"><span data-stu-id="0bac2-774">The requested operation requires elevation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERREUR d' \_ analyse**</span><span class="sxs-lookup"><span data-stu-id="0bac2-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR\_REPARSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-776">741 (0x2E5)</span><span class="sxs-lookup"><span data-stu-id="0bac2-776">741 (0x2E5)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-777">Une analyse doit être effectuée par le gestionnaire d’objets, car le nom du fichier a entraîné un lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="0bac2-777">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERREUR \_ \_ de rupture \_ de verrou OPLOCK en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="0bac2-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERROR\_OPLOCK\_BREAK\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-779">742 (0x2E6)</span><span class="sxs-lookup"><span data-stu-id="0bac2-779">742 (0x2E6)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-780">Une opération d’ouverture/de création est terminée alors qu’une interruption oplock est en cours.</span><span class="sxs-lookup"><span data-stu-id="0bac2-780">An open/create operation completed while an oplock break is underway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**VOLUME d’erreurs \_ \_ monté**</span><span class="sxs-lookup"><span data-stu-id="0bac2-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**ERROR\_VOLUME\_MOUNTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-782">743 (0x2E7)</span><span class="sxs-lookup"><span data-stu-id="0bac2-782">743 (0x2E7)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-783">Un nouveau volume a été monté par un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0bac2-783">A new volume has been mounted by a file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERREUR \_ RXACT \_ validée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR\_RXACT\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-785">744 (0x2E8)</span><span class="sxs-lookup"><span data-stu-id="0bac2-785">744 (0x2E8)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-786">Cet état du niveau de réussite indique que l’état de la transaction existe déjà pour la sous-arborescence du Registre, mais qu’une validation de transaction a été abandonnée précédemment.</span><span class="sxs-lookup"><span data-stu-id="0bac2-786">This success level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="0bac2-787">La validation est maintenant terminée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-787">The commit has now been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERREUR de \_ notification de \_ nettoyage**</span><span class="sxs-lookup"><span data-stu-id="0bac2-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR\_NOTIFY\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-789">745 (0x2E9)</span><span class="sxs-lookup"><span data-stu-id="0bac2-789">745 (0x2E9)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-790">Cela indique qu’une demande de notification de modification a été effectuée en raison de la fermeture du handle qui a effectué la demande de notification de modification.</span><span class="sxs-lookup"><span data-stu-id="0bac2-790">This indicates that a notify change request has been completed due to closing the handle which made the notify change request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERREUR \_ échec de la connexion au \_ transport principal \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR\_PRIMARY\_TRANSPORT\_CONNECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-792">746 (0x2EA)</span><span class="sxs-lookup"><span data-stu-id="0bac2-792">746 (0x2EA)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-793">{Échec de la connexion sur le transport principal} Une tentative de connexion au serveur distant% HS sur le transport principal a été effectuée, mais la connexion a échoué.</span><span class="sxs-lookup"><span data-stu-id="0bac2-793">{Connect Failure on Primary Transport} An attempt was made to connect to the remote server %hs on the primary transport, but the connection failed.</span></span> <span data-ttu-id="0bac2-794">L’ordinateur a pu se connecter à un transport secondaire.</span><span class="sxs-lookup"><span data-stu-id="0bac2-794">The computer WAS able to connect on a secondary transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_transition de \_ défaillance de page d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**ERROR\_PAGE\_FAULT\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-796">747 (0x2EB)</span><span class="sxs-lookup"><span data-stu-id="0bac2-796">747 (0x2EB)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-797">L’erreur de page était une erreur de transition.</span><span class="sxs-lookup"><span data-stu-id="0bac2-797">Page fault was a transition fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**Page d’erreur de \_ \_ \_ la demande de défaillance \_ zéro**</span><span class="sxs-lookup"><span data-stu-id="0bac2-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERROR\_PAGE\_FAULT\_DEMAND\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-799">748 (0x2EC)</span><span class="sxs-lookup"><span data-stu-id="0bac2-799">748 (0x2EC)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-800">L’erreur de page était une erreur nulle à la demande.</span><span class="sxs-lookup"><span data-stu-id="0bac2-800">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**\_ \_ \_ copie d’erreur \_ de page d’erreur lors de l' \_ écriture**</span><span class="sxs-lookup"><span data-stu-id="0bac2-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**ERROR\_PAGE\_FAULT\_COPY\_ON\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-802">749 (0x2ED)</span><span class="sxs-lookup"><span data-stu-id="0bac2-802">749 (0x2ED)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-803">L’erreur de page était une erreur nulle à la demande.</span><span class="sxs-lookup"><span data-stu-id="0bac2-803">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**Page d’erreur page de garde des erreurs \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**ERROR\_PAGE\_FAULT\_GUARD\_PAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-805">750 (0x2EE)</span><span class="sxs-lookup"><span data-stu-id="0bac2-805">750 (0x2EE)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-806">L’erreur de page était une erreur nulle à la demande.</span><span class="sxs-lookup"><span data-stu-id="0bac2-806">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_fichier de \_ \_ pagination \_ des erreurs de page d’erreur**</span><span class="sxs-lookup"><span data-stu-id="0bac2-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**ERROR\_PAGE\_FAULT\_PAGING\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-808">751 (0x2EF)</span><span class="sxs-lookup"><span data-stu-id="0bac2-808">751 (0x2EF)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-809">L’erreur de page a été satisfaite par la lecture à partir d’un périphérique de stockage secondaire.</span><span class="sxs-lookup"><span data-stu-id="0bac2-809">Page fault was satisfied by reading from a secondary storage device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**PAGE de cache des erreurs \_ \_ \_ verrouillée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**ERROR\_CACHE\_PAGE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-811">752 (0x2F0)</span><span class="sxs-lookup"><span data-stu-id="0bac2-811">752 (0x2F0)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-812">La page mise en cache a été verrouillée pendant l’opération.</span><span class="sxs-lookup"><span data-stu-id="0bac2-812">Cached page was locked during operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERREUR \_ de \_ vidage sur incident**</span><span class="sxs-lookup"><span data-stu-id="0bac2-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERROR\_CRASH\_DUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-814">753 (0x2F1)</span><span class="sxs-lookup"><span data-stu-id="0bac2-814">753 (0x2F1)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-815">Le vidage sur incident existe dans le fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="0bac2-815">Crash dump exists in paging file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**tampon d’erreur- \_ \_ tous les \_ zéros**</span><span class="sxs-lookup"><span data-stu-id="0bac2-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**ERROR\_BUFFER\_ALL\_ZEROS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-817">754 (0x2F2)</span><span class="sxs-lookup"><span data-stu-id="0bac2-817">754 (0x2F2)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-818">La mémoire tampon spécifiée ne contient que des zéros.</span><span class="sxs-lookup"><span data-stu-id="0bac2-818">Specified buffer contains all zeros.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERREUR d’analyse de l' \_ \_ objet**</span><span class="sxs-lookup"><span data-stu-id="0bac2-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR\_REPARSE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-820">755 (0x2F3)</span><span class="sxs-lookup"><span data-stu-id="0bac2-820">755 (0x2F3)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-821">Une analyse doit être effectuée par le gestionnaire d’objets, car le nom du fichier a entraîné un lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="0bac2-821">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**Erreurs de ressources d’erreur \_ \_ \_ modifiées**</span><span class="sxs-lookup"><span data-stu-id="0bac2-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**ERROR\_RESOURCE\_REQUIREMENTS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-823">756 (0x2F4)</span><span class="sxs-lookup"><span data-stu-id="0bac2-823">756 (0x2F4)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-824">L’appareil a réussi une requête-stop et ses besoins en ressources ont changé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-824">The device has succeeded a query-stop and its resource requirements have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**traduction d’erreur \_ \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**ERROR\_TRANSLATION\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-826">757 (0x2F5)</span><span class="sxs-lookup"><span data-stu-id="0bac2-826">757 (0x2F5)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-827">Le traducteur a traduit ces ressources dans l’espace global et aucune autre traduction ne doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-827">The translator has translated these resources into the global space and no further translations should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**\_aucune erreur \_ à \_ terminer**</span><span class="sxs-lookup"><span data-stu-id="0bac2-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERROR\_NOTHING\_TO\_TERMINATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-829">758 (0x2F6)</span><span class="sxs-lookup"><span data-stu-id="0bac2-829">758 (0x2F6)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-830">Un processus en cours d’arrêt n’a aucun thread à arrêter.</span><span class="sxs-lookup"><span data-stu-id="0bac2-830">A process being terminated has no threads to terminate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**le \_ processus \_ d’erreur n’est pas \_ dans le \_ travail**</span><span class="sxs-lookup"><span data-stu-id="0bac2-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**ERROR\_PROCESS\_NOT\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-832">759 (0x2F7)</span><span class="sxs-lookup"><span data-stu-id="0bac2-832">759 (0x2F7)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-833">Le processus spécifié ne fait pas partie d’un travail.</span><span class="sxs-lookup"><span data-stu-id="0bac2-833">The specified process is not part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**\_traitement \_ des erreurs dans le \_ travail**</span><span class="sxs-lookup"><span data-stu-id="0bac2-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**ERROR\_PROCESS\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-835">760 (0x2F8)</span><span class="sxs-lookup"><span data-stu-id="0bac2-835">760 (0x2F8)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-836">Le processus spécifié fait partie d’un travail.</span><span class="sxs-lookup"><span data-stu-id="0bac2-836">The specified process is part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERREUR \_ VOLSNAP \_ prêt pour la mise en veille prolongée \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR\_VOLSNAP\_HIBERNATE\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-838">761 (0x2F9)</span><span class="sxs-lookup"><span data-stu-id="0bac2-838">761 (0x2F9)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-839">{Service VSS} Le système est maintenant prêt pour la mise en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-839">{Volume Shadow Copy Service} The system is now ready for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERREUR \_ FSFILTER \_ op \_ s’est terminée \_ avec succès**</span><span class="sxs-lookup"><span data-stu-id="0bac2-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR\_FSFILTER\_OP\_COMPLETED\_SUCCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-841">762 (0x2FA)</span><span class="sxs-lookup"><span data-stu-id="0bac2-841">762 (0x2FA)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-842">Un système de fichiers ou un pilote de filtre de système de fichiers a réussi une opération FsFilter.</span><span class="sxs-lookup"><span data-stu-id="0bac2-842">A file system or file system filter driver has successfully completed an FsFilter operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**vecteur d’interruption d’erreur \_ \_ \_ déjà \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="0bac2-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**ERROR\_INTERRUPT\_VECTOR\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-844">763 (0x2FB)</span><span class="sxs-lookup"><span data-stu-id="0bac2-844">763 (0x2FB)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-845">Le vecteur d’interruption spécifié était déjà connecté.</span><span class="sxs-lookup"><span data-stu-id="0bac2-845">The specified interrupt vector was already connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**interruption d’erreur \_ \_ toujours \_ connectée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**ERROR\_INTERRUPT\_STILL\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-847">764 (0x2FC)</span><span class="sxs-lookup"><span data-stu-id="0bac2-847">764 (0x2FC)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-848">Le vecteur d’interruption spécifié est toujours connecté.</span><span class="sxs-lookup"><span data-stu-id="0bac2-848">The specified interrupt vector is still connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**\_attente \_ d’erreur pour \_ OPLOCK**</span><span class="sxs-lookup"><span data-stu-id="0bac2-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR\_WAIT\_FOR\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-850">765 (0x2FD)</span><span class="sxs-lookup"><span data-stu-id="0bac2-850">765 (0x2FD)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-851">Une opération est bloquée en attente d’un oplock.</span><span class="sxs-lookup"><span data-stu-id="0bac2-851">An operation is blocked waiting for an oplock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERREUR de gestion de l' \_ \_ exception dbg \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR\_DBG\_EXCEPTION\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-853">766 (0x2FE)</span><span class="sxs-lookup"><span data-stu-id="0bac2-853">766 (0x2FE)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-854">Exception gérée par le débogueur.</span><span class="sxs-lookup"><span data-stu-id="0bac2-854">Debugger handled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERREUR \_ dbg \_ continue**</span><span class="sxs-lookup"><span data-stu-id="0bac2-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR\_DBG\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-856">767 (0x2FF)</span><span class="sxs-lookup"><span data-stu-id="0bac2-856">767 (0x2FF)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-857">Le débogueur a continué.</span><span class="sxs-lookup"><span data-stu-id="0bac2-857">Debugger continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**\_ \_ pile contextuelle de rappel d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**ERROR\_CALLBACK\_POP\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-859">768 (0x300)</span><span class="sxs-lookup"><span data-stu-id="0bac2-859">768 (0x300)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-860">Une exception s’est produite dans un rappel en mode utilisateur et la trame de rappel du noyau doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-860">An exception occurred in a user mode callback and the kernel callback frame should be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**COMPRESSION des erreurs \_ \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**ERROR\_COMPRESSION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-862">769 (0x301)</span><span class="sxs-lookup"><span data-stu-id="0bac2-862">769 (0x301)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-863">La compression est désactivée pour ce volume.</span><span class="sxs-lookup"><span data-stu-id="0bac2-863">Compression is disabled for this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERREUR \_ CANTFETCHBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="0bac2-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR\_CANTFETCHBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-865">770 (0x302)</span><span class="sxs-lookup"><span data-stu-id="0bac2-865">770 (0x302)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-866">Le fournisseur de données ne peut pas extraire vers l’arrière à travers un jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="0bac2-866">The data provider cannot fetch backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERREUR \_ CANTSCROLLBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="0bac2-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR\_CANTSCROLLBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-868">771 (0x303)</span><span class="sxs-lookup"><span data-stu-id="0bac2-868">771 (0x303)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-869">Le fournisseur de données ne peut pas faire défiler vers l’arrière d’un jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="0bac2-869">The data provider cannot scroll backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERREUR \_ ROWSNOTRELEASED**</span><span class="sxs-lookup"><span data-stu-id="0bac2-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERROR\_ROWSNOTRELEASED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-871">772 (0x304)</span><span class="sxs-lookup"><span data-stu-id="0bac2-871">772 (0x304)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-872">Le fournisseur de données exige que les données précédemment extraites soient libérées avant de demander des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0bac2-872">The data provider requires that previously fetched data is released before asking for more data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**\_indicateurs d' \_ accesseur d’erreur incorrects \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERROR\_BAD\_ACCESSOR\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-874">773 (0x305)</span><span class="sxs-lookup"><span data-stu-id="0bac2-874">773 (0x305)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-875">Le fournisseur de données n’a pas pu interpréter les indicateurs définis pour une liaison de colonne dans un accesseur.</span><span class="sxs-lookup"><span data-stu-id="0bac2-875">The data provider was not able to interpret the flags set for a column binding in an accessor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_Erreurs \_ rencontrées**</span><span class="sxs-lookup"><span data-stu-id="0bac2-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**ERROR\_ERRORS\_ENCOUNTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-877">774 (0x306)</span><span class="sxs-lookup"><span data-stu-id="0bac2-877">774 (0x306)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-878">Une ou plusieurs erreurs se sont produites lors du traitement de la demande.</span><span class="sxs-lookup"><span data-stu-id="0bac2-878">One or more errors occurred while processing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERREUR \_ non \_ possible**</span><span class="sxs-lookup"><span data-stu-id="0bac2-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-880">775 (0x307)</span><span class="sxs-lookup"><span data-stu-id="0bac2-880">775 (0x307)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-881">L’implémentation ne peut pas effectuer la requête.</span><span class="sxs-lookup"><span data-stu-id="0bac2-881">The implementation is not capable of performing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**\_demande \_ d’erreur \_ hors \_ séquence**</span><span class="sxs-lookup"><span data-stu-id="0bac2-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**ERROR\_REQUEST\_OUT\_OF\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-883">776 (0x308)</span><span class="sxs-lookup"><span data-stu-id="0bac2-883">776 (0x308)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-884">Le client d’un composant a demandé une opération qui n’est pas valide compte tenu de l’état de l’instance du composant.</span><span class="sxs-lookup"><span data-stu-id="0bac2-884">The client of a component requested an operation which is not valid given the state of the component instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**erreur d’analyse de la version d’erreur \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**ERROR\_VERSION\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-886">777 (0x309)</span><span class="sxs-lookup"><span data-stu-id="0bac2-886">777 (0x309)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-887">Impossible d’analyser un numéro de version.</span><span class="sxs-lookup"><span data-stu-id="0bac2-887">A version number could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERREUR \_ BADSTARTPOSITION**</span><span class="sxs-lookup"><span data-stu-id="0bac2-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERROR\_BADSTARTPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-889">778 (0x30A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-889">778 (0x30A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-890">La position de début de l’itérateur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0bac2-890">The iterator's start position is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**ERREUR de \_ mémoire \_ matérielle**</span><span class="sxs-lookup"><span data-stu-id="0bac2-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**ERROR\_MEMORY\_HARDWARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-892">779 (0x30B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-892">779 (0x30B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-893">Le matériel a signalé une erreur de mémoire incorrecte.</span><span class="sxs-lookup"><span data-stu-id="0bac2-893">The hardware has reported an uncorrectable memory error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERREUR \_ de \_ réparation de disque \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR\_DISK\_REPAIR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-895">780 (0x30C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-895">780 (0x30C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-896">L’opération tentée a nécessité l’activation de la réparation spontanée.</span><span class="sxs-lookup"><span data-stu-id="0bac2-896">The attempted operation required self healing to be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERREUR \_ de ressource insuffisante \_ \_ pour la \_ \_ taille de section partagée spécifiée \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR\_INSUFFICIENT\_RESOURCE\_FOR\_SPECIFIED\_SHARED\_SECTION\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-898">781 (0x30D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-898">781 (0x30D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-899">Le tas du Bureau a rencontré une erreur lors de l’allocation de la mémoire de la session.</span><span class="sxs-lookup"><span data-stu-id="0bac2-899">The Desktop heap encountered an error while allocating session memory.</span></span> <span data-ttu-id="0bac2-900">Le journal des événements système contient des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0bac2-900">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**erreur \_ de \_ transition de POWERSTATE du système d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-902">782 (0x30E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-902">782 (0x30E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-903">L’état d’alimentation du système passe de %2 à %3.</span><span class="sxs-lookup"><span data-stu-id="0bac2-903">The system power state is transitioning from %2 to %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**erreur \_ de \_ \_ transition complexe \_ POWERSTATE du système d’erreur**</span><span class="sxs-lookup"><span data-stu-id="0bac2-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_COMPLEX\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-905">783 (0x30F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-905">783 (0x30F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-906">L’état d’alimentation du système passe de %2 à %3, mais peut entrer %4.</span><span class="sxs-lookup"><span data-stu-id="0bac2-906">The system power state is transitioning from %2 to %3 but could enter %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERREUR \_ MCA \_ exception**</span><span class="sxs-lookup"><span data-stu-id="0bac2-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR\_MCA\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-908">784 (0x310)</span><span class="sxs-lookup"><span data-stu-id="0bac2-908">784 (0x310)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-909">Un thread est distribué avec une EXCEPTION MCA en raison de MCA.</span><span class="sxs-lookup"><span data-stu-id="0bac2-909">A thread is getting dispatched with MCA EXCEPTION because of MCA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**\_audit d’accès aux erreurs \_ \_ par \_ stratégie**</span><span class="sxs-lookup"><span data-stu-id="0bac2-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR\_ACCESS\_AUDIT\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-911">785 (0x311)</span><span class="sxs-lookup"><span data-stu-id="0bac2-911">785 (0x311)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-912">L’accès à %1 est analysé par la règle de stratégie %2.</span><span class="sxs-lookup"><span data-stu-id="0bac2-912">Access to %1 is monitored by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**\_accès aux erreurs \_ désactivé \_ non \_ protégé \_ par \_ la \_ stratégie**</span><span class="sxs-lookup"><span data-stu-id="0bac2-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_NO\_SAFER\_UI\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-914">786 (0x312)</span><span class="sxs-lookup"><span data-stu-id="0bac2-914">786 (0x312)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-915">L’accès à %1 a été restreint par votre administrateur par la règle de stratégie %2.</span><span class="sxs-lookup"><span data-stu-id="0bac2-915">Access to %1 has been restricted by your Administrator by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERREUR lors de l' \_ abandon de \_ HIBERFILE**</span><span class="sxs-lookup"><span data-stu-id="0bac2-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR\_ABANDON\_HIBERFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-917">787 (0x313)</span><span class="sxs-lookup"><span data-stu-id="0bac2-917">787 (0x313)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-918">Un fichier de mise en veille prolongée valide a été invalidé et doit être abandonné.</span><span class="sxs-lookup"><span data-stu-id="0bac2-918">A valid hibernation file has been invalidated and should be abandoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERREUR de \_ perte du \_ réseau de données WRITEBEHIND \_ \_ \_ déconnecté**</span><span class="sxs-lookup"><span data-stu-id="0bac2-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-920">788 (0x314)</span><span class="sxs-lookup"><span data-stu-id="0bac2-920">788 (0x314)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-921">{Échec de l’écriture différée} Windows n’a pas pu enregistrer toutes les données du fichier% HS ; les données ont été perdues.</span><span class="sxs-lookup"><span data-stu-id="0bac2-921">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="0bac2-922">Cette erreur peut être due à des problèmes de connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="0bac2-922">This error may be caused by network connectivity issues.</span></span> <span data-ttu-id="0bac2-923">Essayez d’enregistrer ce fichier ailleurs.</span><span class="sxs-lookup"><span data-stu-id="0bac2-923">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERREUR lors de la perte du serveur de \_ \_ \_ données WRITEBEHIND \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-925">789 (0x315)</span><span class="sxs-lookup"><span data-stu-id="0bac2-925">789 (0x315)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-926">{Échec de l’écriture différée} Windows n’a pas pu enregistrer toutes les données du fichier% HS ; les données ont été perdues.</span><span class="sxs-lookup"><span data-stu-id="0bac2-926">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="0bac2-927">Cette erreur a été retournée par le serveur sur lequel se trouve le fichier.</span><span class="sxs-lookup"><span data-stu-id="0bac2-927">This error was returned by the server on which the file exists.</span></span> <span data-ttu-id="0bac2-928">Essayez d’enregistrer ce fichier ailleurs.</span><span class="sxs-lookup"><span data-stu-id="0bac2-928">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERREUR lors de la \_ perte du \_ \_ \_ disque local de données WRITEBEHIND \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_LOCAL\_DISK\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-930">790 (0x316)</span><span class="sxs-lookup"><span data-stu-id="0bac2-930">790 (0x316)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-931">{Échec de l’écriture différée} Windows n’a pas pu enregistrer toutes les données du fichier% HS ; les données ont été perdues.</span><span class="sxs-lookup"><span data-stu-id="0bac2-931">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="0bac2-932">Cette erreur peut se produire si l’appareil a été supprimé ou si le média est protégé en écriture.</span><span class="sxs-lookup"><span data-stu-id="0bac2-932">This error may be caused if the device has been removed or the media is write-protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERREUR \_ de \_ table MCFG incorrecte \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR\_BAD\_MCFG\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-934">791 (0x317)</span><span class="sxs-lookup"><span data-stu-id="0bac2-934">791 (0x317)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-935">Les ressources requises pour cet appareil sont en conflit avec la table MCFG.</span><span class="sxs-lookup"><span data-stu-id="0bac2-935">The resources required for this device conflict with the MCFG table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERREUR \_ de \_ réparation de disque \_ redirigée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR\_DISK\_REPAIR\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-937">792 (0x318)</span><span class="sxs-lookup"><span data-stu-id="0bac2-937">792 (0x318)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-938">La réparation du volume n’a pas pu être effectuée tant qu’il est en ligne.</span><span class="sxs-lookup"><span data-stu-id="0bac2-938">The volume repair could not be performed while it is online.</span></span> <span data-ttu-id="0bac2-939">Planifiez la mise hors connexion du volume afin qu’il puisse être réparé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-939">Please schedule to take the volume offline so that it can be repaired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ÉCHEC de la \_ réparation du disque erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR\_DISK\_REPAIR\_UNSUCCESSFUL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-941">793 (0x319)</span><span class="sxs-lookup"><span data-stu-id="0bac2-941">793 (0x319)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-942">La réparation du volume a échoué.</span><span class="sxs-lookup"><span data-stu-id="0bac2-942">The volume repair was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERREUR \_ de \_ saturation du journal \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR\_CORRUPT\_LOG\_OVERFULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-944">794 (0x31A)</span><span class="sxs-lookup"><span data-stu-id="0bac2-944">794 (0x31A)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-945">L’un des journaux d’altération du volume est plein.</span><span class="sxs-lookup"><span data-stu-id="0bac2-945">One of the volume corruption logs is full.</span></span> <span data-ttu-id="0bac2-946">Les dommages qui peuvent être détectés ne seront pas consignés.</span><span class="sxs-lookup"><span data-stu-id="0bac2-946">Further corruptions that may be detected won't be logged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERREUR \_ de \_ journal \_ endommagé endommagé**</span><span class="sxs-lookup"><span data-stu-id="0bac2-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR\_CORRUPT\_LOG\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-948">795 (0x31B)</span><span class="sxs-lookup"><span data-stu-id="0bac2-948">795 (0x31B)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-949">L’un des journaux d’altération du volume est endommagé en interne et doit être recréé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-949">One of the volume corruption logs is internally corrupted and needs to be recreated.</span></span> <span data-ttu-id="0bac2-950">Le volume peut contenir des altérations non détectées et doit être analysé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-950">The volume may contain undetected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERREUR \_ de \_ journal endommagé \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="0bac2-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR\_CORRUPT\_LOG\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-952">796 (0x31C)</span><span class="sxs-lookup"><span data-stu-id="0bac2-952">796 (0x31C)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-953">L’un des journaux d’altération de volume n’est pas disponible pour être utilisé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-953">One of the volume corruption logs is unavailable for being operated on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERREUR \_ \_ fichier journal endommagé \_ supprimé \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR\_CORRUPT\_LOG\_DELETED\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-955">797 (0x31D)</span><span class="sxs-lookup"><span data-stu-id="0bac2-955">797 (0x31D)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-956">L’un des journaux d’altération du volume a été supprimé tout en conservant des enregistrements d’altération.</span><span class="sxs-lookup"><span data-stu-id="0bac2-956">One of the volume corruption logs was deleted while still having corruption records in them.</span></span> <span data-ttu-id="0bac2-957">Le volume contient des altérations détectées et doit être analysé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-957">The volume contains detected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERREUR \_ de \_ journal \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="0bac2-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR\_CORRUPT\_LOG\_CLEARED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-959">798 (0x31E)</span><span class="sxs-lookup"><span data-stu-id="0bac2-959">798 (0x31E)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-960">L’un des journaux d’altération du volume a été effacé par CHKDSK et ne contient plus de dommages réels.</span><span class="sxs-lookup"><span data-stu-id="0bac2-960">One of the volume corruption logs was cleared by chkdsk and no longer contains real corruptions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERREUR \_ \_ nom orphelin \_ épuisé**</span><span class="sxs-lookup"><span data-stu-id="0bac2-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR\_ORPHAN\_NAME\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-962">799 (0x31F)</span><span class="sxs-lookup"><span data-stu-id="0bac2-962">799 (0x31F)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-963">Des fichiers orphelins existent sur le volume mais n’ont pas pu être récupérés car aucun nouveau nom n’a pu être créé dans le répertoire de récupération.</span><span class="sxs-lookup"><span data-stu-id="0bac2-963">Orphaned files exist on the volume but could not be recovered because no more new names could be created in the recovery directory.</span></span> <span data-ttu-id="0bac2-964">Les fichiers doivent être déplacés à partir du répertoire de récupération.</span><span class="sxs-lookup"><span data-stu-id="0bac2-964">Files must be moved from the recovery directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERREUR \_ OPLOCK \_ basculée \_ vers le \_ nouveau \_ handle**</span><span class="sxs-lookup"><span data-stu-id="0bac2-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR\_OPLOCK\_SWITCHED\_TO\_NEW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-966">800 (0x320)</span><span class="sxs-lookup"><span data-stu-id="0bac2-966">800 (0x320)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-967">Le oplock associé à ce descripteur est maintenant associé à un autre handle.</span><span class="sxs-lookup"><span data-stu-id="0bac2-967">The oplock that was associated with this handle is now associated with a different handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**l’erreur \_ ne peut pas \_ accorder le \_ \_ OPLOCK demandé**</span><span class="sxs-lookup"><span data-stu-id="0bac2-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR\_CANNOT\_GRANT\_REQUESTED\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-969">801 (0x321)</span><span class="sxs-lookup"><span data-stu-id="0bac2-969">801 (0x321)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-970">Un oplock du niveau demandé ne peut pas être accordé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-970">An oplock of the requested level cannot be granted.</span></span> <span data-ttu-id="0bac2-971">Un oplock d’un niveau inférieur peut être disponible.</span><span class="sxs-lookup"><span data-stu-id="0bac2-971">An oplock of a lower level may be available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERREUR \_ Impossible d' \_ interrompre \_ OPLOCK**</span><span class="sxs-lookup"><span data-stu-id="0bac2-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR\_CANNOT\_BREAK\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-973">802 (0x322)</span><span class="sxs-lookup"><span data-stu-id="0bac2-973">802 (0x322)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-974">L’opération n’a pas abouti, car cela entraînerait la rupture d’un oplock.</span><span class="sxs-lookup"><span data-stu-id="0bac2-974">The operation did not complete successfully because it would cause an oplock to be broken.</span></span> <span data-ttu-id="0bac2-975">L’appelant a demandé que les verrous oplock existants ne soient pas rompus.</span><span class="sxs-lookup"><span data-stu-id="0bac2-975">The caller has requested that existing oplocks not be broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**descripteur OPLOCK de l’erreur \_ \_ \_ fermé**</span><span class="sxs-lookup"><span data-stu-id="0bac2-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERROR\_OPLOCK\_HANDLE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-977">803 (0x323)</span><span class="sxs-lookup"><span data-stu-id="0bac2-977">803 (0x323)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-978">Le handle avec lequel ce oplock est associé a été fermé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-978">The handle with which this oplock was associated has been closed.</span></span> <span data-ttu-id="0bac2-979">Le verrou oplock est maintenant rompu.</span><span class="sxs-lookup"><span data-stu-id="0bac2-979">The oplock is now broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERREUR \_ aucune \_ \_ condition ACE**</span><span class="sxs-lookup"><span data-stu-id="0bac2-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR\_NO\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-981">804 (0x324)</span><span class="sxs-lookup"><span data-stu-id="0bac2-981">804 (0x324)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-982">L’entrée de contrôle d’accès (ACE) spécifiée ne contient pas de condition.</span><span class="sxs-lookup"><span data-stu-id="0bac2-982">The specified access control entry (ACE) does not contain a condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERREUR \_ de \_ condition ACE non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0bac2-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR\_INVALID\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-984">805 (0x325)</span><span class="sxs-lookup"><span data-stu-id="0bac2-984">805 (0x325)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-985">L’entrée de contrôle d’accès (ACE) spécifiée contient une condition non valide.</span><span class="sxs-lookup"><span data-stu-id="0bac2-985">The specified access control entry (ACE) contains an invalid condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**HANDLE de fichier d’erreur \_ \_ \_ révoqué**</span><span class="sxs-lookup"><span data-stu-id="0bac2-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**ERROR\_FILE\_HANDLE\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-987">806 (0x326)</span><span class="sxs-lookup"><span data-stu-id="0bac2-987">806 (0x326)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-988">L’accès au descripteur de fichier spécifié a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="0bac2-988">Access to the specified file handle has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**IMAGE d’erreur \_ \_ à une \_ \_ base différente**</span><span class="sxs-lookup"><span data-stu-id="0bac2-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**ERROR\_IMAGE\_AT\_DIFFERENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-990">807 (0x327)</span><span class="sxs-lookup"><span data-stu-id="0bac2-990">807 (0x327)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-991">Un fichier image a été mappé à une adresse différente de celle spécifiée dans le fichier image, mais les corrections sont toujours effectuées automatiquement sur l’image.</span><span class="sxs-lookup"><span data-stu-id="0bac2-991">An image file was mapped at a different address from the one specified in the image file but fixups will still be automatically performed on the image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERREUR \_ EA \_ accès \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="0bac2-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR\_EA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-993">994 (0x3E2)</span><span class="sxs-lookup"><span data-stu-id="0bac2-993">994 (0x3E2)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-994">L’accès à l’attribut étendu a été refusé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-994">Access to the extended attribute was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**ERREUR de l' \_ opération \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="0bac2-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**ERROR\_OPERATION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-996">995 (0x3E3)</span><span class="sxs-lookup"><span data-stu-id="0bac2-996">995 (0x3E3)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-997">L’opération d’e/s a été annulée en raison de la sortie d’un thread ou d’une demande de l’application.</span><span class="sxs-lookup"><span data-stu-id="0bac2-997">The I/O operation has been aborted because of either a thread exit or an application request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERREUR d' \_ e/s \_ incomplète**</span><span class="sxs-lookup"><span data-stu-id="0bac2-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERROR\_IO\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-999">996 (0x3E4)</span><span class="sxs-lookup"><span data-stu-id="0bac2-999">996 (0x3E4)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-1000">L’événement d’e/s avec chevauchement n’est pas dans un état signalé.</span><span class="sxs-lookup"><span data-stu-id="0bac2-1000">Overlapped I/O event is not in a signaled state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERREUR d' \_ e/s \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="0bac2-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERROR\_IO\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-1002">997 (0x3E5)</span><span class="sxs-lookup"><span data-stu-id="0bac2-1002">997 (0x3E5)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-1003">L’opération d’e/s avec chevauchement est en cours.</span><span class="sxs-lookup"><span data-stu-id="0bac2-1003">Overlapped I/O operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERREUR \_ NOaccess**</span><span class="sxs-lookup"><span data-stu-id="0bac2-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR\_NOACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-1005">998 (0x3E6)</span><span class="sxs-lookup"><span data-stu-id="0bac2-1005">998 (0x3E6)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-1006">Accès non valide à l’emplacement de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0bac2-1006">Invalid access to memory location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0bac2-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERREUR \_ SWAPERROR**</span><span class="sxs-lookup"><span data-stu-id="0bac2-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR\_SWAPERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac2-1008">999 (0x3E7)</span><span class="sxs-lookup"><span data-stu-id="0bac2-1008">999 (0x3E7)</span></span>
</dt> <dt>



<span data-ttu-id="0bac2-1009">Erreur lors de l’exécution de l’opération InPage.</span><span class="sxs-lookup"><span data-stu-id="0bac2-1009">Error performing inpage operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="0bac2-1010">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bac2-1010">Requirements</span></span>



| <span data-ttu-id="0bac2-1011">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bac2-1011">Requirement</span></span> | <span data-ttu-id="0bac2-1012">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bac2-1012">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0bac2-1013">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bac2-1013">Minimum supported client</span></span><br/> | <span data-ttu-id="0bac2-1014">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bac2-1014">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0bac2-1015">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bac2-1015">Minimum supported server</span></span><br/> | <span data-ttu-id="0bac2-1016">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bac2-1016">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0bac2-1017">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bac2-1017">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bac2-1018"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bac2-1018"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bac2-1019">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bac2-1019">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bac2-1020">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="0bac2-1020">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
