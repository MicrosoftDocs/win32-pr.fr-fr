---
description: 'En savoir plus sur : propriété JET_ENUMCOLUMNID. ctagSequence'
title: JET_ENUMCOLUMNID. ctagSequence, propriété
TOCTitle: 'ctagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.ctagsequence(v=EXCHG.10)
ms:contentKeyID: 55107537
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_ctagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e12c8c6a102cbb20862b3cc9859f7e632ade8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519292"
---
# <a name="jet_enumcolumnidctagsequence-property"></a><span data-ttu-id="75367-103">JET_ENUMCOLUMNID. ctagSequence, propriété</span><span class="sxs-lookup"><span data-stu-id="75367-103">JET_ENUMCOLUMNID.ctagSequence property</span></span>

<span data-ttu-id="75367-104">Obtient ou définit le nombre de valeurs de colonne (par index de base un) à énumérer pour l’ID de colonne spécifié.</span><span class="sxs-lookup"><span data-stu-id="75367-104">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="75367-105">Si ctagSequence a la valeur 0 (zéro), rgtagSequence est ignoré et toutes les valeurs de colonne pour l’ID de colonne spécifié seront énumérées.</span><span class="sxs-lookup"><span data-stu-id="75367-105">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="75367-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75367-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75367-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="75367-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75367-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75367-108">Syntax</span></span>

``` vb
'Declaration
Public Property ctagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer

value = instance.ctagSequence

instance.ctagSequence = value
```

``` csharp
public int ctagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="75367-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="75367-109">Property value</span></span>

<span data-ttu-id="75367-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="75367-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="75367-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75367-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75367-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="75367-112">Reference</span></span>

[<span data-ttu-id="75367-113">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="75367-113">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="75367-114">Membres JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="75367-114">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="75367-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="75367-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
