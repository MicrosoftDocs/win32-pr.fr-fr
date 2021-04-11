---
description: 'En savoir plus sur : propriété JET_INDEXCREATE. szKey'
title: JET_INDEXCREATE. szKey, propriété
TOCTitle: 'szKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.szkey(v=EXCHG.10)
ms:contentKeyID: 55103656
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86ade65ee28eef6314d31653772b0c22657476d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320497"
---
# <a name="jet_indexcreateszkey-property"></a><span data-ttu-id="b9b00-103">JET_INDEXCREATE. szKey, propriété</span><span class="sxs-lookup"><span data-stu-id="b9b00-103">JET_INDEXCREATE.szKey property</span></span>

<span data-ttu-id="b9b00-104">Obtient ou définit la description de la clé d’index.</span><span class="sxs-lookup"><span data-stu-id="b9b00-104">Gets or sets the description of the index key.</span></span> <span data-ttu-id="b9b00-105">Il s’agit d’une chaîne double qui se termine par un caractère null des jetons délimités par des valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="b9b00-105">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="b9b00-106">Chaque jeton est au format \[ direction-spécificateur- \] \[ nom-colonne \] , où direction-Specification est « + » ou « - ».</span><span class="sxs-lookup"><span data-stu-id="b9b00-106">Each token is of the form \[direction-specifier\]\[column-name\], where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="b9b00-107">par exemple, un szKey de « + ABC \\ 0-Def \\ 0 + GHI \\ 0 » sera indexé sur les trois colonnes « ABC » (dans l’ordre croissant), « def » (dans l’ordre décroissant) et « GHI » (dans l’ordre croissant).</span><span class="sxs-lookup"><span data-stu-id="b9b00-107">for example, a szKey of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span>

<span data-ttu-id="b9b00-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9b00-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b9b00-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b9b00-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9b00-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9b00-110">Syntax</span></span>

``` vb
'Declaration
Public Property szKey As String
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As String

value = instance.szKey

instance.szKey = value
```

``` csharp
public string szKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b9b00-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b9b00-111">Property value</span></span>

<span data-ttu-id="b9b00-112">Type : [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b9b00-112">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9b00-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9b00-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9b00-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b9b00-114">Reference</span></span>

[<span data-ttu-id="b9b00-115">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="b9b00-115">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="b9b00-116">Membres JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="b9b00-116">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="b9b00-117">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b9b00-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
