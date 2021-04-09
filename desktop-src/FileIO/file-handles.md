---
description: Lorsqu’un fichier est ouvert par un processus à l’aide de la fonction CreateFile, un descripteur de fichier lui est associé jusqu’à ce que le processus se termine ou que le handle soit fermé à l’aide de la fonction CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Descripteurs de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868245"
---
# <a name="file-handles"></a>Descripteurs de fichiers

Lorsqu’un fichier est ouvert par un processus à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , un *descripteur de fichier* lui est associé jusqu’à ce que le processus se termine ou que le handle soit fermé à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Le descripteur de fichier est utilisé pour identifier le fichier dans de nombreux appels de fonction.

Chaque descripteur de fichier et objet de fichier est généralement unique à chaque processus qui ouvre un fichier ; les seules exceptions sont lorsqu’un descripteur de fichier détenu par un processus est dupliqué, ou lorsqu’un processus enfant hérite des handles de fichiers du processus parent. Dans ces situations, ces descripteurs de fichiers sont uniques, mais ils voient un seul objet de fichier partagé. Consultez [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) pour plus d’informations sur la duplication des descripteurs de fichiers détenus par les processus.

Notez que, si les descripteurs de fichiers sont généralement privés pour un processus, les données de fichier sur lesquelles pointe le point de fichier ne sont pas. Par conséquent, les processus et les threads qui partagent le même fichier doivent synchroniser leur accès. Pour la plupart des opérations sur un fichier, un processus identifie le fichier par le biais de son pool privé de handles.

 

 
