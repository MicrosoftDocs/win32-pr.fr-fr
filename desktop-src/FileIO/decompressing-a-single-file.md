---
description: Une application peut décompresser un fichier compressé unique à l’aide des fonctions LZOpenFile, LZCopy et LZClose.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Décompression d’un fichier unique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8da6ee4ee80e42d6ff70c3d9c50efdc572f97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516991"
---
# <a name="decompressing-a-single-file"></a>Décompression d’un fichier unique

Une application peut décompresser un fichier compressé unique en effectuant les tâches suivantes :

1.  Ouvrez le fichier source en appelant la fonction [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .
2.  Ouvrez le fichier de destination en appelant [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copiez le fichier source dans le fichier de destination en appelant la fonction [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) et en passant les handles retournés par [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
4.  Fermez les fichiers en appelant la fonction [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .

 

 



