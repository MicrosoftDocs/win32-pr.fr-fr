---
description: Un fichier est une unité de données dans le système de fichiers qu’un utilisateur peut accéder et gérer.
ms.assetid: 271bad79-c23b-45ee-938c-d17dae89db1a
title: Fichiers et clusters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75384900d5d487ab02bd19c13cc2c25e9a310b3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009945"
---
# <a name="files-and-clusters"></a>Fichiers et clusters

Un *fichier* est une unité de données dans le système de fichiers qu’un utilisateur peut accéder et gérer. Un fichier doit avoir un nom unique dans son répertoire. Il se compose d’un ou de plusieurs flux d’octets qui contiennent un ensemble de données associées, ainsi qu’un ensemble d’attributs (également appelés propriétés) qui décrivent le fichier ou les données dans le fichier. L’heure de création d’un fichier est un exemple d’attribut de fichier.

Lorsqu’un fichier est créé, un flux par défaut sans nom est créé pour stocker toutes les données écrites dans le fichier pendant qu’il est ouvert. Vous pouvez également créer des flux supplémentaires dans le fichier. Ces flux supplémentaires sont appelés flux alternatifs. L’illustration suivante représente un fichier avec le flux par défaut et deux flux de remplacement.

![fichier avec un flux par défaut et deux flux alternatifs](images/fig1.png)

Les attributs de fichier ne sont pas stockés dans les flux de données avec les données de fichier, mais ils sont stockés ailleurs et gérés par le système d’exploitation.

Toutes les données du système de fichiers, y compris le code et les répertoires d’amorçage du système, sont stockées par le système de fichiers NTFS dans les fichiers. D’autres systèmes de fichiers stockent ces informations dans des régions de disques externes au système de fichiers. l’un des avantages du stockage de ces informations dans des fichiers est que Windows peut localiser, accéder et gérer facilement les informations. D’autres avantages sont que chacun de ces fichiers peut être protégé par un descripteur de sécurité et, en cas de corruption partielle du disque, il peut être rapidement déplacé vers une partie plus sûre du disque.

L’unité de stockage fondamentale de tous les systèmes de fichiers pris en charge est un *cluster*, qui est un groupe de secteurs. Cela permet au système de fichiers d’optimiser l’administration des données de disque indépendamment de la taille de secteur de disque définie par le contrôleur de disque matériel. Si le disque à administrer est volumineux et que de grandes quantités de données sont déplacées et organisées en une seule opération, l’administrateur peut ajuster la taille du cluster pour l’adapter à ce.

Windows gère les fichiers par le biais d' [objets fichier](file-objects.md), de [descripteurs de fichiers](file-handles.md)et de [pointeurs de fichiers](file-pointers.md).

Pour plus d’informations sur les flux de fichiers, consultez [flux de fichiers](file-streams.md). Pour plus d’informations sur les clusters, consultez [clusters et étendues](clusters-and-extents.md). Pour plus d’informations sur l’accès et la gestion des fichiers [, consultez informations](file-management.md) de référence sur la gestion des fichiers et la [gestion](file-management-reference.md)des fichiers.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                       | Description                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Flux de fichiers](file-streams.md)<br/>                 | Dans le système de fichiers NTFS, les flux contiennent les données écrites dans un fichier et qui fournissent plus d’informations sur un fichier que les attributs et les propriétés.<br/>                                                                                         |
| [Objets fichier](file-objects.md)<br/>                 | Les *objets fichier* fonctionnent comme l’interface logique entre les processus du noyau et du mode utilisateur, ainsi que les données de fichier qui résident sur le disque physique.<br/>                                                                                                      |
| [Descripteurs de fichiers](file-handles.md)<br/>                 | Lorsqu’un fichier est ouvert par un processus à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , un *descripteur de fichier* lui est associé jusqu’à ce que le processus se termine ou que le handle soit fermé à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .<br/> |
| [Pointeurs de fichiers](file-pointers.md)<br/>               | Un pointeur de fichier est une valeur de décalage de 64 bits qui spécifie l’octet suivant à lire ou l’emplacement de réception de l’octet suivant écrit.<br/>                                                                                                                 |
| [Clusters et étendues](clusters-and-extents.md)<br/> | Les clusters peuvent être référencés à partir de deux perspectives différentes : dans le fichier et sur le volume.<br/>                                                                                                                                                   |



 

 

