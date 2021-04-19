---
description: 'En savoir plus sur : méthode API. JetSetCurrentIndex'
title: API. JetSetCurrentIndex, méthode
TOCTitle: 'JetSetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed3c069962fe879e250f90e34744780dfe2eb862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530267"
---
# <a name="apijetsetcurrentindex-method"></a><span data-ttu-id="d0247-103">API. JetSetCurrentIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="d0247-103">Api.JetSetCurrentIndex method</span></span>

<span data-ttu-id="d0247-104">Définit l’index actuel d’un curseur.</span><span class="sxs-lookup"><span data-stu-id="d0247-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="d0247-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0247-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d0247-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d0247-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0247-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0247-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As StringApi.JetSetCurrentIndex(sesid, tableid, _
    index)
```

``` csharp
public static void JetSetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index
)
```

#### <a name="parameters"></a><span data-ttu-id="d0247-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0247-108">Parameters</span></span>

  - <span data-ttu-id="d0247-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d0247-109">sesid</span></span>  
    <span data-ttu-id="d0247-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d0247-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d0247-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d0247-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d0247-112">TableID</span><span class="sxs-lookup"><span data-stu-id="d0247-112">tableid</span></span>  
    <span data-ttu-id="d0247-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d0247-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d0247-114">Curseur sur lequel définir l’index.</span><span class="sxs-lookup"><span data-stu-id="d0247-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="d0247-115">index</span><span class="sxs-lookup"><span data-stu-id="d0247-115">index</span></span>  
    <span data-ttu-id="d0247-116">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d0247-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d0247-117">Nom de l’index à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="d0247-117">The name of the index to be selected.</span></span> <span data-ttu-id="d0247-118">Si la valeur est null ou vide, l’index primaire est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d0247-118">If this is null or empty the primary index will be selected.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0247-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0247-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0247-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d0247-120">Reference</span></span>

[<span data-ttu-id="d0247-121">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="d0247-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d0247-122">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="d0247-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d0247-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d0247-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
