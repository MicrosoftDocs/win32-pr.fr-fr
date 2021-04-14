---
description: 'En savoir plus sur : méthode Update. Save (Byte, Int32, Int32)'
title: Update. Save, méthode (Byte, Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485153"
---
# <a name="updatesave-method-byte--int32-int32"></a><span data-ttu-id="c20b5-103">Update. Save, méthode (Byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="c20b5-103">Update.Save method (Byte , Int32, Int32)</span></span>

<span data-ttu-id="c20b5-104">Mettez à jour TableID.</span><span class="sxs-lookup"><span data-stu-id="c20b5-104">Update the tableid.</span></span>

<span data-ttu-id="c20b5-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c20b5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c20b5-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c20b5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c20b5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c20b5-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="c20b5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c20b5-108">Parameters</span></span>

  - <span data-ttu-id="c20b5-109">signet</span><span class="sxs-lookup"><span data-stu-id="c20b5-109">bookmark</span></span>  
    <span data-ttu-id="c20b5-110">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="c20b5-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="c20b5-111">Retourne le signet de l’enregistrement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="c20b5-111">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="c20b5-112">Peut être Null.</span><span class="sxs-lookup"><span data-stu-id="c20b5-112">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="c20b5-113">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="c20b5-113">bookmarkSize</span></span>  
    <span data-ttu-id="c20b5-114">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c20b5-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c20b5-115">Taille de la mémoire tampon du signet.</span><span class="sxs-lookup"><span data-stu-id="c20b5-115">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="c20b5-116">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="c20b5-116">actualBookmarkSize</span></span>  
    <span data-ttu-id="c20b5-117">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c20b5-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c20b5-118">Retourne la taille réelle du signet.</span><span class="sxs-lookup"><span data-stu-id="c20b5-118">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="c20b5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c20b5-119">Remarks</span></span>

<span data-ttu-id="c20b5-120">L’enregistrement est la dernière étape de l’exécution d’une instruction INSERT ou Update.</span><span class="sxs-lookup"><span data-stu-id="c20b5-120">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="c20b5-121">La mise à jour commence par appeler la création d’un objet de mise à jour, puis en appelant JetSetColumn ou JetSetColumns une ou plusieurs fois pour définir l’état de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c20b5-121">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="c20b5-122">Enfin, Update est appelé pour terminer l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c20b5-122">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="c20b5-123">Les index sont mis à jour uniquement par Update ou et non pendant JetSetColumn ou JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="c20b5-123">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="c20b5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c20b5-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c20b5-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c20b5-125">Reference</span></span>

[<span data-ttu-id="c20b5-126">Classe de mise à jour</span><span class="sxs-lookup"><span data-stu-id="c20b5-126">Update class</span></span>](./update-class.md)

[<span data-ttu-id="c20b5-127">Mettre à jour les membres</span><span class="sxs-lookup"><span data-stu-id="c20b5-127">Update members</span></span>](./update-members.md)

[<span data-ttu-id="c20b5-128">Enregistrer la surcharge</span><span class="sxs-lookup"><span data-stu-id="c20b5-128">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="c20b5-129">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c20b5-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
