---
description: Bien qu’il existe peu de limites techniques quant au type et à la taille des données qu’une application peut stocker dans le registre, certaines recommandations pratiques existent pour favoriser l’efficacité du système.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Espace de stockage du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533928"
---
# <a name="registry-storage-space"></a><span data-ttu-id="50dd5-103">Espace de stockage du Registre</span><span class="sxs-lookup"><span data-stu-id="50dd5-103">Registry Storage Space</span></span>

<span data-ttu-id="50dd5-104">Bien qu’il existe peu de limites techniques quant au type et à la taille des données qu’une application peut stocker dans le registre, certaines recommandations pratiques existent pour favoriser l’efficacité du système.</span><span class="sxs-lookup"><span data-stu-id="50dd5-104">Although there are few technical limits to the type and size of data an application can store in the registry, certain practical guidelines exist to promote system efficiency.</span></span> <span data-ttu-id="50dd5-105">Une application doit stocker des données de configuration et d’initialisation dans le registre, et stocker d’autres types de données ailleurs.</span><span class="sxs-lookup"><span data-stu-id="50dd5-105">An application should store configuration and initialization data in the registry, and store other kinds of data elsewhere.</span></span>

<span data-ttu-id="50dd5-106">En règle générale, les données composées de plus d’un ou de deux kilo-octets (K) doivent être stockées en tant que fichier et référencées à l’aide d’une clé dans le registre plutôt que d’être stockées comme valeur.</span><span class="sxs-lookup"><span data-stu-id="50dd5-106">Generally, data consisting of more than one or two kilobytes (K) should be stored as a file and referred to by using a key in the registry rather than being stored as a value.</span></span> <span data-ttu-id="50dd5-107">Au lieu de dupliquer de grands éléments de données dans le registre, une application doit enregistrer les données en tant que fichier et faire référence au fichier.</span><span class="sxs-lookup"><span data-stu-id="50dd5-107">Instead of duplicating large pieces of data in the registry, an application should save the data as a file and refer to the file.</span></span> <span data-ttu-id="50dd5-108">Le code binaire exécutable ne doit jamais être stocké dans le registre.</span><span class="sxs-lookup"><span data-stu-id="50dd5-108">Executable binary code should never be stored in the registry.</span></span>

<span data-ttu-id="50dd5-109">Une entrée de valeur utilise un espace de registre bien inférieur à celui d’une clé.</span><span class="sxs-lookup"><span data-stu-id="50dd5-109">A value entry uses much less registry space than a key.</span></span> <span data-ttu-id="50dd5-110">Pour économiser de l’espace, une application doit regrouper des données similaires en tant que structure et stocker la structure en tant que valeur au lieu de stocker chacun des membres de la structure sous la forme d’une clé distincte.</span><span class="sxs-lookup"><span data-stu-id="50dd5-110">To save space, an application should group similar data together as a structure and store the structure as a value rather than storing each of the structure members as a separate key.</span></span> <span data-ttu-id="50dd5-111">(Le stockage des données sous forme binaire permet à une application de stocker des données en une seule valeur qui serait autrement constituée de plusieurs types incompatibles.)</span><span class="sxs-lookup"><span data-stu-id="50dd5-111">(Storing the data in binary form allows an application to store data in one value that would otherwise be made up of several incompatible types.)</span></span>

<span data-ttu-id="50dd5-112">Les affichages des fichiers du Registre sont mappés dans la mémoire de réserve paginée.</span><span class="sxs-lookup"><span data-stu-id="50dd5-112">Views of the registry files are mapped in paged pool memory.</span></span>

<span data-ttu-id="50dd5-113">**Windows server 2008 pour 32 bits, Windows Vista avec SP1 pour 32 bits, Windows Vista, Windows Server 2003, Windows XP :** Les affichages des fichiers du Registre sont mappés dans l’espace d’adressage du cache de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="50dd5-113">**Windows Server 2008 for 32-bit, Windows Vista with SP1 for 32-bit, Windows Vista, Windows Server 2003, Windows XP:** Views of the registry files are mapped in the computer cache address space.</span></span> <span data-ttu-id="50dd5-114">Par conséquent, quelle que soit la taille des données du Registre, il n’y a pas de facturation supérieure à 4 mégaoctets (Mo).</span><span class="sxs-lookup"><span data-stu-id="50dd5-114">Therefore, regardless of the size of the registry data, it is not charged more than 4 megabytes (MB).</span></span>

