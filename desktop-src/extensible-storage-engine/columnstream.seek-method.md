---
description: 'En savoir plus sur : méthode ColumnStream. Seek'
title: ColumnStream. Seek, méthode
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527561"
---
# <a name="columnstreamseek-method"></a><span data-ttu-id="10ba9-103">ColumnStream. Seek, méthode</span><span class="sxs-lookup"><span data-stu-id="10ba9-103">ColumnStream.Seek method</span></span>

<span data-ttu-id="10ba9-104">Définit la position dans le flux actuel.</span><span class="sxs-lookup"><span data-stu-id="10ba9-104">Sets the position in the current stream.</span></span>

<span data-ttu-id="10ba9-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10ba9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10ba9-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="10ba9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10ba9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10ba9-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a><span data-ttu-id="10ba9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10ba9-108">Parameters</span></span>

  - <span data-ttu-id="10ba9-109">offset</span><span class="sxs-lookup"><span data-stu-id="10ba9-109">offset</span></span>  
    <span data-ttu-id="10ba9-110">Type : [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="10ba9-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="10ba9-111">Décalage d’octet par rapport au paramètre Origin.</span><span class="sxs-lookup"><span data-stu-id="10ba9-111">Byte offset relative to the origin parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="10ba9-112">origin</span><span class="sxs-lookup"><span data-stu-id="10ba9-112">origin</span></span>  
    <span data-ttu-id="10ba9-113">Type : [System. IO. SeekOrigin](/dotnet/api/system.io.seekorigin)</span><span class="sxs-lookup"><span data-stu-id="10ba9-113">Type: [System.IO.SeekOrigin](/dotnet/api/system.io.seekorigin)</span></span>  
    
    <span data-ttu-id="10ba9-114">SeekOrigin indiquant le point de référence pour la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="10ba9-114">A SeekOrigin indicating the reference point for the new position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="10ba9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10ba9-115">Return value</span></span>

<span data-ttu-id="10ba9-116">Type : [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="10ba9-116">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
<span data-ttu-id="10ba9-117">Nouvelle position dans le flux actuel.</span><span class="sxs-lookup"><span data-stu-id="10ba9-117">The new position in the current stream.</span></span>  

## <a name="see-also"></a><span data-ttu-id="10ba9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10ba9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10ba9-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="10ba9-119">Reference</span></span>

[<span data-ttu-id="10ba9-120">ColumnStream, classe</span><span class="sxs-lookup"><span data-stu-id="10ba9-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="10ba9-121">Membres ColumnStream</span><span class="sxs-lookup"><span data-stu-id="10ba9-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="10ba9-122">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="10ba9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
