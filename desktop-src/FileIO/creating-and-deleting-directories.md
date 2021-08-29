---
description: Une application peut créer et supprimer par programmation des répertoires.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Création et suppression de répertoires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862907ad3adef3a4502961820a6f5ffcb1cd932541b03226854d81372ca6e13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533735"
---
# <a name="creating-and-deleting-directories"></a>Création et suppression de répertoires

Une application peut créer et supprimer par programmation des répertoires.

Pour créer un répertoire, utilisez la fonction [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)ou [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) . Un répertoire reçoit le nom spécifié lors de sa création. Les conventions pour nommer un répertoire obéissent aux conventions pour nommer un fichier. Pour obtenir une description de ces conventions, consultez [attribution d’un nom à un fichier](naming-a-file.md).

Pour supprimer un répertoire existant, utilisez la fonction [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) ou [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) . Avant de supprimer un répertoire, vous devez vous assurer que le répertoire est vide et que vous disposez du privilège supprimer l’accès pour le répertoire. Pour ce faire, appelez la fonction [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .

 

 
