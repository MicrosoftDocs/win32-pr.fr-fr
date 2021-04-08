---
title: Inscription d’une DLL de sécurité RAS
description: Le programme d’installation d’une DLL de sécurité RAS doit inscrire la DLL auprès du serveur RAS Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672773"
---
# <a name="registering-a-ras-security-dll"></a><span data-ttu-id="f7e13-103">Inscription d’une DLL de sécurité RAS</span><span class="sxs-lookup"><span data-stu-id="f7e13-103">Registering a RAS Security DLL</span></span>

<span data-ttu-id="f7e13-104">Le programme d’installation d’une DLL de sécurité RAS doit inscrire la DLL auprès du serveur RAS Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f7e13-104">The setup program for a RAS security DLL must register the DLL with the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="f7e13-105">Une seule DLL de sécurité RAS peut être inscrite, car la prise en charge de plusieurs dll de sécurité n’est pas fournie.</span><span class="sxs-lookup"><span data-stu-id="f7e13-105">Only one RAS security DLL can be registered as support for multiple security DLLs is not provided.</span></span> <span data-ttu-id="f7e13-106">Pour inscrire une DLL de sécurité RAS, définissez la valeur *DllPath* sous la clé suivante dans le registre :</span><span class="sxs-lookup"><span data-stu-id="f7e13-106">To register a RAS security DLL, set the *DLLPath* value under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| <span data-ttu-id="f7e13-107">Nom de la valeur</span><span class="sxs-lookup"><span data-stu-id="f7e13-107">Value name</span></span> | <span data-ttu-id="f7e13-108">Données de valeur</span><span class="sxs-lookup"><span data-stu-id="f7e13-108">Value data</span></span>                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e13-109">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="f7e13-109">*DLLPath*</span></span>  | <span data-ttu-id="f7e13-110">Chaîne **\_ SZ reg** qui contient le chemin d’accès de la dll.</span><span class="sxs-lookup"><span data-stu-id="f7e13-110">A **REG\_SZ** string that contains the path of the DLL.</span></span> <span data-ttu-id="f7e13-111">Cette chaîne doit spécifier le chemin d’accès complet, sauf si la DLL se trouve dans un répertoire listé dans le chemin d’accès système.</span><span class="sxs-lookup"><span data-stu-id="f7e13-111">This string should specify the full path unless the DLL is in a directory listed in the system path.</span></span> |



 

<span data-ttu-id="f7e13-112">Le programme d’installation d’une DLL de sécurité RAS doit également fournir des fonctionnalités de suppression/désinstallation.</span><span class="sxs-lookup"><span data-stu-id="f7e13-112">The setup program for a RAS security DLL must also provide remove/uninstall functionality.</span></span> <span data-ttu-id="f7e13-113">Si un utilisateur supprime la DLL, le programme d’installation doit supprimer la valeur *DllPath* du Registre.</span><span class="sxs-lookup"><span data-stu-id="f7e13-113">If a user removes the DLL, the setup program must delete the *DLLPath* value from the registry.</span></span> <span data-ttu-id="f7e13-114">Le service RAS ne démarre pas si la valeur *DllPath* spécifie une dll qui est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f7e13-114">The RAS service does not start if the *DLLPath* value specifies a DLL that cannot be found.</span></span>

<span data-ttu-id="f7e13-115">Une DLL de sécurité RAS doit exporter les fonctions [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) et [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) .</span><span class="sxs-lookup"><span data-stu-id="f7e13-115">A RAS security DLL must export the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) and [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) functions.</span></span>

 

 




