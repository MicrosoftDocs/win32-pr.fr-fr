---
description: 'En savoir plus sur : méthode API. JetSetCurrentIndex3'
title: API. JetSetCurrentIndex3, méthode
TOCTitle: 'JetSetCurrentIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex3(v=EXCHG.10)
ms:contentKeyID: 55100805
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c56f259a35026bb47a5e58b7b364b52d9bedbc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520005"
---
# <a name="apijetsetcurrentindex3-method"></a><span data-ttu-id="e6dd8-103">API. JetSetCurrentIndex3, méthode</span><span class="sxs-lookup"><span data-stu-id="e6dd8-103">Api.JetSetCurrentIndex3 method</span></span>

<span data-ttu-id="e6dd8-104">Définit l’index actuel d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="e6dd8-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="e6dd8-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6dd8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6dd8-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6dd8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6dd8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6dd8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex3 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex3(sesid, _
    tableid, index, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex3(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="e6dd8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6dd8-108">Parameters</span></span>

  - <span data-ttu-id="e6dd8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e6dd8-109">sesid</span></span>  
    <span data-ttu-id="e6dd8-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e6dd8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e6dd8-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e6dd8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6dd8-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e6dd8-112">tableid</span></span>  
    <span data-ttu-id="e6dd8-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e6dd8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e6dd8-114">Curseur sur lequel définir l’index.</span><span class="sxs-lookup"><span data-stu-id="e6dd8-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6dd8-115">index</span><span class="sxs-lookup"><span data-stu-id="e6dd8-115">index</span></span>  
    <span data-ttu-id="e6dd8-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e6dd8-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e6dd8-117">Nom de l’index à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="e6dd8-117">The name of the index to be selected.</span></span> <span data-ttu-id="e6dd8-118">Si la valeur est null ou vide, l’index primaire est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e6dd8-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6dd8-119">grbit</span><span class="sxs-lookup"><span data-stu-id="e6dd8-119">grbit</span></span>  
    <span data-ttu-id="e6dd8-120">Type : [Microsoft. ISAM. esent. Interop. SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e6dd8-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e6dd8-121">Définissez les options d’index.</span><span class="sxs-lookup"><span data-stu-id="e6dd8-121">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6dd8-122">itagSequence</span><span class="sxs-lookup"><span data-stu-id="e6dd8-122">itagSequence</span></span>  
    <span data-ttu-id="e6dd8-123">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e6dd8-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e6dd8-124">Numéro de séquence de la valeur de colonne à valeurs multiples qui sera utilisée pour positionner le curseur sur le nouvel index.</span><span class="sxs-lookup"><span data-stu-id="e6dd8-124">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="e6dd8-125">Ce paramètre est utilisé uniquement conjointement avec [nomove](./setcurrentindexgrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="e6dd8-125">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="e6dd8-126">Lorsque ce paramètre n’est pas présent ou qu’il est défini sur zéro, sa valeur est supposée être 1.</span><span class="sxs-lookup"><span data-stu-id="e6dd8-126">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6dd8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6dd8-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6dd8-128">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e6dd8-128">Reference</span></span>

[<span data-ttu-id="e6dd8-129">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="e6dd8-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e6dd8-130">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="e6dd8-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e6dd8-131">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e6dd8-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
