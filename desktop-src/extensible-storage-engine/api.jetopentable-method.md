---
description: 'En savoir plus sur : méthode API. JetOpenTable'
title: API. JetOpenTable, méthode
TOCTitle: 'JetOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentable(v=EXCHG.10)
ms:contentKeyID: 55100776
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5764138d4ea387b68c94805c6966f7ce0e817c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952975"
---
# <a name="apijetopentable-method"></a><span data-ttu-id="27776-103">API. JetOpenTable, méthode</span><span class="sxs-lookup"><span data-stu-id="27776-103">Api.JetOpenTable method</span></span>

<span data-ttu-id="27776-104">Ouvre un curseur sur une table créée précédemment.</span><span class="sxs-lookup"><span data-stu-id="27776-104">Opens a cursor on a previously created table.</span></span>

<span data-ttu-id="27776-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="27776-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="27776-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="27776-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="27776-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27776-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    parameters As Byte(), _
    parametersSize As Integer, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim parameters As Byte()
Dim parametersSize As Integer
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As JET_wrn

returnValue = Api.JetOpenTable(sesid, _
    dbid, tablename, parameters, parametersSize, _
    grbit, tableid)
```

``` csharp
public static JET_wrn JetOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    byte[] parameters,
    int parametersSize,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="27776-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27776-108">Parameters</span></span>

  - <span data-ttu-id="27776-109">sesid</span><span class="sxs-lookup"><span data-stu-id="27776-109">sesid</span></span>  
    <span data-ttu-id="27776-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="27776-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="27776-111">Session de base de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="27776-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="27776-112">dbid</span><span class="sxs-lookup"><span data-stu-id="27776-112">dbid</span></span>  
    <span data-ttu-id="27776-113">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="27776-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="27776-114">Base de données dans laquelle ouvrir la table.</span><span class="sxs-lookup"><span data-stu-id="27776-114">The database to open the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="27776-115">tablename</span><span class="sxs-lookup"><span data-stu-id="27776-115">tablename</span></span>  
    <span data-ttu-id="27776-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="27776-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="27776-117">Nom de la table à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="27776-117">The name of the table to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="27776-118">parameters</span><span class="sxs-lookup"><span data-stu-id="27776-118">parameters</span></span>  
    <span data-ttu-id="27776-119">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="27776-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="27776-120">Le paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="27776-120">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="27776-121">parametersSize</span><span class="sxs-lookup"><span data-stu-id="27776-121">parametersSize</span></span>  
    <span data-ttu-id="27776-122">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="27776-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="27776-123">Le paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="27776-123">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="27776-124">grbit</span><span class="sxs-lookup"><span data-stu-id="27776-124">grbit</span></span>  
    <span data-ttu-id="27776-125">Type : [Microsoft. ISAM. esent. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="27776-125">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="27776-126">Options d’ouverture de la table.</span><span class="sxs-lookup"><span data-stu-id="27776-126">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="27776-127">TableID</span><span class="sxs-lookup"><span data-stu-id="27776-127">tableid</span></span>  
    <span data-ttu-id="27776-128">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="27776-128">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="27776-129">Retourne la table ouverte.</span><span class="sxs-lookup"><span data-stu-id="27776-129">Returns the opened table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="27776-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27776-130">Return value</span></span>

<span data-ttu-id="27776-131">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="27776-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="27776-132">AVERTISSEMENT ESENT.</span><span class="sxs-lookup"><span data-stu-id="27776-132">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="27776-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27776-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="27776-134">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="27776-134">Reference</span></span>

[<span data-ttu-id="27776-135">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="27776-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="27776-136">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="27776-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="27776-137">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="27776-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
