---
description: Répertorie les exportations de DLL qui doivent être implémentées pour créer un gestionnaire d’informations d’identification.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implémentation d’un gestionnaire d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867862"
---
# <a name="implementing-a-credential-manager"></a><span data-ttu-id="d0eb2-103">Implémentation d’un gestionnaire d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="d0eb2-103">Implementing a Credential Manager</span></span>

<span data-ttu-id="d0eb2-104">Pour créer un gestionnaire d’informations d’identification, vous devez créer une DLL qui exporte les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0eb2-104">To create a credential manager, you must create a DLL that exports the following functions:</span></span>

-   [<span data-ttu-id="d0eb2-105">**NPLogonNotify**</span><span class="sxs-lookup"><span data-stu-id="d0eb2-105">**NPLogonNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [<span data-ttu-id="d0eb2-106">**NPPasswordChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="d0eb2-106">**NPPasswordChangeNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

<span data-ttu-id="d0eb2-107">Pour restaurer les notifications aux fonctions [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) et [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) pour l’ouverture de session par carte à puce, créez une entrée de Registre appelée **SmartCardLogonNotify** comme **DWORD**, puis définissez-la sur 1 :</span><span class="sxs-lookup"><span data-stu-id="d0eb2-107">To restore notifications to the [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) functions for smart card logon, create a registry entry called **SmartCardLogonNotify** as a **DWORD**, and set it to 1:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

<span data-ttu-id="d0eb2-108">**Windows Server 2003 et Windows XP :** L’entrée de Registre **SmartCardLogonNotify** n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d0eb2-108">**Windows Server 2003 and Windows XP:** The **SmartCardLogonNotify** registry entry is not required.</span></span>

<span data-ttu-id="d0eb2-109">En outre, les gestionnaires d’informations d’identification doivent également prendre en charge la fonction [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) pour le démarrage de WNNC \_ (la prise en charge d’autres index n’est pas requise pour les gestionnaires d’informations d’identification).</span><span class="sxs-lookup"><span data-stu-id="d0eb2-109">In addition, credential managers should also support the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function for WNNC\_START (supporting other indexes is not required for credential managers).</span></span> <span data-ttu-id="d0eb2-110">Cela indique à MPR qu’un gestionnaire d’informations d’identification démarrera.</span><span class="sxs-lookup"><span data-stu-id="d0eb2-110">This tells MPR when a credential manager will start.</span></span> <span data-ttu-id="d0eb2-111">En appelant **NPGetCaps** avec le paramètre *NINDEX* défini sur WNNC \_ Start, le MPR obtient le temps d’attente avant d’appeler les fonctions de point d’entrée de gestion des informations d’identification du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d0eb2-111">By calling **NPGetCaps** with the *nIndex* parameter set to WNNC\_START, the MPR gets the time to wait before calling the provider's credential management entry point functions.</span></span> <span data-ttu-id="d0eb2-112">Et si le MPR dispose de ces informations, il peut le transférer au gestionnaire d’informations d’identification, en définissant le délai d’expiration.</span><span class="sxs-lookup"><span data-stu-id="d0eb2-112">And if the MPR has this information, it can forward it to the credential manager, setting the time out.</span></span>

 

 



