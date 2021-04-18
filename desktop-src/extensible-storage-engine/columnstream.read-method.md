---
description: 'En savoir plus sur : méthode ColumnStream. Read'
title: ColumnStream. Read, méthode
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536412"
---
# <a name="columnstreamread-method"></a><span data-ttu-id="4758a-103">ColumnStream. Read, méthode</span><span class="sxs-lookup"><span data-stu-id="4758a-103">ColumnStream.Read method</span></span>

<span data-ttu-id="4758a-104">Lit une séquence d'octets dans le flux actuel et avance la position dans le flux du nombre d'octets lus.</span><span class="sxs-lookup"><span data-stu-id="4758a-104">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span>

<span data-ttu-id="4758a-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4758a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4758a-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4758a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4758a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4758a-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="4758a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4758a-108">Parameters</span></span>

  - <span data-ttu-id="4758a-109">buffer</span><span class="sxs-lookup"><span data-stu-id="4758a-109">buffer</span></span>  
    <span data-ttu-id="4758a-110">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="4758a-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="4758a-111">Mémoire tampon à lire.</span><span class="sxs-lookup"><span data-stu-id="4758a-111">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="4758a-112">offset</span><span class="sxs-lookup"><span data-stu-id="4758a-112">offset</span></span>  
    <span data-ttu-id="4758a-113">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4758a-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4758a-114">Offset dans la mémoire tampon à lire.</span><span class="sxs-lookup"><span data-stu-id="4758a-114">The offset in the buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="4758a-115">count</span><span class="sxs-lookup"><span data-stu-id="4758a-115">count</span></span>  
    <span data-ttu-id="4758a-116">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4758a-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4758a-117">Nombre d'octets à lire.</span><span class="sxs-lookup"><span data-stu-id="4758a-117">The number of bytes to read.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4758a-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4758a-118">Return value</span></span>

<span data-ttu-id="4758a-119">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4758a-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="4758a-120">Nombre d’octets lus dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4758a-120">The number of bytes read into the buffer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4758a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4758a-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4758a-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4758a-122">Reference</span></span>

[<span data-ttu-id="4758a-123">ColumnStream, classe</span><span class="sxs-lookup"><span data-stu-id="4758a-123">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="4758a-124">Membres ColumnStream</span><span class="sxs-lookup"><span data-stu-id="4758a-124">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="4758a-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4758a-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
