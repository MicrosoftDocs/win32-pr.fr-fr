---
title: À propos de la configuration du registre des DLL d’administration RAS
description: Comprendre la configuration requise pour l’inscription d’une DLL d’administration du service d’accès à distance (RAS) tierce avec RAS. RAS prend en charge plusieurs DLL d’administration RAS.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Administration RAS RRAS, configuration du registre DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9a7b7c48422264a890a74b1bab36e61672f11d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406662"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="f9278-105">À propos de la configuration du registre des DLL d’administration RAS</span><span class="sxs-lookup"><span data-stu-id="f9278-105">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="f9278-106">Le programme d’installation d’une DLL d’administration RAS tierce doit inscrire la DLL auprès de RAS en fournissant des informations sous la clé suivante dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f9278-106">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="f9278-107">Pour inscrire la DLL, définissez les valeurs suivantes sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="f9278-107">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="f9278-108">Nom de la valeur</span><span class="sxs-lookup"><span data-stu-id="f9278-108">Value name</span></span>    | <span data-ttu-id="f9278-109">Données de valeur</span><span class="sxs-lookup"><span data-stu-id="f9278-109">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="f9278-110">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="f9278-110">*DisplayName*</span></span> | <span data-ttu-id="f9278-111">Chaîne **\_ SZ reg** qui contient le nom complet convivial de la dll.</span><span class="sxs-lookup"><span data-stu-id="f9278-111">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="f9278-112">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="f9278-112">*DLLPath*</span></span>     | <span data-ttu-id="f9278-113">Chaîne **\_ SZ reg** contenant le chemin d’accès complet de la dll.</span><span class="sxs-lookup"><span data-stu-id="f9278-113">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="f9278-114">Étant donné que RAS prend en charge plusieurs DLL d’administration RAS, la valeur de Registre **DllPath** peut contenir une liste de chemins séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="f9278-114">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="f9278-115">Par exemple, l’entrée de Registre pour une DLL d’administration RAS d’une société fictive nommée ProElectron, Inc., peut être la suivante :</span><span class="sxs-lookup"><span data-stu-id="f9278-115">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="f9278-116">*DisplayName*: **reg \_ SZ** : dll d’administration RAS ProElectron</span><span class="sxs-lookup"><span data-stu-id="f9278-116">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="f9278-117">*DllPath*: **reg \_ SZ** : C : \\ NT \\ system32 \\ntwkadm.dll ; C : \\ NT \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="f9278-117">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="f9278-118">RAS appelle les dll dans l’ordre dans lequel elles sont répertoriées dans cette valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="f9278-118">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="f9278-119">La valeur de Registre *DisplayName* ne contient toujours qu’un seul nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f9278-119">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="f9278-120">Le programme d’installation d’une DLL d’administration RAS doit également fournir des fonctionnalités de suppression et de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="f9278-120">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="f9278-121">Si un utilisateur supprime la DLL, le programme d’installation doit supprimer les entrées de Registre pour la DLL.</span><span class="sxs-lookup"><span data-stu-id="f9278-121">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="f9278-122">**Windows 2000/NT :** RAS ne prenant en charge qu’une seule DLL d’administration RAS, la valeur de Registre **DllPath** ne peut pas contenir une liste de chemins séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="f9278-122">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




