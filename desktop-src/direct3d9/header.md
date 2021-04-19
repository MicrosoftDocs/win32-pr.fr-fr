---
description: Les définitions suivantes doivent être utilisées lors de la lecture et de l’écriture directes de l’en-tête binaire.
ms.assetid: 19c36f94-8088-417d-867d-3a02912087dc
title: En-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfaa589382812cfd752d47cc8b95cda0139385b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515308"
---
# <a name="header"></a><span data-ttu-id="a6c39-103">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6c39-103">Header</span></span>

<span data-ttu-id="a6c39-104">Les définitions suivantes doivent être utilisées lors de la lecture et de l’écriture directes de l’en-tête binaire.</span><span class="sxs-lookup"><span data-stu-id="a6c39-104">The following definitions should be used when directly reading and writing the binary header.</span></span>

> [!Note]  
> <span data-ttu-id="a6c39-105">Les flux de données compressés ne sont actuellement pas pris en charge et ne sont donc pas détaillés ici.</span><span class="sxs-lookup"><span data-stu-id="a6c39-105">Compressed data streams are not currently supported and are therefore not detailed here.</span></span>

 


```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```



## <a name="related-topics"></a><span data-ttu-id="a6c39-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6c39-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6c39-107">Encodage Binaire</span><span class="sxs-lookup"><span data-stu-id="a6c39-107">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



