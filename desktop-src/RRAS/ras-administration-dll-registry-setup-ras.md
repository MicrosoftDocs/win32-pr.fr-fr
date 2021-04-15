---
title: Configuration du registre des DLL d’administration RAS
description: Le programme d’installation d’une DLL d’administration RAS tierce doit inscrire la DLL auprès de RAS en fournissant des informations sous la clé suivante dans le registre.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507406"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="2e4bb-103">Configuration du registre des DLL d’administration RAS</span><span class="sxs-lookup"><span data-stu-id="2e4bb-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="2e4bb-104">Le programme d’installation d’une DLL d’administration RAS tierce doit inscrire la DLL auprès de RAS en fournissant des informations sous la clé suivante dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2e4bb-105">Pour inscrire la DLL, définissez les valeurs suivantes sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="2e4bb-106">Nom de la valeur</span><span class="sxs-lookup"><span data-stu-id="2e4bb-106">Value name</span></span>    | <span data-ttu-id="2e4bb-107">Données de valeur</span><span class="sxs-lookup"><span data-stu-id="2e4bb-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="2e4bb-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="2e4bb-108">*DisplayName*</span></span> | <span data-ttu-id="2e4bb-109">Chaîne **\_ SZ reg** qui contient le nom complet convivial de la dll.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="2e4bb-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="2e4bb-110">*DLLPath*</span></span>     | <span data-ttu-id="2e4bb-111">Chaîne **\_ SZ reg** contenant le chemin d’accès complet de la dll.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="2e4bb-112">Par exemple, l’entrée de Registre pour une DLL d’administration RAS d’une société fictive nommée ProElectron, Inc. peut être :</span><span class="sxs-lookup"><span data-stu-id="2e4bb-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2e4bb-113">*DisplayName* : **reg \_ SZ** : dll d’administration RAS ProElectron</span><span class="sxs-lookup"><span data-stu-id="2e4bb-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="2e4bb-114">*DllPath* : **reg \_ SZ** : C : \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="2e4bb-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="2e4bb-115">Le programme d’installation d’une DLL d’administration RAS doit également fournir des fonctionnalités de suppression/désinstallation.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="2e4bb-116">Si un utilisateur supprime la DLL, le programme d’installation doit supprimer les entrées de registre de la DLL.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




