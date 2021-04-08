---
title: Clé de file_extension
description: Associe une extension de nom de fichier à un ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840794"
---
# <a name="file_extension-key"></a><span data-ttu-id="a2514-103">Clé de> de l’extension de fichier <\_</span><span class="sxs-lookup"><span data-stu-id="a2514-103"><file\_extension> Key</span></span>

<span data-ttu-id="a2514-104">Associe une extension de nom de fichier à un ProgID.</span><span class="sxs-lookup"><span data-stu-id="a2514-104">Associates a file name extension with a ProgID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a2514-105">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="a2514-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a><span data-ttu-id="a2514-106">Notes</span><span class="sxs-lookup"><span data-stu-id="a2514-106">Remarks</span></span>

<span data-ttu-id="a2514-107">Les informations contenues dans la clé d’extension de nom de fichier sont utilisées à la fois par l’Explorateur Windows et les monikers de fichier.</span><span class="sxs-lookup"><span data-stu-id="a2514-107">The information contained in the file name extension key is used by both the Windows Explorer and file monikers.</span></span> <span data-ttu-id="a2514-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) utilise la clé d’extension de nom de fichier pour fournir le CLSID associé.</span><span class="sxs-lookup"><span data-stu-id="a2514-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) uses the file name extension key to supply the associated CLSID.</span></span>

<span data-ttu-id="a2514-109">La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.</span><span class="sxs-lookup"><span data-stu-id="a2514-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2514-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2514-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2514-111">**FileType**</span><span class="sxs-lookup"><span data-stu-id="a2514-111">**FileType**</span></span>](filetype-key.md)
</dt> <dt>

[<span data-ttu-id="a2514-112">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="a2514-112">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




