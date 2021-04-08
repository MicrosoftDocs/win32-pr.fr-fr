---
description: Moniteur réseau utilise la fonction d’exportation DllMain pour identifier l’existence de l’analyseur et libère les ressources que Moniteur réseau utilise pour stocker des informations sur l’analyseur.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implémentation de l’analyseur DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750052"
---
# <a name="implementing-dllmain-parser"></a><span data-ttu-id="29507-103">Implémentation de l’analyseur DllMain</span><span class="sxs-lookup"><span data-stu-id="29507-103">Implementing DllMain Parser</span></span>

<span data-ttu-id="29507-104">Moniteur réseau utilise la fonction d’exportation **DllMain** pour identifier l’existence de l’analyseur et libère les ressources que Moniteur réseau utilise pour stocker des informations sur l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="29507-104">Network Monitor uses the **DllMain** export function to identify the existence of the parser, and release resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="29507-105">Lorsque Moniteur réseau appelle **DllMain** pour la première fois, la dll de l’analyseur appelle [**CreateProtocol**](createprotocol.md) pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="29507-105">When Network Monitor calls **DllMain** for the first time, the parser DLL calls [**CreateProtocol**](createprotocol.md) to do the following:</span></span>

-   <span data-ttu-id="29507-106">Spécifiez le protocole détecté par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="29507-106">Specify the protocol that the parser detects.</span></span>
-   <span data-ttu-id="29507-107">Fournissez des points d’entrée pour les autres fonctions d’exportation de l’analyseur qui Moniteur réseaunt les appels.</span><span class="sxs-lookup"><span data-stu-id="29507-107">Provide entry points for remaining parser export functions that Network Monitor calls.</span></span>

<span data-ttu-id="29507-108">Lorsque Moniteur réseau appelle **DllMain** pour la dernière fois, **DllMain** appelle [**DestroyProtocol**](destroyprotocol.md) pour libérer toutes les ressources que Moniteur réseau utilise pour stocker des informations sur l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="29507-108">When Network Monitor calls **DllMain** for the last time, **DllMain** calls [**DestroyProtocol**](destroyprotocol.md) to release all resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="29507-109">La procédure suivante identifie les étapes nécessaires à l’implémentation de **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="29507-109">The following procedure identifies the steps necessary to implement **DllMain**.</span></span>

<span data-ttu-id="29507-110">**Pour implémenter DllMain**</span><span class="sxs-lookup"><span data-stu-id="29507-110">**To implement DllMain**</span></span>

1.  <span data-ttu-id="29507-111">Spécifiez la structure [**ENTRYPOINTS**](entrypoints.md) pour la fonction [**CreateProtocol**](createprotocol.md) et la variable d’attachement globale.</span><span class="sxs-lookup"><span data-stu-id="29507-111">Specify the [**ENTRYPOINTS**](entrypoints.md) structure for the [**CreateProtocol**](createprotocol.md) function and global Attach variable.</span></span> <span data-ttu-id="29507-112">La variable d’attachement est utilisée pour effectuer le suivi du nombre d’instances de protocole en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="29507-112">The Attach variable is used to track the number of protocol instances that are running.</span></span>
2.  <span data-ttu-id="29507-113">Examinez la valeur du paramètre de *commande* défini par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="29507-113">Look at the value of the *Command* parameter that the operating system sets.</span></span>

    <span data-ttu-id="29507-114">Si le paramètre de *commande* est défini sur dll \_ process \_ Attach et Attach a la valeur 0, appelez [**CreateProtocol**](createprotocol.md) pour fournir le nom de protocole et les points d’entrée pour les fonctions d’exportation suivantes.</span><span class="sxs-lookup"><span data-stu-id="29507-114">If the *Command* parameter is set to DLL\_PROCESS\_ATTACH and Attach is 0, then call [**CreateProtocol**](createprotocol.md) to provide the protocol name and entry points for the following export functions.</span></span>

    -   <span data-ttu-id="29507-115">**S’inscrire**</span><span class="sxs-lookup"><span data-stu-id="29507-115">**Register**</span></span>
    -   <span data-ttu-id="29507-116">**Désinscrire**</span><span class="sxs-lookup"><span data-stu-id="29507-116">**Deregister**</span></span>
    -   <span data-ttu-id="29507-117">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="29507-117">**RecognizeFrame**</span></span>
    -   <span data-ttu-id="29507-118">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="29507-118">**AttachProperties**</span></span>
    -   <span data-ttu-id="29507-119">**FormatProperties** (requis uniquement si Moniteur réseau affichera les propriétés de protocole).</span><span class="sxs-lookup"><span data-stu-id="29507-119">**FormatProperties** (only required if Network Monitor will be displaying the protocol properties).</span></span>

    <span data-ttu-id="29507-120">Si le paramètre de *commande* est défini sur \_ détacher le processus de la dll \_ et que Attach a la valeur 0, appelez [**DestroyProtocol**](destroyprotocol.md) à l’aide du handle d’instance retourné par [**CreateProtocol**](createprotocol.md) .</span><span class="sxs-lookup"><span data-stu-id="29507-120">If the *Command* parameter is set to DLL\_PROCESS\_DETACH and Attach is 0, then call [**DestroyProtocol**](destroyprotocol.md) using the instance handle that [**CreateProtocol**](createprotocol.md) returns.</span></span>

3.  <span data-ttu-id="29507-121">Retourne la **valeur true** , car la fonction de l’analyseur **DllMain** doit toujours retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="29507-121">Return **TRUE** because the **DllMain** parser function must always return **TRUE**.</span></span>

<span data-ttu-id="29507-122">Voici une implémentation de base de **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="29507-122">The following is a basic implementation of **DllMain**.</span></span> <span data-ttu-id="29507-123">L’exemple de code utilise une instruction case pour intercepter les valeurs du paramètre *Command* afin de déterminer si [**CreateProtocol**](createprotocol.md) ou [**DestroyProtocol**](destroyprotocol.md) doit être appelé.</span><span class="sxs-lookup"><span data-stu-id="29507-123">The code example uses a case statement to trap values of the *Command* parameter to determine if [**CreateProtocol**](createprotocol.md) or [**DestroyProtocol**](destroyprotocol.md) should be called.</span></span>

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



