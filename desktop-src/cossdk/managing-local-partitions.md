---
description: En guise d’alternative à la création et à la configuration de partitions locales par le biais de l’outil d’administration Services de composants, vous pouvez gérer les partitions par programme en utilisant des collections et des propriétés d’administration COM+ spécifiques à la partition.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Gestion des partitions locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd551fc73c76067c4ab2e988fba79ee702df53c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950815"
---
# <a name="managing-local-partitions"></a><span data-ttu-id="2ed6a-103">Gestion des partitions locales</span><span class="sxs-lookup"><span data-stu-id="2ed6a-103">Managing Local Partitions</span></span>

<span data-ttu-id="2ed6a-104">En guise d’alternative à la création et à la configuration de partitions locales par le biais de l’outil d’administration Services de composants, vous pouvez gérer les partitions par programme en utilisant des collections et des propriétés d’administration COM+ spécifiques à la partition.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-104">As an alternative to creating and configuring local partitions through the Component Services administrative tool, you can manage partitions programmatically by using partition-specific COM+ administration collections and properties.</span></span>

> [!Note]  
> <span data-ttu-id="2ed6a-105">Le service partitions COM+ n’est pas activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-105">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="2ed6a-106">Pour utiliser le service partitions COM+, vous devez l’activer par le biais de l’outil d’administration Services de composants ou en modifiant la propriété PartitionsEnabled de la collection [**LocalComputer**](localcomputer.md) sur true.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-106">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="2ed6a-107">La sous-routine suivante écrite dans Visual Basic Script montre comment créer une partition sur l’ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="2ed6a-107">The following subroutine written in Visual Basic script demonstrates how to create a partition on the local computer:</span></span>


```VB
Sub CreatePartition (PartitonGuid, PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   Set part = collPartitions.Add
   ' If you don't specify a partition GUID, one is created for you.
   ' Otherwise, you can specify one this way:
   part.Value("ID") = PartitonGuid
   part.Value("Name") = PartitionName
   collPartitions.SaveChanges
   Set part = Nothing
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub 
```



<span data-ttu-id="2ed6a-108">La sous-routine suivante écrite dans Visual Basic Script montre comment supprimer une partition de l’ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="2ed6a-108">The following subroutine written in Visual Basic script demonstrates how to delete a partition from the local computer:</span></span>


```VB
Sub DeletePartition (PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   numPartitions = collPartitions.Count
   ' Begin with the last partition, and work forward through the list.
   For i = numPartitions - 1 To 0 Step -1 
       If collPartitions.Item(i).Value("Name") = PartitionName Then
           collPartitions.Remove i
       End If
   Next
   collPartitions.SaveChanges
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="2ed6a-109">La sous-routine suivante écrite dans Visual Basic Script montre comment définir la partition par défaut d’un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="2ed6a-109">The following subroutine written in Visual Basic script demonstrates how to set the default partition for a user:</span></span>


```VB
Sub SetDefaultPartitionForUser(UserName, PartitionGuid)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   Set user = collUsers.Add
   user.Value("AccountName") = UserName
   user.Value("DefaultPartitionID") = PartitionGuid
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



<span data-ttu-id="2ed6a-110">La sous-routine suivante écrite dans Visual Basic Script montre comment supprimer la partition par défaut pour un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="2ed6a-110">The following subroutine written in Visual Basic script demonstrates how to remove the default partition for a user:</span></span>


```VB
Sub RemoveDefaultPartitionForUser(UserName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   numUsers = collUsers.Count
   ' Begin with the last user, and work forward through the list.
   For i = numUsers - 1 To 0 Step -1
       If collUsers.Item(i).Value("AccountName") = UserName Then
           collUsers.Remove i
       End If
   Next
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="2ed6a-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ed6a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed6a-112">Collecte des métriques de partition</span><span class="sxs-lookup"><span data-stu-id="2ed6a-112">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="2ed6a-113">Configuration du cache de partition</span><span class="sxs-lookup"><span data-stu-id="2ed6a-113">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="2ed6a-114">Regroupement d’applications en partitions</span><span class="sxs-lookup"><span data-stu-id="2ed6a-114">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="2ed6a-115">Gestion des partitions dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="2ed6a-115">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="2ed6a-116">Définition des droits d’administration pour une partition</span><span class="sxs-lookup"><span data-stu-id="2ed6a-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



