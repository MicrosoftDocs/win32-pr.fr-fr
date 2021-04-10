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
# <a name="managing-local-partitions"></a>Gestion des partitions locales

En guise d’alternative à la création et à la configuration de partitions locales par le biais de l’outil d’administration Services de composants, vous pouvez gérer les partitions par programme en utilisant des collections et des propriétés d’administration COM+ spécifiques à la partition.

> [!Note]  
> Le service partitions COM+ n’est pas activé par défaut. Pour utiliser le service partitions COM+, vous devez l’activer par le biais de l’outil d’administration Services de composants ou en modifiant la propriété PartitionsEnabled de la collection [**LocalComputer**](localcomputer.md) sur true.

 

La sous-routine suivante écrite dans Visual Basic Script montre comment créer une partition sur l’ordinateur local :


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



La sous-routine suivante écrite dans Visual Basic Script montre comment supprimer une partition de l’ordinateur local :


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



La sous-routine suivante écrite dans Visual Basic Script montre comment définir la partition par défaut d’un utilisateur :


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



La sous-routine suivante écrite dans Visual Basic Script montre comment supprimer la partition par défaut pour un utilisateur :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Collecte des métriques de partition](collecting-partition-metrics.md)
</dt> <dt>

[Configuration du cache de partition](configuring-the-partition-cache.md)
</dt> <dt>

[Regroupement d’applications en partitions](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestion des partitions dans Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Définition des droits d’administration pour une partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



