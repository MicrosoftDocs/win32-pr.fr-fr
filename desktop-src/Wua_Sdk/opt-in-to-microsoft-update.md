---
description: Vous pouvez choisir un ordinateur dans le service Microsoft Update, puis inscrire ce service auprès de Mises à jour automatiques.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In à Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112155"
---
# <a name="opt-in-to-microsoft-update"></a><span data-ttu-id="6ad0e-103">Opt-In à Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="6ad0e-103">Opt-In to Microsoft Update</span></span>

<span data-ttu-id="6ad0e-104">Vous pouvez choisir un ordinateur dans le service Microsoft Update, puis inscrire ce service auprès de Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-104">You can opt a computer in to the Microsoft Update service and then register that service with Automatic Updates.</span></span>

<span data-ttu-id="6ad0e-105">L’exemple de script de cette rubrique montre comment utiliser Windows Update Agent (WUA) pour inscrire le service Microsoft Update avec Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-105">The scripting sample in this topic shows you how to use Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="6ad0e-106">Sinon, pour inscrire le service, l’utilisateur peut visiter Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-106">Alternatively, to register the service, the user can visit Microsoft Update.</span></span>

<span data-ttu-id="6ad0e-107">Avant de tenter d’exécuter cet exemple, vérifiez que la version de WUA installée sur l’ordinateur est la version 7.0.6000 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-107">Before you attempt to run this sample, verify that the version of WUA that is installed on the computer is version 7.0.6000 or a later version.</span></span> <span data-ttu-id="6ad0e-108">Pour plus d’informations sur la façon de déterminer la version de WUA installée, consultez [détermination de la version actuelle de WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="6ad0e-108">For more information about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>

## <a name="example"></a><span data-ttu-id="6ad0e-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ad0e-109">Example</span></span>

<span data-ttu-id="6ad0e-110">L’exemple de script suivant montre comment utiliser l’agent de Windows Update (WUA) pour inscrire le service Microsoft Update avec Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-110">The following scripting sample shows you how to use the Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="6ad0e-111">L’exemple autorise le traitement différé ou hors connexion si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-111">The sample allows deferred or offline processing if needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ad0e-112">Ce script est destiné à illustrer l’utilisation des API d’agent Windows Update et fournit un exemple de la façon dont les développeurs peuvent utiliser ces API pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-112">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="6ad0e-113">Ce script n’est pas conçu comme un code de production, et le script lui-même n’est pas pris en charge par Microsoft (bien que les API de l’agent de Windows Update sous-jacent soient prises en charge).</span><span class="sxs-lookup"><span data-stu-id="6ad0e-113">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



<span data-ttu-id="6ad0e-114">Dans les versions antérieures de WUA (version WUA minimale de 7.0.6000), vous pouvez simplifier le processus d’abonnement à l’aide d’un paramètre du Registre.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-114">In earlier versions of WUA (a minimum WUA version of 7.0.6000), you can simplify the opt-in process by using a registry setting.</span></span> <span data-ttu-id="6ad0e-115">Une fois la clé de Registre et les valeurs configurées, le Microsoft Update processus d’abonnement se produit la prochaine fois que WUA effectue une recherche.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-115">After the registry key and values are configured, the Microsoft Update opt-in process occurs the next time WUA performs a search.</span></span> <span data-ttu-id="6ad0e-116">Le processus d’abonnement peut être déclenché par Mises à jour automatiques ou par un appelant d’API.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-116">The opt-in process may be triggered by Automatic Updates or by an API caller.</span></span>

<span data-ttu-id="6ad0e-117">Par exemple, le chemin d’accès complet de la clé de Registre et les valeurs à définir pour le processus d’abonnement sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6ad0e-117">For example, the full path of the registry key and values to set for the opt-in process are as follows:</span></span>

<span data-ttu-id="6ad0e-118">**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **PendingServiceRegistration** \\ **7971f918-A847-4430-9279-4a52d1efe18d**</span><span class="sxs-lookup"><span data-stu-id="6ad0e-118">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**WindowsUpdate**\\**PendingServiceRegistration**\\**7971f918-a847-4430-9279-4a52d1efe18d**</span></span>

<span data-ttu-id="6ad0e-119">**ClientApplicationID** = mon application</span><span class="sxs-lookup"><span data-stu-id="6ad0e-119">**ClientApplicationID** = My App</span></span>

<span data-ttu-id="6ad0e-120">**RegisterWithAU** = 1</span><span class="sxs-lookup"><span data-stu-id="6ad0e-120">**RegisterWithAU** = 1</span></span>

> [!Note]
>
> <span data-ttu-id="6ad0e-121">La clé de Registre est respectée une seule fois lorsque WUA est mis à jour à partir d’une version antérieure à la version 7.0.6000 vers la version 7.0.6000 ou vers une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-121">The registry key is respected once only when WUA is updated from a version that is earlier than version 7.0.6000 to version 7.0.6000 or to a later version.</span></span> <span data-ttu-id="6ad0e-122">Nous vous recommandons d’utiliser le remplacement des valeurs de Registre existantes, car le remplacement des valeurs peut modifier le résultat d’une demande d’inscription de service antérieure.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-122">We recommend discretion when overwriting existing registry values because overwriting the values may change the result of an earlier service registration request.</span></span>
>
> <span data-ttu-id="6ad0e-123">La création de cette clé de Registre nécessite des informations d’identification d’administration.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-123">Creating this registry key requires administrative credentials.</span></span> <span data-ttu-id="6ad0e-124">Pour Windows Vista, l’appelant doit créer la clé de Registre dans un processus avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="6ad0e-124">For Windows Vista, the caller must create the registry key in an elevated process.</span></span>

 

 

 



