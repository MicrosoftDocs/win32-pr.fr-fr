---
description: 'En savoir plus sur : méthode Update. SaveAndGotoBookmark'
title: Update. SaveAndGotoBookmark, méthode
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d682657b9821f782af339a3d0c3253b6fa771d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514854"
---
# <a name="updatesaveandgotobookmark-method"></a><span data-ttu-id="91c01-103">Update. SaveAndGotoBookmark, méthode</span><span class="sxs-lookup"><span data-stu-id="91c01-103">Update.SaveAndGotoBookmark method</span></span>

<span data-ttu-id="91c01-104">Mettez à jour l’TableID et positionnez l’TableID sur l’enregistrement qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="91c01-104">Update the tableid and position the tableid on the record that was modified.</span></span> <span data-ttu-id="91c01-105">Cela peut être utile lors de l’insertion d’un enregistrement, car par défaut, TableID reste à son ancien emplacement.</span><span class="sxs-lookup"><span data-stu-id="91c01-105">This can be useful when inserting a record because by default the tableid remains in its old location.</span></span>

<span data-ttu-id="91c01-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="91c01-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="91c01-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="91c01-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="91c01-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91c01-108">Syntax</span></span>

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a><span data-ttu-id="91c01-109">Notes</span><span class="sxs-lookup"><span data-stu-id="91c01-109">Remarks</span></span>

<span data-ttu-id="91c01-110">L’enregistrement est la dernière étape de l’exécution d’une instruction INSERT ou Update.</span><span class="sxs-lookup"><span data-stu-id="91c01-110">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="91c01-111">La mise à jour commence par appeler la création d’un objet de mise à jour, puis en appelant JetSetColumn ou JetSetColumns une ou plusieurs fois pour définir l’état de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="91c01-111">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="91c01-112">Enfin, Update est appelé pour terminer l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="91c01-112">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="91c01-113">Les index sont mis à jour uniquement par Update ou et non pendant JetSetColumn ou JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="91c01-113">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="91c01-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91c01-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="91c01-115">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="91c01-115">Reference</span></span>

[<span data-ttu-id="91c01-116">Classe de mise à jour</span><span class="sxs-lookup"><span data-stu-id="91c01-116">Update class</span></span>](./update-class.md)

[<span data-ttu-id="91c01-117">Mettre à jour les membres</span><span class="sxs-lookup"><span data-stu-id="91c01-117">Update members</span></span>](./update-members.md)

[<span data-ttu-id="91c01-118">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="91c01-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
