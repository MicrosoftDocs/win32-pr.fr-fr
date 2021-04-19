---
description: 'En savoir plus sur : JET_CALLBACK délégué'
title: Délégué JET_CALLBACK
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617cbefba047f822b338627a782be7e016c2a16f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522182"
---
# <a name="jet_callback-delegate"></a><span data-ttu-id="49577-103">Délégué JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="49577-103">JET_CALLBACK delegate</span></span>

<span data-ttu-id="49577-104">Fonction de rappel polyvalente utilisée par le moteur de base de données pour informer l’application d’un événement impliquant la défragmentation en ligne et les notifications de l’état du curseur.</span><span class="sxs-lookup"><span data-stu-id="49577-104">A multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="49577-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="49577-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="49577-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="49577-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="49577-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49577-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a><span data-ttu-id="49577-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49577-108">Parameters</span></span>

  - <span data-ttu-id="49577-109">sesid</span><span class="sxs-lookup"><span data-stu-id="49577-109">sesid</span></span>  
    <span data-ttu-id="49577-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="49577-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="49577-111">Session pour laquelle le rappel est effectué.</span><span class="sxs-lookup"><span data-stu-id="49577-111">The session for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="49577-112">dbid</span><span class="sxs-lookup"><span data-stu-id="49577-112">dbid</span></span>  
    <span data-ttu-id="49577-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="49577-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="49577-114">Base de données pour laquelle le rappel est effectué.</span><span class="sxs-lookup"><span data-stu-id="49577-114">The database for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="49577-115">TableID</span><span class="sxs-lookup"><span data-stu-id="49577-115">tableid</span></span>  
    <span data-ttu-id="49577-116">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="49577-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="49577-117">Curseur pour lequel le rappel est effectué.</span><span class="sxs-lookup"><span data-stu-id="49577-117">The cursor for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="49577-118">cbtyp</span><span class="sxs-lookup"><span data-stu-id="49577-118">cbtyp</span></span>  
    <span data-ttu-id="49577-119">Type : [Microsoft.ISAM.esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="49577-119">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="49577-120">Opération pour laquelle le rappel est effectué.</span><span class="sxs-lookup"><span data-stu-id="49577-120">The operation for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="49577-121">arg1</span><span class="sxs-lookup"><span data-stu-id="49577-121">arg1</span></span>  
    <span data-ttu-id="49577-122">Type : [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="49577-122">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="49577-123">Premier argument spécifique au rappel.</span><span class="sxs-lookup"><span data-stu-id="49577-123">First callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="49577-124">arg2</span><span class="sxs-lookup"><span data-stu-id="49577-124">arg2</span></span>  
    <span data-ttu-id="49577-125">Type : [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="49577-125">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="49577-126">Deuxième argument spécifique au rappel.</span><span class="sxs-lookup"><span data-stu-id="49577-126">Second callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="49577-127">contexte</span><span class="sxs-lookup"><span data-stu-id="49577-127">context</span></span>  
    <span data-ttu-id="49577-128">Type : [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="49577-128">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="49577-129">Contexte de rappel.</span><span class="sxs-lookup"><span data-stu-id="49577-129">Callback context.</span></span>

<!-- end list -->

  - <span data-ttu-id="49577-130">unused</span><span class="sxs-lookup"><span data-stu-id="49577-130">unused</span></span>  
    <span data-ttu-id="49577-131">Type : [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="49577-131">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="49577-132">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="49577-132">This parameter is not used.</span></span>

#### <a name="return-value"></a><span data-ttu-id="49577-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49577-133">Return value</span></span>

<span data-ttu-id="49577-134">Type : [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="49577-134">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="49577-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49577-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="49577-136">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="49577-136">Reference</span></span>

[<span data-ttu-id="49577-137">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="49577-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
