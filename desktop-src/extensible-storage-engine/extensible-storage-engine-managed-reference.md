---
description: 'En savoir plus sur : référence gérée par le moteur de stockage extensible'
title: Référence gérée du moteur de stockage extensible
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034168"
---
# <a name="extensible-storage-engine-managed-reference"></a><span data-ttu-id="144a4-103">Référence gérée du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="144a4-103">Extensible Storage Engine Managed Reference</span></span>

<span data-ttu-id="144a4-104">Recherchez des informations de référence pour la bibliothèque ManagedESENT.</span><span class="sxs-lookup"><span data-stu-id="144a4-104">Find reference information for the ManagedESENT library.</span></span> <span data-ttu-id="144a4-105">La bibliothèque ManagedESENT fournit un accès géré à ESENT, le moteur de base de données pouvant être incorporé natif à Windows.</span><span class="sxs-lookup"><span data-stu-id="144a4-105">The ManagedESENT library provides managed access to ESENT, the embeddable database engine that is native to Windows.</span></span>


<span data-ttu-id="144a4-106">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="144a4-106">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="144a4-107">**Dans cet article**</span><span class="sxs-lookup"><span data-stu-id="144a4-107">**In this article**</span></span>  
<span data-ttu-id="144a4-108">Comment la bibliothèque ManagedESENT est-elle différente de ESENT ?</span><span class="sxs-lookup"><span data-stu-id="144a4-108">How is the ManagedESENT library different than ESENT?</span></span>  
<span data-ttu-id="144a4-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="144a4-109">Requirements</span></span>  
<span data-ttu-id="144a4-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="144a4-110">In this section</span></span>  

## <a name="how-is-the-managedesent-library-different-than-esent"></a><span data-ttu-id="144a4-111">Comment la bibliothèque ManagedESENT est-elle différente de ESENT ?</span><span class="sxs-lookup"><span data-stu-id="144a4-111">How is the ManagedESENT library different than ESENT?</span></span>

<span data-ttu-id="144a4-112">ESENT est un moteur de base de données transactionnelle, pouvant être incorporé, qui vous permet de créer des applications personnalisées qui nécessitent un stockage de données fiable, hautes performances et à faible charge.</span><span class="sxs-lookup"><span data-stu-id="144a4-112">ESENT is an embeddable, transactional database engine that allows you to create custom applications that need reliable, high-performance, low-overhead storage of data.</span></span> <span data-ttu-id="144a4-113">Le moteur ESENT peut aider à répondre à des besoins de données qui vont d’un point aussi simple qu’une table de hachage qui est trop volumineuse pour être stockée en mémoire, plus complexe, comme une application avec des tables, des colonnes et des index.</span><span class="sxs-lookup"><span data-stu-id="144a4-113">The ESENT engine can help with data needs that range from something as simple as a hash table that is too large to store in memory, to something more complex, such as an application with tables, columns, and indexes.</span></span> <span data-ttu-id="144a4-114">Pour créer une application avec ESENT, vous utilisez la DLL esent.dll qui fait partie du système d’exploitation Windows et écrivez votre code avec C/C++.</span><span class="sxs-lookup"><span data-stu-id="144a4-114">To create an application with ESENT, you use the esent.dll DLL that is part of the Windows operating system and write your code with C/C++.</span></span> <span data-ttu-id="144a4-115">Pour plus d’informations sur ESENT, consultez informations de référence sur le [moteur de stockage extensible](./extensible-storage-engine-reference.md).</span><span class="sxs-lookup"><span data-stu-id="144a4-115">For more information about ESENT, see [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).</span></span>

<span data-ttu-id="144a4-116">ManagedESENT s’appuie sur esent.dll, qui fait partie de Windows, il n’y a donc pas de fichiers binaires non gérés supplémentaires à télécharger et à installer.</span><span class="sxs-lookup"><span data-stu-id="144a4-116">ManagedESENT is built on top of esent.dll, which is part of Windows, so there are no extra unmanaged binaries to download and install.</span></span> <span data-ttu-id="144a4-117">Avec la bibliothèque ManagedESENT, vous pouvez créer votre application à l’aide d’un langage managé tel que C \# au lieu de c/C++.</span><span class="sxs-lookup"><span data-stu-id="144a4-117">With the ManagedESENT library, you can create your application by using a managed language such as C\# instead of C/C++.</span></span> <span data-ttu-id="144a4-118">La bibliothèque utilise les mêmes noms de types et de membres pour exposer l’API ESE. par conséquent, si vous êtes déjà familiarisé avec la structure de cette API, vous pouvez facilement passer à cette bibliothèque managée.</span><span class="sxs-lookup"><span data-stu-id="144a4-118">The library uses the same type and member names to expose the ESE API, so if you are already familiar with the structure of this API, you can easily transition to this managed library.</span></span>

## <a name="requirements"></a><span data-ttu-id="144a4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="144a4-119">Requirements</span></span>

<span data-ttu-id="144a4-120">Cette bibliothèque managée requiert les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="144a4-120">This managed library requires the following:</span></span>

  - <span data-ttu-id="144a4-121">Un ordinateur exécutant une version de Windows à partir de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="144a4-121">A computer running a version of Windows starting with Windows Vista</span></span>

  - <span data-ttu-id="144a4-122">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="144a4-122">Visual Studio 2012</span></span>

  - <span data-ttu-id="144a4-123">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="144a4-123">The .NET Framework 4.5</span></span>

## <a name="in-this-section"></a><span data-ttu-id="144a4-124">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="144a4-124">In this section</span></span>

  - [<span data-ttu-id="144a4-125">Microsoft. ISAM. esent</span><span class="sxs-lookup"><span data-stu-id="144a4-125">Microsoft.Isam.Esent</span></span>](./microsoft.isam.esent-namespace.md)

  - [<span data-ttu-id="144a4-126">Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="144a4-126">Microsoft.Isam.Esent.Interop</span></span>](./microsoft.isam.esent.interop-namespace.md)

  - [<span data-ttu-id="144a4-127">Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="144a4-127">Microsoft.Isam.Esent.Interop.Server2003</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [<span data-ttu-id="144a4-128">Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="144a4-128">Microsoft.Isam.Esent.Interop.Vista</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

  - [<span data-ttu-id="144a4-129">Microsoft. ISAM. esent. Interop. une</span><span class="sxs-lookup"><span data-stu-id="144a4-129">Microsoft.Isam.Esent.Interop.Windows7</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [<span data-ttu-id="144a4-130">Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="144a4-130">Microsoft.Isam.Esent.Interop.Windows8</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
