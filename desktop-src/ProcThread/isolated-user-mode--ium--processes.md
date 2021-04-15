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
# <a name="isolated-user-mode-ium-processes"></a>Processus de mode utilisateur isolé (IUM)

Windows 10 a introduit une nouvelle fonctionnalité de sécurité nommée VSM (Virtual Secure mode). VSM s’appuie sur l’hyperviseur Hyper-V et la traduction d’adresses de second niveau (SLAT) pour créer un ensemble de modes appelés « niveaux de confiance virtuels » (VTL). Cette nouvelle architecture logicielle crée une limite de sécurité pour empêcher les processus s’exécutant dans une VTL d’accéder à la mémoire d’une autre VTL. L’avantage de cette isolation comprend une atténuation supplémentaire des attaques de noyau, tout en protégeant les ressources telles que les hachages de mot de passe et les clés Kerberos.

Le diagramme 1 illustre le modèle traditionnel de code en mode noyau et en mode utilisateur exécuté dans l’anneau d’UC 0 et l’anneau 3, respectivement. Dans ce nouveau modèle, le code qui s’exécute dans le modèle traditionnel s’exécute dans VTL0 et il ne peut pas accéder aux VTL1 privilégiés les plus élevés, où le noyau sécurisé et le mode utilisateur isolé (IUM) exécutent du code. Les VTL sont hiérarchiquement, ce qui signifie que tout code s’exécutant dans VTL1 est plus privilégié que le code s’exécutant dans VTL0.

L’isolation VTL est créée par l’hyperviseur Hyper-V qui assigne la mémoire au démarrage à l’aide de la traduction d’adresses de second niveau (SLAT). Il continue à s’exécuter de manière dynamique au fur et à mesure que le système s’exécute, en protégeant la mémoire par le noyau sécurisé, ce qui nécessite une protection de VTL0, car il sera utilisé pour contenir des secrets. Comme des blocs de mémoire distincts sont alloués pour les deux VTL, un environnement d’exécution sécurisé est créé pour VTL1 en affectant des blocs de mémoire exclusifs à VTL1 et VTL0 avec les autorisations d’accès appropriées.

**Diagramme 1-architecture IUM**

![diagramme 1-architecture ium](images/uim-architecture.png)

## <a name="trustlets"></a>Trustlets

Trustlets (également connu sous le nom de processus de confiance, de processus sécurisé ou de processus IUM) sont des programmes qui s’exécutent en tant que processus IUM dans VSM. Ils terminent les appels système en les marshalant sur le noyau Windows exécuté dans VTL0 Ring 0. VSM crée un petit environnement d’exécution qui comprend le petit noyau sécurisé exécuté dans VTL1 (isolé du noyau et des pilotes s’exécutant dans VTL0). L’avantage de sécurité clair est l’isolation des pages en mode utilisateur trustlet dans VTL1 à partir des pilotes exécutés dans le noyau VTL0. Même si le mode noyau de VTL0 est compromis par un programme malveillant, il n’aura pas accès aux pages de processus IUM.

Si VSM est activé, l’environnement de l’autorité de sécurité locale (LSASS) s’exécute en tant que trustlet. LSASS gère la stratégie système locale, l’authentification des utilisateurs et l’audit tout en gérant les données de sécurité sensibles telles que les hachages de mot de passe et les clés Kerberos. Pour tirer parti des avantages de la sécurité VSM, un trustlet nommé LSAISO.exe (LSA isolé) s’exécute dans VTL1 et communique avec LSASS.exe s’exécutant dans VTL0 via un canal RPC. Les secrets LSAISO sont chiffrés avant leur envoi à LSASS exécuté en mode normal VSM et les pages de LSAISO sont protégées contre les codes malveillants s’exécutant dans VTL0.

**Diagramme 2 – conception de Trustlet LSASS**

![Diagramme 2 – conception de trustlet LSASS ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>Implications du mode utilisateur isolé (IUM)

Il n’est pas possible d’effectuer un attachement à un processus IUM, ce qui empêche la possibilité de déboguer du code VTL1. Cela comprend le débogage à la suite des images mémoire et l’attachement des outils de débogage pour le débogage en direct. Il comprend également les tentatives de comptes privilégiés ou de pilotes de noyau permettant de charger une DLL dans un processus IUM, d’injecter un thread ou de fournir un APC en mode utilisateur. De telles tentatives peuvent entraîner une déstabilisation de l’ensemble du système. Les API Windows qui compromettent la sécurité d’un Trustlet peuvent échouer de manière inattendue. Par exemple, le chargement d’une DLL dans un Trustlet le rend disponible dans VTL0, mais pas VTL1. QueueUserApc peut échouer silencieusement si le thread cible est dans un Trustlet. D’autres API, telles que CreateRemoteThread, VirtualAllocEx et Read/WriteProcessMemory, ne fonctionneront pas comme prévu en cas d’utilisation sur Trustlets.

Utilisez l’exemple de code ci-dessous pour empêcher l’appel de fonctions qui tentent d’attacher ou d’injecter du code dans un processus IUM. Cela comprend les pilotes de noyau qui défilent les APC pour l’exécution de code dans un trustlet.

## <a name="remarks"></a>Notes

Si l’état de retour de IsSecureProcess est Success, examinez \_ le \_ paramètre out SecureProcess pour déterminer si le processus est un processus ium. Les processus IUM sont marqués par le système comme « processus sécurisés ». Un résultat booléen TRUE signifie que le processus cible est de type IUM.


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



Le kit WDK pour Windows 10, « Windows Driver Kit-Windows 10.0.15063.0 », contient la définition requise de la \_ structure d’informations de base étendue de processus \_ \_ . La version mise à jour de la structure est définie dans Ntddk. h avec le nouveau champ IsSecureProcess.


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



 

 



