---
description: 'En savoir plus sur : constructeur EsentQuotaException (String, JET_err)'
title: Constructeur EsentQuotaException (String, JET_err)
TOCTitle: EsentQuotaException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentQuotaException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102558
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f615cf2a46beb8c504de3dcc7d6fab1fc23da47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534524"
---
# <a name="esentquotaexception-constructor-string-jet_err"></a><span data-ttu-id="99788-103">Constructeur EsentQuotaException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="99788-103">EsentQuotaException constructor (String, JET_err)</span></span>

<span data-ttu-id="99788-104">Initialise une nouvelle instance de la classe EsentQuotaException.</span><span class="sxs-lookup"><span data-stu-id="99788-104">Initializes a new instance of the EsentQuotaException class.</span></span>

<span data-ttu-id="99788-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99788-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99788-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="99788-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99788-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99788-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentQuotaException(description, _
    err)
```

``` csharp
protected EsentQuotaException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="99788-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99788-108">Parameters</span></span>

  - <span data-ttu-id="99788-109">description</span><span class="sxs-lookup"><span data-stu-id="99788-109">description</span></span>  
    <span data-ttu-id="99788-110">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="99788-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="99788-111">Description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="99788-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="99788-112">Raise</span><span class="sxs-lookup"><span data-stu-id="99788-112">err</span></span>  
    <span data-ttu-id="99788-113">Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="99788-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="99788-114">Code d’erreur de l’exception.</span><span class="sxs-lookup"><span data-stu-id="99788-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="99788-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99788-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99788-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="99788-116">Reference</span></span>

[<span data-ttu-id="99788-117">Classe EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="99788-117">EsentQuotaException class</span></span>](./esentquotaexception-class.md)

[<span data-ttu-id="99788-118">Membres EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="99788-118">EsentQuotaException members</span></span>](./esentquotaexception-members.md)

[<span data-ttu-id="99788-119">Surcharge EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="99788-119">EsentQuotaException overload</span></span>](./esentquotaexception-constructor.md)

[<span data-ttu-id="99788-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="99788-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
