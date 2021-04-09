---
description: 'En savoir plus sur : méthode API. JetSetColumns'
title: API. JetSetColumns, méthode
TOCTitle: 'JetSetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_SETCOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumns(v=EXCHG.10)
ms:contentKeyID: 55100800
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 59d1d16a21996937357d0358625772a4b6712019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750756"
---
# <a name="apijetsetcolumns-method"></a><span data-ttu-id="fa82f-103">API. JetSetColumns, méthode</span><span class="sxs-lookup"><span data-stu-id="fa82f-103">Api.JetSetColumns method</span></span>

<span data-ttu-id="fa82f-104">Permet à une application de définir plusieurs valeurs de colonne en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="fa82f-104">Allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="fa82f-105">Un tableau de structures de [JET_SETCOLUMN](./jet-setcolumn-class.md) est utilisé pour décrire l’ensemble des valeurs de colonne à définir, et pour décrire les mémoires tampons d’entrée pour chaque valeur de colonne à définir.</span><span class="sxs-lookup"><span data-stu-id="fa82f-105">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

<span data-ttu-id="fa82f-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fa82f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fa82f-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fa82f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fa82f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa82f-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Shared Function JetSetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    setcolumns As JET_SETCOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim setcolumns As JET_SETCOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumns(sesid, _
    tableid, setcolumns, numColumns)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public static JET_wrn JetSetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_SETCOLUMN[] setcolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="fa82f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa82f-109">Parameters</span></span>

  - <span data-ttu-id="fa82f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="fa82f-110">sesid</span></span>  
    <span data-ttu-id="fa82f-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fa82f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fa82f-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fa82f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fa82f-113">TableID</span><span class="sxs-lookup"><span data-stu-id="fa82f-113">tableid</span></span>  
    <span data-ttu-id="fa82f-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fa82f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fa82f-115">Curseur sur lequel définir les colonnes.</span><span class="sxs-lookup"><span data-stu-id="fa82f-115">The cursor to set the columns on.</span></span>

<!-- end list -->

  - <span data-ttu-id="fa82f-116">SetColumns</span><span class="sxs-lookup"><span data-stu-id="fa82f-116">setcolumns</span></span>  
    <span data-ttu-id="fa82f-117">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="fa82f-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="fa82f-118">Tableau de structures de [JET_SETCOLUMN](./jet-setcolumn-class.md) décrivant les données à définir.</span><span class="sxs-lookup"><span data-stu-id="fa82f-118">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures describing the data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="fa82f-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="fa82f-119">numColumns</span></span>  
    <span data-ttu-id="fa82f-120">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fa82f-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fa82f-121">Nombre d’entrées dans le paramètre SetColumns.</span><span class="sxs-lookup"><span data-stu-id="fa82f-121">Number of entries in the setcolumns parameter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fa82f-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa82f-122">Return value</span></span>

<span data-ttu-id="fa82f-123">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fa82f-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="fa82f-124">Un avertissement.</span><span class="sxs-lookup"><span data-stu-id="fa82f-124">A warning.</span></span> <span data-ttu-id="fa82f-125">Si le dernier jeu de colonnes a un avertissement, cet avertissement est retourné à partir de JetSetColumns lui-même.</span><span class="sxs-lookup"><span data-stu-id="fa82f-125">If the last column set has a warning, then this warning will be returned from JetSetColumns itself.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fa82f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa82f-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fa82f-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="fa82f-127">Reference</span></span>

[<span data-ttu-id="fa82f-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="fa82f-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fa82f-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="fa82f-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fa82f-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fa82f-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
