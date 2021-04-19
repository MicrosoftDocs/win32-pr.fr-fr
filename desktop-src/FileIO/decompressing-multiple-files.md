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
# <a name="decompressing-multiple-files"></a><span data-ttu-id="77dc7-103">Décompression de plusieurs fichiers</span><span class="sxs-lookup"><span data-stu-id="77dc7-103">Decompressing Multiple Files</span></span>

<span data-ttu-id="77dc7-104">Une application peut décompresser plusieurs fichiers en effectuant les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="77dc7-104">An application can decompress multiple files by performing the following tasks:</span></span>

1.  <span data-ttu-id="77dc7-105">Ouvrez les fichiers sources en appelant la fonction [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="77dc7-105">Open the source files by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="77dc7-106">Ouvrez les fichiers de destination en appelant [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="77dc7-106">Open the destination files by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="77dc7-107">Copiez les fichiers sources dans les fichiers de destination en appelant la fonction [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .</span><span class="sxs-lookup"><span data-stu-id="77dc7-107">Copy the source files to the destination files by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function.</span></span>
4.  <span data-ttu-id="77dc7-108">Fermez les fichiers en appelant la fonction [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="77dc7-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



