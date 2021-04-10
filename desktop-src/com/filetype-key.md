---
title: Clé FileType
description: Utilisé par GetClassFile pour faire correspondre des modèles à différents octets de fichier dans un fichier non composé.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Clé de Registre FileType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029776"
---
# <a name="filetype-key"></a><span data-ttu-id="d69fb-104">Clé FileType</span><span class="sxs-lookup"><span data-stu-id="d69fb-104">FileType Key</span></span>

<span data-ttu-id="d69fb-105">Utilisé par [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) pour faire correspondre des modèles à différents octets de fichier dans un fichier non composé.</span><span class="sxs-lookup"><span data-stu-id="d69fb-105">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d69fb-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="d69fb-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span data-ttu-id="d69fb-107"><span id="offset"></span><span id="OFFSET"></span>*décalage*</span><span class="sxs-lookup"><span data-stu-id="d69fb-107"><span id="offset"></span><span id="OFFSET"></span>*offset*</span></span>
</dt> <dd>

<span data-ttu-id="d69fb-108">Détermine la distance à partir du début ou de la fin du fichier pour commencer la comparaison.</span><span class="sxs-lookup"><span data-stu-id="d69fb-108">Determines how far from the beginning or end of the file to begin the comparison.</span></span> <span data-ttu-id="d69fb-109">Si le décalage est une valeur négative, la comparaison commence à la fin du fichier moins la valeur de décalage.</span><span class="sxs-lookup"><span data-stu-id="d69fb-109">If the offset is a negative value, the comparison begins from the end of the file minus the offset value.</span></span> <span data-ttu-id="d69fb-110">La valeur de décalage est un type décimal, sauf si elle est précédée de « 0x ».</span><span class="sxs-lookup"><span data-stu-id="d69fb-110">The offset value is a decimal type unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="d69fb-111"><span id="cb"></span><span id="CB"></span>*libéré*</span><span class="sxs-lookup"><span data-stu-id="d69fb-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="d69fb-112">Représente la longueur en octets entre le début et la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="d69fb-112">Represents the length in bytes from the beginning to the end of the file.</span></span> <span data-ttu-id="d69fb-113">Représente la plage d’octets dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="d69fb-113">Represents the byte range in the file.</span></span> <span data-ttu-id="d69fb-114">La valeur *CB* est une valeur décimale, sauf si elle est précédée de « 0x ».</span><span class="sxs-lookup"><span data-stu-id="d69fb-114">The *cb* value is a decimal unless preceded by "0x".</span></span>

</dd> <dt>

<span data-ttu-id="d69fb-115"><span id="mask"></span><span id="MASK"></span>*filtrage*</span><span class="sxs-lookup"><span data-stu-id="d69fb-115"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="d69fb-116">Valeur binaire utilisée pour le masquage, qui est effectuée à l’aide d’une opération AND logique, et la plage d’octets spécifiée par *offset* et *CB*.</span><span class="sxs-lookup"><span data-stu-id="d69fb-116">A binary value used for masking, which is performed by using a logical AND operation, and the byte range specified by *offset* and *cb*.</span></span> <span data-ttu-id="d69fb-117">Si cette valeur est omise, les octets sont définis sur tous.</span><span class="sxs-lookup"><span data-stu-id="d69fb-117">If this value is omitted, the bytes are set to all ones.</span></span> <span data-ttu-id="d69fb-118">Cette valeur est toujours hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="d69fb-118">This value is always hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="d69fb-119"><span id="value"></span><span id="VALUE"></span>*ajoutée*</span><span class="sxs-lookup"><span data-stu-id="d69fb-119"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="d69fb-120">Représente le modèle qui doit correspondre pour qu’un fichier soit de ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="d69fb-120">Represents the pattern that must match for a file to be of this file type.</span></span> <span data-ttu-id="d69fb-121">Le modèle est utilisé pour identifier correctement un format de fichier connu à partir de son contenu, et non par son extension.</span><span class="sxs-lookup"><span data-stu-id="d69fb-121">The pattern is used to properly identify a known file format from its contents, not by its extension.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d69fb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="d69fb-122">Remarks</span></span>

<span data-ttu-id="d69fb-123">Les entrées sont utilisées par la fonction [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) pour faire correspondre des modèles à différents octets de fichier dans un fichier non composé.</span><span class="sxs-lookup"><span data-stu-id="d69fb-123">Entries are used by the [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) function to match patterns against various file bytes in a non-compound file.</span></span> <span data-ttu-id="d69fb-124">**Filetype** contient des sous-clés CLSID, chacune ayant une série de sous-clés **0**, **1**, **2**, **3**.</span><span class="sxs-lookup"><span data-stu-id="d69fb-124">**FileType** has CLSID subkeys, each of which has a series of subkeys **0**, **1**, **2**, **3**.</span></span> <span data-ttu-id="d69fb-125">Ces valeurs contiennent des modèles qui, si une correspondance est trouvée, génèrent le CLSID indiqué.</span><span class="sxs-lookup"><span data-stu-id="d69fb-125">These values contain patterns that, if one matches, yield the indicated CLSID.</span></span> <span data-ttu-id="d69fb-126">Par exemple, la valeur « 0, 4, FFFFFFFF, ABCD1234 » indique que les 4 premiers octets doivent être ABCD1234, dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="d69fb-126">For example, a value of "0, 4, FFFFFFFF, ABCD1234" indicates that the first 4 bytes must be ABCD1234, in that order.</span></span> <span data-ttu-id="d69fb-127">La valeur « -4, 4, FEFEFEFE » indique que les quatre derniers octets du fichier doivent être FEFEFEFE.</span><span class="sxs-lookup"><span data-stu-id="d69fb-127">A value of "-4, 4, FEFEFEFE " indicates that the last four bytes in the file must be FEFEFEFE.</span></span> <span data-ttu-id="d69fb-128">Si l’un des modèles correspond, le CLSID est retourné.</span><span class="sxs-lookup"><span data-stu-id="d69fb-128">If either pattern matches, the CLSID is returned.</span></span>

<span data-ttu-id="d69fb-129">La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.</span><span class="sxs-lookup"><span data-stu-id="d69fb-129">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d69fb-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d69fb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d69fb-131">**Extension de fichier<\_>**</span><span class="sxs-lookup"><span data-stu-id="d69fb-131">**<file\_extension>**</span></span>](-file-extension--key.md)
</dt> <dt>

[<span data-ttu-id="d69fb-132">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="d69fb-132">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




