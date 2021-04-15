---
description: Windows 10 a introduit une nouvelle fonctionnalité de sécurité nommée VSM (Virtual Secure mode).
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Processus de mode utilisateur isolé (IUM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a176421174a58abe4ab595bb37ab75434edade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569632"
---
# <a name="isolated-user-mode-ium-processes"></a><span data-ttu-id="69e02-103">Processus de mode utilisateur isolé (IUM)</span><span class="sxs-lookup"><span data-stu-id="69e02-103">Isolated User Mode (IUM) Processes</span></span>

<span data-ttu-id="69e02-104">Windows 10 a introduit une nouvelle fonctionnalité de sécurité nommée VSM (Virtual Secure mode).</span><span class="sxs-lookup"><span data-stu-id="69e02-104">Windows 10 introduced a new security feature named Virtual Secure Mode (VSM).</span></span> <span data-ttu-id="69e02-105">VSM s’appuie sur l’hyperviseur Hyper-V et la traduction d’adresses de second niveau (SLAT) pour créer un ensemble de modes appelés « niveaux de confiance virtuels » (VTL).</span><span class="sxs-lookup"><span data-stu-id="69e02-105">VSM leverages the Hyper-V Hypervisor and Second Level Address Translation (SLAT) to create a set of modes called Virtual Trust Levels (VTLs).</span></span> <span data-ttu-id="69e02-106">Cette nouvelle architecture logicielle crée une limite de sécurité pour empêcher les processus s’exécutant dans une VTL d’accéder à la mémoire d’une autre VTL.</span><span class="sxs-lookup"><span data-stu-id="69e02-106">This new software architecture creates a security boundary to prevent processes running in one VTL from accessing the memory of another VTL.</span></span> <span data-ttu-id="69e02-107">L’avantage de cette isolation comprend une atténuation supplémentaire des attaques de noyau, tout en protégeant les ressources telles que les hachages de mot de passe et les clés Kerberos.</span><span class="sxs-lookup"><span data-stu-id="69e02-107">The benefit of this isolation includes additional mitigation from kernel exploits while protecting assets such as password hashes and Kerberos keys.</span></span>

<span data-ttu-id="69e02-108">Le diagramme 1 illustre le modèle traditionnel de code en mode noyau et en mode utilisateur exécuté dans l’anneau d’UC 0 et l’anneau 3, respectivement.</span><span class="sxs-lookup"><span data-stu-id="69e02-108">Diagram 1 depicts the traditional model of Kernel mode and User mode code running in CPU ring 0 and ring 3, respectively.</span></span> <span data-ttu-id="69e02-109">Dans ce nouveau modèle, le code qui s’exécute dans le modèle traditionnel s’exécute dans VTL0 et il ne peut pas accéder aux VTL1 privilégiés les plus élevés, où le noyau sécurisé et le mode utilisateur isolé (IUM) exécutent du code.</span><span class="sxs-lookup"><span data-stu-id="69e02-109">In this new model, the code running in the traditional model executes in VTL0 and it cannot access the higher privileged VTL1, where the Secure Kernel and Isolated User Mode (IUM) execute code.</span></span> <span data-ttu-id="69e02-110">Les VTL sont hiérarchiquement, ce qui signifie que tout code s’exécutant dans VTL1 est plus privilégié que le code s’exécutant dans VTL0.</span><span class="sxs-lookup"><span data-stu-id="69e02-110">The VTLs are hierarchal meaning any code running in VTL1 is more privileged than code running in VTL0.</span></span>

<span data-ttu-id="69e02-111">L’isolation VTL est créée par l’hyperviseur Hyper-V qui assigne la mémoire au démarrage à l’aide de la traduction d’adresses de second niveau (SLAT).</span><span class="sxs-lookup"><span data-stu-id="69e02-111">The VTL isolation is created by the Hyper-V Hypervisor which assigns memory at boot time using Second Level Address Translation (SLAT).</span></span> <span data-ttu-id="69e02-112">Il continue à s’exécuter de manière dynamique au fur et à mesure que le système s’exécute, en protégeant la mémoire par le noyau sécurisé, ce qui nécessite une protection de VTL0, car il sera utilisé pour contenir des secrets.</span><span class="sxs-lookup"><span data-stu-id="69e02-112">It continues this dynamically as the system runs, protecting memory the Secure Kernel specifies needing protection from VTL0 because it will be used to contain secrets.</span></span> <span data-ttu-id="69e02-113">Comme des blocs de mémoire distincts sont alloués pour les deux VTL, un environnement d’exécution sécurisé est créé pour VTL1 en affectant des blocs de mémoire exclusifs à VTL1 et VTL0 avec les autorisations d’accès appropriées.</span><span class="sxs-lookup"><span data-stu-id="69e02-113">As separate blocks of memory are allocated for the two VTLs, a secure runtime environment is created for VTL1 by assigning exclusive memory blocks to VTL1 and VTL0 with the appropriate access permissions.</span></span>

<span data-ttu-id="69e02-114">**Diagramme 1-architecture IUM**</span><span class="sxs-lookup"><span data-stu-id="69e02-114">**Diagram 1 - IUM Architecture**</span></span>

![diagramme 1-architecture ium](images/uim-architecture.png)

## <a name="trustlets"></a><span data-ttu-id="69e02-116">Trustlets</span><span class="sxs-lookup"><span data-stu-id="69e02-116">Trustlets</span></span>

<span data-ttu-id="69e02-117">Trustlets (également connu sous le nom de processus de confiance, de processus sécurisé ou de processus IUM) sont des programmes qui s’exécutent en tant que processus IUM dans VSM.</span><span class="sxs-lookup"><span data-stu-id="69e02-117">Trustlets (also known as trusted processes, secure processes, or IUM processes) are programs running as IUM processes in VSM.</span></span> <span data-ttu-id="69e02-118">Ils terminent les appels système en les marshalant sur le noyau Windows exécuté dans VTL0 Ring 0.</span><span class="sxs-lookup"><span data-stu-id="69e02-118">They complete system calls by marshalling them over to the Windows kernel running in VTL0 ring 0.</span></span> <span data-ttu-id="69e02-119">VSM crée un petit environnement d’exécution qui comprend le petit noyau sécurisé exécuté dans VTL1 (isolé du noyau et des pilotes s’exécutant dans VTL0).</span><span class="sxs-lookup"><span data-stu-id="69e02-119">VSM creates a small execution environment that includes the small Secure Kernel executing in VTL1 (isolated from the kernel and drivers running in VTL0).</span></span> <span data-ttu-id="69e02-120">L’avantage de sécurité clair est l’isolation des pages en mode utilisateur trustlet dans VTL1 à partir des pilotes exécutés dans le noyau VTL0.</span><span class="sxs-lookup"><span data-stu-id="69e02-120">The clear security benefit is isolation of trustlet user mode pages in VTL1 from drivers running in the VTL0 kernel.</span></span> <span data-ttu-id="69e02-121">Même si le mode noyau de VTL0 est compromis par un programme malveillant, il n’aura pas accès aux pages de processus IUM.</span><span class="sxs-lookup"><span data-stu-id="69e02-121">Even if kernel mode of VTL0 is compromised by malware, it will not have access to the IUM process pages.</span></span>

<span data-ttu-id="69e02-122">Si VSM est activé, l’environnement de l’autorité de sécurité locale (LSASS) s’exécute en tant que trustlet.</span><span class="sxs-lookup"><span data-stu-id="69e02-122">With VSM enabled, the Local Security Authority (LSASS) environment runs as a trustlet.</span></span> <span data-ttu-id="69e02-123">LSASS gère la stratégie système locale, l’authentification des utilisateurs et l’audit tout en gérant les données de sécurité sensibles telles que les hachages de mot de passe et les clés Kerberos.</span><span class="sxs-lookup"><span data-stu-id="69e02-123">LSASS manages the local system policy, user authentication, and auditing while handling sensitive security data such as password hashes and Kerberos keys.</span></span> <span data-ttu-id="69e02-124">Pour tirer parti des avantages de la sécurité VSM, un trustlet nommé LSAISO.exe (LSA isolé) s’exécute dans VTL1 et communique avec LSASS.exe s’exécutant dans VTL0 via un canal RPC.</span><span class="sxs-lookup"><span data-stu-id="69e02-124">To leverage the security benefits of VSM, a trustlet named LSAISO.exe (LSA Isolated) runs in VTL1 and communicates with LSASS.exe running in VTL0 through an RPC channel.</span></span> <span data-ttu-id="69e02-125">Les secrets LSAISO sont chiffrés avant leur envoi à LSASS exécuté en mode normal VSM et les pages de LSAISO sont protégées contre les codes malveillants s’exécutant dans VTL0.</span><span class="sxs-lookup"><span data-stu-id="69e02-125">The LSAISO secrets are encrypted before sending them over to LSASS running in VSM Normal Mode and the pages of LSAISO are protected from malicious code running in VTL0.</span></span>

<span data-ttu-id="69e02-126">**Diagramme 2 – conception de Trustlet LSASS**</span><span class="sxs-lookup"><span data-stu-id="69e02-126">**Diagram 2 – LSASS Trustlet Design**</span></span>

![<span data-ttu-id="69e02-127">Diagramme 2 – conception de trustlet LSASS</span><span class="sxs-lookup"><span data-stu-id="69e02-127">diagram 2 – lsass trustlet design</span></span> ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a><span data-ttu-id="69e02-128">Implications du mode utilisateur isolé (IUM)</span><span class="sxs-lookup"><span data-stu-id="69e02-128">Isolated User Mode (IUM) Implications</span></span>

<span data-ttu-id="69e02-129">Il n’est pas possible d’effectuer un attachement à un processus IUM, ce qui empêche la possibilité de déboguer du code VTL1.</span><span class="sxs-lookup"><span data-stu-id="69e02-129">It is not possible to attach to an IUM process, inhibiting the ability to debug VTL1 code.</span></span> <span data-ttu-id="69e02-130">Cela comprend le débogage à la suite des images mémoire et l’attachement des outils de débogage pour le débogage en direct.</span><span class="sxs-lookup"><span data-stu-id="69e02-130">This includes post mortem debugging of memory dumps and attaching the Debugging Tools for live debugging.</span></span> <span data-ttu-id="69e02-131">Il comprend également les tentatives de comptes privilégiés ou de pilotes de noyau permettant de charger une DLL dans un processus IUM, d’injecter un thread ou de fournir un APC en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="69e02-131">It also includes attempts by privileged accounts or kernel drivers to load a DLL into an IUM process, to inject a thread, or deliver a user-mode APC.</span></span> <span data-ttu-id="69e02-132">De telles tentatives peuvent entraîner une déstabilisation de l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="69e02-132">Such attempts may result in destabilization of the entire system.</span></span> <span data-ttu-id="69e02-133">Les API Windows qui compromettent la sécurité d’un Trustlet peuvent échouer de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="69e02-133">Windows APIs that would compromise the security of a Trustlet may fail in unexpected ways.</span></span> <span data-ttu-id="69e02-134">Par exemple, le chargement d’une DLL dans un Trustlet le rend disponible dans VTL0, mais pas VTL1.</span><span class="sxs-lookup"><span data-stu-id="69e02-134">For example, loading a DLL into a Trustlet will make it available in VTL0 but not VTL1.</span></span> <span data-ttu-id="69e02-135">QueueUserApc peut échouer silencieusement si le thread cible est dans un Trustlet.</span><span class="sxs-lookup"><span data-stu-id="69e02-135">QueueUserApc may silently fail if the target thread is in a Trustlet.</span></span> <span data-ttu-id="69e02-136">D’autres API, telles que CreateRemoteThread, VirtualAllocEx et Read/WriteProcessMemory, ne fonctionneront pas comme prévu en cas d’utilisation sur Trustlets.</span><span class="sxs-lookup"><span data-stu-id="69e02-136">Other APIs, such as CreateRemoteThread, VirtualAllocEx, and Read/WriteProcessMemory will also not work as expected when used against Trustlets.</span></span>

<span data-ttu-id="69e02-137">Utilisez l’exemple de code ci-dessous pour empêcher l’appel de fonctions qui tentent d’attacher ou d’injecter du code dans un processus IUM.</span><span class="sxs-lookup"><span data-stu-id="69e02-137">Use the sample code below to prevent calling any functions which attempt to attach or inject code into an IUM process.</span></span> <span data-ttu-id="69e02-138">Cela comprend les pilotes de noyau qui défilent les APC pour l’exécution de code dans un trustlet.</span><span class="sxs-lookup"><span data-stu-id="69e02-138">This includes kernel drivers that queue APCs for execution of code in a trustlet.</span></span>

## <a name="remarks"></a><span data-ttu-id="69e02-139">Notes</span><span class="sxs-lookup"><span data-stu-id="69e02-139">Remarks</span></span>

<span data-ttu-id="69e02-140">Si l’état de retour de IsSecureProcess est Success, examinez \_ le \_ paramètre out SecureProcess pour déterminer si le processus est un processus ium.</span><span class="sxs-lookup"><span data-stu-id="69e02-140">If the return status of IsSecureProcess is success, examine the SecureProcess \_Out\_ parameter to determine if the process is an IUM process.</span></span> <span data-ttu-id="69e02-141">Les processus IUM sont marqués par le système comme « processus sécurisés ».</span><span class="sxs-lookup"><span data-stu-id="69e02-141">IUM processes are marked by the system to be “Secure Processes”.</span></span> <span data-ttu-id="69e02-142">Un résultat booléen TRUE signifie que le processus cible est de type IUM.</span><span class="sxs-lookup"><span data-stu-id="69e02-142">A Boolean result of TRUE means the target process is of type IUM.</span></span>


```C++
NTSTATUS
IsSecureProcess(
   _In_ HANDLE ProcessHandle,
   _Out_ BOOLEAN *SecureProcess
   )
{
   NTSTATUS status;

       // definition included in ntddk.h  
   PROCESS_EXTENDED_BASIC_INFORMATION extendedInfo = {0};
 
   PAGED_CODE(); 
  
   extendedInfo.Size = sizeof(extendedInfo);

   // Query for the process information  
   status = ZwQueryInformationProcess(
                  ProcessHandle, ProcessBasicInformation, &extendedInfo,
                  sizeof(extendedInfo), NULL);

   if (NT_SUCCESS(status)) {
      *SecureProcess = (BOOLEAN)(extendedInfo.IsSecureProcess != 0);
   }
 
          return status;
}
```



<span data-ttu-id="69e02-143">Le kit WDK pour Windows 10, « Windows Driver Kit-Windows 10.0.15063.0 », contient la définition requise de la \_ structure d’informations de base étendue de processus \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="69e02-143">The WDK for Windows 10, “Windows Driver Kit - Windows 10.0.15063.0”, contains the required definition of the PROCESS\_EXTENDED\_BASIC\_INFORMATION structure.</span></span> <span data-ttu-id="69e02-144">La version mise à jour de la structure est définie dans Ntddk. h avec le nouveau champ IsSecureProcess.</span><span class="sxs-lookup"><span data-stu-id="69e02-144">The updated version of the structure is defined in ntddk.h with the new IsSecureProcess field.</span></span>


```C++
typedef struct _PROCESS_EXTENDED_BASIC_INFORMATION {
    SIZE_T Size;    // Ignored as input, written with structure size on output
    PROCESS_BASIC_INFORMATION BasicInfo;
    union {
        ULONG Flags;
        struct {
            ULONG IsProtectedProcess : 1;
            ULONG IsWow64Process : 1;
            ULONG IsProcessDeleting : 1;
            ULONG IsCrossSessionCreate : 1;
            ULONG IsFrozen : 1;
            ULONG IsBackground : 1;
            ULONG IsStronglyNamed : 1;
            ULONG IsSecureProcess : 1;
            ULONG IsSubsystemProcess : 1;
            ULONG SpareBits : 23;
        } DUMMYSTRUCTNAME;
    } DUMMYUNIONNAME;
} PROCESS_EXTENDED_BASIC_INFORMATION, *PPROCESS_EXTENDED_BASIC_INFORMATION;
```



 

 



