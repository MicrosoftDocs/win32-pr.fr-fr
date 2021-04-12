---
description: 'En savoir plus sur : constructeur EsentFatalException (String, JET_err)'
title: Constructeur EsentFatalException (String, JET_err)
TOCTitle: EsentFatalException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101610
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f025b93e626c4b0f2ab6bb7729169aaff1d67707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202987"
---
# <a name="esentfatalexception-constructor-string-jet_err"></a><span data-ttu-id="6c637-103">Constructeur EsentFatalException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="6c637-103">EsentFatalException constructor (String, JET_err)</span></span>

<span data-ttu-id="6c637-104">Initialise une nouvelle instance de la classe EsentFatalException.</span><span class="sxs-lookup"><span data-stu-id="6c637-104">Initializes a new instance of the EsentFatalException class.</span></span>

<span data-ttu-id="6c637-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c637-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c637-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c637-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c637-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c637-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentFatalException(description, _
    err)
```

``` csharp
protected EsentFatalException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="6c637-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c637-108">Parameters</span></span>

  - <span data-ttu-id="6c637-109">description</span><span class="sxs-lookup"><span data-stu-id="6c637-109">description</span></span>  
    <span data-ttu-id="6c637-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6c637-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6c637-111">Description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="6c637-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c637-112">Raise</span><span class="sxs-lookup"><span data-stu-id="6c637-112">err</span></span>  
    <span data-ttu-id="6c637-113">Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6c637-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="6c637-114">Code d’erreur de l’exception.</span><span class="sxs-lookup"><span data-stu-id="6c637-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c637-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c637-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c637-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6c637-116">Reference</span></span>

[<span data-ttu-id="6c637-117">EsentFatalException, classe</span><span class="sxs-lookup"><span data-stu-id="6c637-117">EsentFatalException class</span></span>](./esentfatalexception-class.md)

[<span data-ttu-id="6c637-118">Membres EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="6c637-118">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="6c637-119">Surcharge EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="6c637-119">EsentFatalException overload</span></span>](./esentfatalexception-constructor.md)

[<span data-ttu-id="6c637-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6c637-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
