---
description: 'En savoir plus sur : constructeur EsentIOException (String, JET_err)'
title: Constructeur EsentIOException (String, JET_err)
TOCTitle: EsentIOException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentIOException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102030
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087f22d7836ff41ac97b65c15be1b51dfac84a8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518281"
---
# <a name="esentioexception-constructor-string-jet_err"></a><span data-ttu-id="3020d-103">Constructeur EsentIOException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="3020d-103">EsentIOException constructor (String, JET_err)</span></span>

<span data-ttu-id="3020d-104">Initialise une nouvelle instance de la classe EsentIOException.</span><span class="sxs-lookup"><span data-stu-id="3020d-104">Initializes a new instance of the EsentIOException class.</span></span>

<span data-ttu-id="3020d-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3020d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3020d-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3020d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3020d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3020d-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentIOException(description, _
    err)
```

``` csharp
protected EsentIOException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="3020d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3020d-108">Parameters</span></span>

  - <span data-ttu-id="3020d-109">description</span><span class="sxs-lookup"><span data-stu-id="3020d-109">description</span></span>  
    <span data-ttu-id="3020d-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3020d-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3020d-111">Description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="3020d-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="3020d-112">Raise</span><span class="sxs-lookup"><span data-stu-id="3020d-112">err</span></span>  
    <span data-ttu-id="3020d-113">Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3020d-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="3020d-114">Code d’erreur de l’exception.</span><span class="sxs-lookup"><span data-stu-id="3020d-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="3020d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3020d-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3020d-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3020d-116">Reference</span></span>

[<span data-ttu-id="3020d-117">Classe EsentIOException</span><span class="sxs-lookup"><span data-stu-id="3020d-117">EsentIOException class</span></span>](./esentioexception-class.md)

[<span data-ttu-id="3020d-118">Membres EsentIOException</span><span class="sxs-lookup"><span data-stu-id="3020d-118">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="3020d-119">Surcharge EsentIOException</span><span class="sxs-lookup"><span data-stu-id="3020d-119">EsentIOException overload</span></span>](./esentioexception-constructor.md)

[<span data-ttu-id="3020d-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3020d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