<span data-ttu-id="50dd5-115">La taille maximale d’une ruche de Registre est de 2 Go, à l’exception de la ruche système.</span><span class="sxs-lookup"><span data-stu-id="50dd5-115">The maximum size of a registry hive is 2 GB, except for the system hive.</span></span>

<span data-ttu-id="50dd5-116">**Windows server 2003 avec SP1, Windows server 2003 et Windows XP :** Il n’existe aucune limite explicite quant à la quantité d’espace totale pouvant être consommée par les ruches dans la mémoire de réserve paginée et dans l’espace disque, bien que les quotas système puissent affecter la taille maximale réelle.</span><span class="sxs-lookup"><span data-stu-id="50dd5-116">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** There are no explicit limits on the total amount of space that may be consumed by hives in paged pool memory and in disk space, although system quotas may affect the actual maximum size.</span></span> <span data-ttu-id="50dd5-117">La taille maximale d’une ruche de registre était limitée à 2 Go à compter de Windows Server 2003 avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="50dd5-117">The maximum size of a registry hive was limited to 2 GB starting with Windows Server 2003 with Service Pack 2 (SP2).</span></span>

<span data-ttu-id="50dd5-118">La taille maximale de la ruche système est limitée par la mémoire physique, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="50dd5-118">The maximum size of the system hive is limited by physical memory as shown in the following table.</span></span> 

| <span data-ttu-id="50dd5-119">Système</span><span class="sxs-lookup"><span data-stu-id="50dd5-119">System</span></span>                      | <span data-ttu-id="50dd5-120">Taille maximale de la ruche système</span><span class="sxs-lookup"><span data-stu-id="50dd5-120">Maximum size of the system hive</span></span>                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dd5-121">systèmes basés sur x86</span><span class="sxs-lookup"><span data-stu-id="50dd5-121">x86-based systems</span></span>           | <span data-ttu-id="50dd5-122">50% de la mémoire physique, jusqu’à 400 Mo. **Windows server 2003 avec SP2, Windows server 2003 avec SP1, Windows server 2003 et Windows XP :** 25% de la mémoire physique, jusqu’à 200 Mo.</span><span class="sxs-lookup"><span data-stu-id="50dd5-122">50 percent of physical memory, up to 400 MB.**Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** 25 percent of physical memory, up to 200 MB.</span></span><br/>                                    |
| <span data-ttu-id="50dd5-123">systèmes basés sur x64</span><span class="sxs-lookup"><span data-stu-id="50dd5-123">x64-based systems</span></span>           | <span data-ttu-id="50dd5-124">50% de la mémoire physique, jusqu’à 1,5 Go. **Windows Server 2003 avec SP2 :** 25% de la mémoire système, jusqu’à 200 Mo.</span><span class="sxs-lookup"><span data-stu-id="50dd5-124">50 percent of physical memory, up to 1.5 GB.**Windows Server 2003 with SP2:** 25 percent of system memory, up to 200 MB.</span></span><br/> <span data-ttu-id="50dd5-125">**Windows server 2003 avec SP1, Windows server 2003 et Windows XP 64-bit Edition :** 32 Mo.</span><span class="sxs-lookup"><span data-stu-id="50dd5-125">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/> |
| <span data-ttu-id="50dd5-126">Systèmes basés sur Intel Itanium</span><span class="sxs-lookup"><span data-stu-id="50dd5-126">Intel Itanium-based systems</span></span> | <span data-ttu-id="50dd5-127">50% de la mémoire physique, jusqu’à 1 Go. **Windows server 2008, Windows Vista, Windows server 2003 avec SP2, Windows server 2003 avec SP1, Windows server 2003 et Windows XP édition 64 bits :** 32 Mo.</span><span class="sxs-lookup"><span data-stu-id="50dd5-127">50 percent of physical memory, up to 1 GB.**Windows Server 2008, Windows Vista, Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/>                         |



 

