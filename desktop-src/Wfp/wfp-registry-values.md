---
description: 'Les valeurs de Registre WFP se trouvent dans la clé de Registre suivante : HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valeurs de Registre WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533680"
---
# <a name="wfp-registry-values"></a><span data-ttu-id="71825-103">Valeurs de Registre WFP</span><span class="sxs-lookup"><span data-stu-id="71825-103">WFP Registry Values</span></span>

<span data-ttu-id="71825-104">\[Les valeurs de Registre WFP ne sont pas prises en charge à partir de Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="71825-104">\[WFP registry values are not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="71825-105">WFP utilise plusieurs valeurs de Registre pour les paramètres de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="71825-105">WFP uses several registry values for customization settings.</span></span> <span data-ttu-id="71825-106">Les valeurs de Registre WFP se trouvent dans la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="71825-106">The WFP registry values are located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

<span data-ttu-id="71825-107">Voici les valeurs de Registre WFP.</span><span class="sxs-lookup"><span data-stu-id="71825-107">The following are the WFP registry values.</span></span>

<dl> <dt>

<span data-ttu-id="71825-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span><span class="sxs-lookup"><span data-stu-id="71825-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span></span>
</dt> <dd>

<span data-ttu-id="71825-109">Emplacement du cache.</span><span class="sxs-lookup"><span data-stu-id="71825-109">Location of the cache.</span></span> <span data-ttu-id="71825-110">Il doit s’agir d’un chemin d’accès local.</span><span class="sxs-lookup"><span data-stu-id="71825-110">This must be a local path.</span></span> <span data-ttu-id="71825-111">La valeur par défaut est% SystemRoot% \\ system32 \\ dllcache.</span><span class="sxs-lookup"><span data-stu-id="71825-111">The default value is %systemroot%\\system32\\dllcache.</span></span>

</dd> <dt>

<span data-ttu-id="71825-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span><span class="sxs-lookup"><span data-stu-id="71825-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span></span>
</dt> <dd>

<span data-ttu-id="71825-113">Options de quota.</span><span class="sxs-lookup"><span data-stu-id="71825-113">Quota options.</span></span> <span data-ttu-id="71825-114">Cette valeur de Registre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="71825-114">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="71825-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="71825-115">Value</span></span>                  | <span data-ttu-id="71825-116">Signification</span><span class="sxs-lookup"><span data-stu-id="71825-116">Meaning</span></span>                                                  |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="71825-117">QUOTA SFC- \_ \_ tous les \_ fichiers</span><span class="sxs-lookup"><span data-stu-id="71825-117">SFC\_QUOTA\_ALL\_FILES</span></span> | <span data-ttu-id="71825-118">La taille du cache DLL est illimitée.</span><span class="sxs-lookup"><span data-stu-id="71825-118">Size of the DLL cache is unlimited.</span></span> <span data-ttu-id="71825-119">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="71825-119">This is the default.</span></span> |
| <span data-ttu-id="71825-120">Autres valeurs</span><span class="sxs-lookup"><span data-stu-id="71825-120">Other values</span></span>           | <span data-ttu-id="71825-121">Taille du cache DLL, dans les fichiers.</span><span class="sxs-lookup"><span data-stu-id="71825-121">Size of the DLL cache, in files.</span></span>                         |



 

</dd> <dt>

<span data-ttu-id="71825-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span><span class="sxs-lookup"><span data-stu-id="71825-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span></span>
</dt> <dd>

<span data-ttu-id="71825-123">Options d’analyse.</span><span class="sxs-lookup"><span data-stu-id="71825-123">Scan options.</span></span> <span data-ttu-id="71825-124">Cette valeur de Registre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="71825-124">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="71825-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="71825-125">Value</span></span>             | <span data-ttu-id="71825-126">Signification</span><span class="sxs-lookup"><span data-stu-id="71825-126">Meaning</span></span>                                                   |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="71825-127">\_analyse SFC \_ normale</span><span class="sxs-lookup"><span data-stu-id="71825-127">SFC\_SCAN\_NORMAL</span></span> | <span data-ttu-id="71825-128">N’analyse pas les fichiers protégés au démarrage.</span><span class="sxs-lookup"><span data-stu-id="71825-128">Do not scan protected files at boot.</span></span> <span data-ttu-id="71825-129">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="71825-129">This is the default.</span></span> |
| <span data-ttu-id="71825-130">\_toujours analyser \_ SFC</span><span class="sxs-lookup"><span data-stu-id="71825-130">SFC\_SCAN\_ALWAYS</span></span> | <span data-ttu-id="71825-131">Analyser les fichiers protégés à chaque démarrage.</span><span class="sxs-lookup"><span data-stu-id="71825-131">Scan protected files at every boot.</span></span>                       |
| <span data-ttu-id="71825-132">\_analyse SFC \_ une seule fois</span><span class="sxs-lookup"><span data-stu-id="71825-132">SFC\_SCAN\_ONCE</span></span>   | <span data-ttu-id="71825-133">Analyser les fichiers protégés au prochain démarrage.</span><span class="sxs-lookup"><span data-stu-id="71825-133">Scan protected files at the next boot.</span></span>                    |



 

</dd> </dl>

 

 



