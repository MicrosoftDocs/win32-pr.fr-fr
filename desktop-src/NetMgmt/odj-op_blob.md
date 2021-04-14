---
title: OP_BLOB
description: Définition du OP_BLOB IDL
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383176"
---
# <a name="op_blob-structure"></a><span data-ttu-id="49e2b-103">Structure OP_BLOB</span><span class="sxs-lookup"><span data-stu-id="49e2b-103">OP_BLOB structure</span></span>

<span data-ttu-id="49e2b-104">Contient une mémoire tampon d’octets opaque.</span><span class="sxs-lookup"><span data-stu-id="49e2b-104">Contains an opaque byte buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49e2b-105">Syntax</span></span>

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a><span data-ttu-id="49e2b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="49e2b-106">Members</span></span>

### <a name="cbblob"></a><span data-ttu-id="49e2b-107">cbBlob</span><span class="sxs-lookup"><span data-stu-id="49e2b-107">cbBlob</span></span>

<span data-ttu-id="49e2b-108">Spécifie la taille de pBlob en octets.</span><span class="sxs-lookup"><span data-stu-id="49e2b-108">Specifies the the size of pBlob in bytes.</span></span>

### <a name="pblob"></a><span data-ttu-id="49e2b-109">pBlob</span><span class="sxs-lookup"><span data-stu-id="49e2b-109">pBlob</span></span>

<span data-ttu-id="49e2b-110">Pointe vers une mémoire tampon d’octets.</span><span class="sxs-lookup"><span data-stu-id="49e2b-110">Points to a byte buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="49e2b-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49e2b-111">See also</span></span>

[<span data-ttu-id="49e2b-112">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="49e2b-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
