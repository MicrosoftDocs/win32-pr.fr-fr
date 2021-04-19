---
description: 'En savoir plus sur : constructeur EsentMemoryException (String, JET_err)'
title: Constructeur EsentMemoryException (String, JET_err)
TOCTitle: EsentMemoryException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60cdb6fda03695a4afb41d82e83aaeeb9415f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533850"
---
# <a name="esentmemoryexception-constructor-string-jet_err"></a><span data-ttu-id="3dee1-103">Constructeur EsentMemoryException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="3dee1-103">EsentMemoryException constructor (String, JET_err)</span></span>

<span data-ttu-id="3dee1-104">Initialise une nouvelle instance de la classe EsentMemoryException.</span><span class="sxs-lookup"><span data-stu-id="3dee1-104">Initializes a new instance of the EsentMemoryException class.</span></span>

<span data-ttu-id="3dee1-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3dee1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3dee1-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3dee1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3dee1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dee1-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentMemoryException(description, _
    err)
```

``` csharp
protected EsentMemoryException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="3dee1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dee1-108">Parameters</span></span>

  - <span data-ttu-id="3dee1-109">description</span><span class="sxs-lookup"><span data-stu-id="3dee1-109">description</span></span>  
    <span data-ttu-id="3dee1-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3dee1-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3dee1-111">Description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="3dee1-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="3dee1-112">Raise</span><span class="sxs-lookup"><span data-stu-id="3dee1-112">err</span></span>  
    <span data-ttu-id="3dee1-113">Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3dee1-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="3dee1-114">Code d’erreur de l’exception.</span><span class="sxs-lookup"><span data-stu-id="3dee1-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="3dee1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dee1-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3dee1-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3dee1-116">Reference</span></span>

[<span data-ttu-id="3dee1-117">Classe EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="3dee1-117">EsentMemoryException class</span></span>](./esentmemoryexception-class.md)

[<span data-ttu-id="3dee1-118">Membres EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="3dee1-118">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="3dee1-119">Surcharge EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="3dee1-119">EsentMemoryException overload</span></span>](./esentmemoryexception-constructor.md)

[<span data-ttu-id="3dee1-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3dee1-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
