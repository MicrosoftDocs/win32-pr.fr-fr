---
description: Le mappage de fichier peut être utilisé pour partager un fichier ou une mémoire entre deux ou plusieurs processus. Pour partager un fichier ou une mémoire, tous les processus doivent utiliser le nom ou le handle du même objet de mappage de fichier.
ms.assetid: 942cb50d-df07-444f-bba5-58194556ae66
title: Partage de fichiers et de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d402eba3f87f1f799593ae0d6b23fba06124a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094049"
---
# <a name="sharing-files-and-memory"></a>Partage de fichiers et de mémoire

Le mappage de fichier peut être utilisé pour partager un fichier ou une mémoire entre deux ou plusieurs processus. Pour partager un fichier ou une mémoire, tous les processus doivent utiliser le nom ou le handle du même objet de mappage de fichier.

Pour partager un fichier, le premier processus crée ou ouvre un fichier à l’aide de la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) . Ensuite, il crée un objet de mappage de fichier à l’aide de la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) , en spécifiant le descripteur de fichier et un nom pour l’objet de mappage de fichier. Les noms des objets Event, Semaphore, mutex, Timer Timer, Job et file Mapping partagent le même espace de noms. Par conséquent, les fonctions **CreateFileMapping** et [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) échouent si elles spécifient un nom qui est utilisé par un objet d’un autre type.

Pour partager la mémoire qui n’est pas associée à un fichier, un processus doit utiliser la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) et spécifier une valeur de handle non valide \_ \_ en tant que paramètre *hFile* au lieu d’un descripteur de fichier existant. L’objet de mappage de fichier correspondant accède à la mémoire sauvegardée par le fichier de pagination système. Vous devez spécifier une taille supérieure à zéro quand vous spécifiez un *hFile* de \_ valeur de handle non valide \_ dans un appel à **CreateFileMapping**.

Le moyen le plus simple pour d’autres processus d’obtenir un handle de l’objet de mappage de fichier créé par le premier processus consiste à utiliser la fonction [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) et à spécifier le nom de l’objet. C’est ce que l’on appelle la « *mémoire partagée*». Si l’objet de mappage de fichier n’a pas de nom, le processus doit obtenir un descripteur à l’aide de l’héritage ou de la duplication. Pour plus d’informations sur l’héritage et la duplication, consultez [héritage](../procthread/inheritance.md).

Les processus qui partagent des fichiers ou de la mémoire doivent créer des vues de fichier à l’aide de la fonction [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) ou [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) . Ils doivent coordonner leur accès à l’aide de sémaphores, de mutex, d’événements ou d’une autre technique d’exclusion mutuelle. Pour plus d’informations, consultez [Synchronization](../sync/synchronization.md).

Un objet de mappage de fichier partagé n’est pas détruit jusqu’à ce que tous les processus qui l’utilisent ferment leurs Handles à l’aide de la fonction [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

Pour plus d’informations sur la sécurité de l’objet de mappage de fichiers, consultez [sécurité du mappage de fichiers et droits d’accès](file-mapping-security-and-access-rights.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une mémoire partagée nommée](creating-named-shared-memory.md)
</dt> </dl>

 

 
