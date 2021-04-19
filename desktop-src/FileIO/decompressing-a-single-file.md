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
# <a name="decompressing-a-single-file"></a><span data-ttu-id="a7b88-103">Décompression d’un fichier unique</span><span class="sxs-lookup"><span data-stu-id="a7b88-103">Decompressing a Single File</span></span>

<span data-ttu-id="a7b88-104">Une application peut décompresser un fichier compressé unique en effectuant les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="a7b88-104">An application can decompress a single compressed file by performing the following tasks:</span></span>

1.  <span data-ttu-id="a7b88-105">Ouvrez le fichier source en appelant la fonction [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="a7b88-105">Open the source file by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="a7b88-106">Ouvrez le fichier de destination en appelant [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="a7b88-106">Open the destination file by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="a7b88-107">Copiez le fichier source dans le fichier de destination en appelant la fonction [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) et en passant les handles retournés par [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="a7b88-107">Copy the source file to the destination file by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function and passing the handles returned by [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
4.  <span data-ttu-id="a7b88-108">Fermez les fichiers en appelant la fonction [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="a7b88-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



