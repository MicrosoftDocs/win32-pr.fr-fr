---
description: 'En savoir plus sur : Update. Save, méthode'
title: Update. Save, méthode
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad933c9601dc1a20932550aef363e067458ff79e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106535035"
---
# <a name="updatesave-method"></a><span data-ttu-id="1f7d1-103">Update. Save, méthode</span><span class="sxs-lookup"><span data-stu-id="1f7d1-103">Update.Save method</span></span>

<span data-ttu-id="1f7d1-104">Mettez à jour TableID.</span><span class="sxs-lookup"><span data-stu-id="1f7d1-104">Update the tableid.</span></span>

<span data-ttu-id="1f7d1-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f7d1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1f7d1-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1f7d1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f7d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f7d1-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a><span data-ttu-id="1f7d1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1f7d1-108">Remarks</span></span>

<span data-ttu-id="1f7d1-109">L’enregistrement est la dernière étape de l’exécution d’une instruction INSERT ou Update.</span><span class="sxs-lookup"><span data-stu-id="1f7d1-109">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="1f7d1-110">La mise à jour commence par appeler la création d’un objet de mise à jour, puis en appelant JetSetColumn ou JetSetColumns une ou plusieurs fois pour définir l’état de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1f7d1-110">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="1f7d1-111">Enfin, Update est appelé pour terminer l’opération de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="1f7d1-111">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="1f7d1-112">Les index sont mis à jour uniquement par Update ou et non pendant JetSetColumn ou JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="1f7d1-112">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f7d1-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f7d1-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f7d1-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1f7d1-114">Reference</span></span>

[<span data-ttu-id="1f7d1-115">Classe de mise à jour</span><span class="sxs-lookup"><span data-stu-id="1f7d1-115">Update class</span></span>](./update-class.md)

[<span data-ttu-id="1f7d1-116">Mettre à jour les membres</span><span class="sxs-lookup"><span data-stu-id="1f7d1-116">Update members</span></span>](./update-members.md)

[<span data-ttu-id="1f7d1-117">Enregistrer la surcharge</span><span class="sxs-lookup"><span data-stu-id="1f7d1-117">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="1f7d1-118">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1f7d1-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
