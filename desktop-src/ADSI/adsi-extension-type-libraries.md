---
title: Bibliothèques de types d’extension ADSI
description: Les bibliothèques de types pour les extensions ne sont pas fusionnées.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- Bibliothèques de types d’extension ADSI ADSI
- ADSI d’extensions, bibliothèques de types d’extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507042"
---
# <a name="adsi-extension-type-libraries"></a><span data-ttu-id="4447b-105">Bibliothèques de types d’extension ADSI</span><span class="sxs-lookup"><span data-stu-id="4447b-105">ADSI Extension Type Libraries</span></span>

<span data-ttu-id="4447b-106">Les bibliothèques de types pour les extensions ne sont pas fusionnées.</span><span class="sxs-lookup"><span data-stu-id="4447b-106">The type libraries for extensions are not merged.</span></span> <span data-ttu-id="4447b-107">Les clients ADSI doivent inclure spécifiquement la bibliothèque de types pour chaque extension.</span><span class="sxs-lookup"><span data-stu-id="4447b-107">ADSI clients must specifically include the type library for each extension.</span></span> <span data-ttu-id="4447b-108">La bibliothèque de types est requise pour Visual Basic pour activer les liaisons antérieures.</span><span class="sxs-lookup"><span data-stu-id="4447b-108">The type library is required for Visual Basic to enable early bindings.</span></span> <span data-ttu-id="4447b-109">Les applications clientes écrites en C/C++ peuvent appeler la méthode **QueryInterface** sur les interfaces d’extension définies dans les fichiers d’en-tête d’extension.</span><span class="sxs-lookup"><span data-stu-id="4447b-109">Client applications written in C/C++ can call the **QueryInterface** method on the extension interfaces defined in the extension header files.</span></span>

 

 




