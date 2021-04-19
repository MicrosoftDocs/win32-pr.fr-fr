---
description: Une application peut décompresser plusieurs fichiers à l’aide des fonctions LZOpenFile, LZCopy et LZClose.
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: Décompression de plusieurs fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524572"
---
# <a name="decompressing-multiple-files"></a>Décompression de plusieurs fichiers

Une application peut décompresser plusieurs fichiers en effectuant les tâches suivantes :

1.  Ouvrez les fichiers sources en appelant la fonction [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .
2.  Ouvrez les fichiers de destination en appelant [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copiez les fichiers sources dans les fichiers de destination en appelant la fonction [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .
4.  Fermez les fichiers en appelant la fonction [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .

 

 