## <a name="windows-2000"></a><span data-ttu-id="50dd5-128">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="50dd5-128">Windows 2000</span></span>

<span data-ttu-id="50dd5-129">Les données du Registre sont stockées dans la réserve paginée, une zone de mémoire physique utilisée pour les données système qui peuvent être écrites sur le disque quand elles ne sont pas utilisées.</span><span class="sxs-lookup"><span data-stu-id="50dd5-129">Registry data is stored in the paged pool, an area of physical memory used for system data that can be written to disk when not in use.</span></span> <span data-ttu-id="50dd5-130">La valeur **RegistrySizeLimit** établit la quantité maximale de réserve paginée pouvant être consommée par les données de registre de toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="50dd5-130">The **RegistrySizeLimit** value establishes the maximum amount of paged pool that can be consumed by registry data from all applications.</span></span> <span data-ttu-id="50dd5-131">Cette valeur se trouve dans la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="50dd5-131">This value is located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

<span data-ttu-id="50dd5-132">Par défaut, la limite de taille du Registre est de 25% de la réserve paginée.</span><span class="sxs-lookup"><span data-stu-id="50dd5-132">By default, the registry size limit is 25 percent of the paged pool.</span></span> <span data-ttu-id="50dd5-133">(La taille par défaut de la réserve paginée est de 32 Mo. il s’agit donc de 8 Mo.) Le système vérifie que la valeur minimale de **RegistrySizeLimit** est de 4 Mo et la valeur maximale est environ 80% de la valeur **PagedPoolSize** .</span><span class="sxs-lookup"><span data-stu-id="50dd5-133">(The default size of the paged pool is 32 MB, so this is 8 MB.) The system ensures that the minimum value of **RegistrySizeLimit** is 4 MB and the maximum is approximately 80 percent of the **PagedPoolSize** value.</span></span> <span data-ttu-id="50dd5-134">Si la valeur de cette entrée est supérieure à 80% de la taille de la réserve paginée, le système définit la taille maximale du Registre à 80% de la taille de la réserve paginée.</span><span class="sxs-lookup"><span data-stu-id="50dd5-134">If the value of this entry is greater than 80 percent of the size of the paged pool, the system sets the maximum size of the registry to 80 percent of the size of the paged pool.</span></span> <span data-ttu-id="50dd5-135">Cela empêche le registre de consommer l’espace requis par les processus.</span><span class="sxs-lookup"><span data-stu-id="50dd5-135">This prevents the registry from consuming space needed by processes.</span></span> <span data-ttu-id="50dd5-136">Notez que la définition de cette valeur n’alloue pas d’espace dans la réserve paginée et ne garantit pas que l’espace sera disponible si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="50dd5-136">Note that setting this value does not allocate space in the paged pool, nor does it assure that the space will be available if needed.</span></span>

<span data-ttu-id="50dd5-137">La taille de la réserve paginée est déterminée par la valeur **PagedPoolSize** dans la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="50dd5-137">The paged pool size is determined by the **PagedPoolSize** value in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

<span data-ttu-id="50dd5-138">Pour obtenir un exemple de la façon de déterminer la taille actuelle et la taille maximale du Registre, consultez [détermination de la taille du Registre](determining-the-registry-size.md).</span><span class="sxs-lookup"><span data-stu-id="50dd5-138">For an example of how to determine the current and maximum sizes of the registry, see [Determining the Registry Size](determining-the-registry-size.md).</span></span>

<span data-ttu-id="50dd5-139">La taille maximale de la réserve paginée est d’environ 300 470 Mo, de sorte que la limite de la taille du Registre est de 240-376 Mo.</span><span class="sxs-lookup"><span data-stu-id="50dd5-139">The maximum paged pool is approximately 300,470 MB so the registry size limit is 240-376 MB.</span></span> <span data-ttu-id="50dd5-140">Toutefois, si le commutateur/3GB est utilisé, la taille maximale de la réserve paginée est de 192 Mo, de sorte que le registre peut comporter jusqu’à 153,6 Mo.</span><span class="sxs-lookup"><span data-stu-id="50dd5-140">However, if the /3GB switch is used, the maximum paged pool size is 192 MB, so the registry can be a maximum of 153.6 MB.</span></span>

 

 




