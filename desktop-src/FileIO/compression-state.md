---
description: Chaque fichier et répertoire sur un volume qui prend en charge la compression de fichiers et de répertoires individuels a un état de compression.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: État de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19abfe0deecb951c00dacb00c64dd8dcf7af56d37fe9112095cdce403619f843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582419"
---
# <a name="compression-state"></a>État de compression

Chaque fichier et répertoire sur un volume qui prend en charge la compression de fichiers et de répertoires individuels a un *État de compression*.

Tandis que l’attribut de compression d’un fichier ou d’un répertoire indique simplement si le fichier ou le répertoire est compressé ou non compressé, l’état de compression spécifie également le format des données compressées.

Utilisez le code de contrôle [**FSCTL \_ obtenir la \_ compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) pour déterminer l’état de compression d’un fichier ou d’un répertoire.

L’état de compression est encodé sous la forme d’une valeur de 16 bits. Une valeur d’état de compression du format de COMPRESSION \_ \_ aucun indique qu’un fichier n’est pas compressé. \_La valeur par défaut du format de compression \_ indique qu’un fichier est compressé, en utilisant le format de compression par défaut. Toute autre valeur indique qu’un fichier est compressé, en utilisant le format de compression spécifié par la valeur d’état de compression.

Utilisez le code de contrôle de [**\_ \_ compression Set FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) pour définir l’état de compression d’un fichier ou d’un répertoire. Cette opération définit également l’attribut de compression du fichier ou du répertoire.

La définition de l’état de compression d’un fichier sur une valeur différente de zéro compresse le fichier, en utilisant le format de compression encodé à l’aide de la valeur d’état de compression. La définition de l’état de compression d’un fichier sur zéro décompresse le fichier. Il s’agit d’opérations synchrones. Le fichier est compressé ou décompressé immédiatement lorsque vous définissez son état de compression.

La définition de l’état de compression d’un répertoire n’entraîne pas de compression ou de décompression immédiate. Au lieu de cela, la définition de l’état de compression d’un répertoire définit un état de compression par défaut qui sera attribué à tous les fichiers et sous-répertoires nouvellement créés.

 

 
