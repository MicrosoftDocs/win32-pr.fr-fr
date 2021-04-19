---
description: 'En savoir plus sur : constructeur EsentOperationException (String, JET_err)'
title: Constructeur EsentOperationException (String, JET_err)
TOCTitle: EsentOperationException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentOperationException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102376
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb25ea404e4581b369f9d81e772ba4b2e95f7fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527429"
---
# <a name="esentoperationexception-constructor-string-jet_err"></a><span data-ttu-id="4a691-103">Constructeur EsentOperationException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="4a691-103">EsentOperationException constructor (String, JET_err)</span></span>

<span data-ttu-id="4a691-104">Initialise une nouvelle instance de la classe EsentOperationException.</span><span class="sxs-lookup"><span data-stu-id="4a691-104">Initializes a new instance of the EsentOperationException class.</span></span>

<span data-ttu-id="4a691-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a691-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4a691-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4a691-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a691-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a691-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentOperationException(description, _
    err)
```

``` csharp
protected EsentOperationException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="4a691-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a691-108">Parameters</span></span>

  - <span data-ttu-id="4a691-109">description</span><span class="sxs-lookup"><span data-stu-id="4a691-109">description</span></span>  
    <span data-ttu-id="4a691-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4a691-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4a691-111">Description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="4a691-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a691-112">Raise</span><span class="sxs-lookup"><span data-stu-id="4a691-112">err</span></span>  
    <span data-ttu-id="4a691-113">Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4a691-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="4a691-114">Code d’erreur de l’exception.</span><span class="sxs-lookup"><span data-stu-id="4a691-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a691-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a691-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a691-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4a691-116">Reference</span></span>

[<span data-ttu-id="4a691-117">EsentOperationException, classe</span><span class="sxs-lookup"><span data-stu-id="4a691-117">EsentOperationException class</span></span>](./esentoperationexception-class.md)

[<span data-ttu-id="4a691-118">Membres EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="4a691-118">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="4a691-119">Surcharge EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="4a691-119">EsentOperationException overload</span></span>](./esentoperationexception-constructor.md)

[<span data-ttu-id="4a691-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4a691-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
