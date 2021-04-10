---
description: Une application peut créer et supprimer par programmation des répertoires.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Création et suppression de répertoires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114338"
---
# <a name="creating-and-deleting-directories"></a>Création et suppression de répertoires

Une application peut créer et supprimer par programmation des répertoires.

Pour créer un répertoire, utilisez la fonction [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)ou [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) . Un répertoire reçoit le nom spécifié lors de sa création. Les conventions pour nommer un répertoire obéissent aux conventions pour nommer un fichier. Pour obtenir une description de ces conventions, consultez [attribution d’un nom à un fichier](naming-a-file.md).

Pour supprimer un répertoire existant, utilisez la fonction [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) ou [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) . Avant de supprimer un répertoire, vous devez vous assurer que le répertoire est vide et que vous disposez du privilège supprimer l’accès pour le répertoire. Pour ce faire, appelez la fonction [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .

 

 
