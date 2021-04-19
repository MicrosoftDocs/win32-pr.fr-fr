---
description: 'En savoir plus sur : InstanceParameters. PreferredVerPages, propriété'
title: InstanceParameters. PreferredVerPages, propriété
TOCTitle: 'PreferredVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.preferredverpages(v=EXCHG.10)
ms:contentKeyID: 55103322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PreferredVerPages
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 067d41cd3fb945b2f18d3cd6154b1eef6793b1e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518523"
---
# <a name="instanceparameterspreferredverpages-property"></a><span data-ttu-id="b27dd-103">InstanceParameters. PreferredVerPages, propriété</span><span class="sxs-lookup"><span data-stu-id="b27dd-103">InstanceParameters.PreferredVerPages property</span></span>

<span data-ttu-id="b27dd-104">Obtient ou définit le nombre préféré de pages de la Banque des versions réservées pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="b27dd-104">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="b27dd-105">Si la taille de la Banque des versions dépasse ce seuil, toutes les informations qui sont utilisées uniquement pour les tâches en arrière-plan facultatives, telles que la récupération de l’espace supprimé dans la base de données, sont sacrifiées pour conserver de l’espace pour les informations transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="b27dd-105">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="b27dd-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b27dd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b27dd-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b27dd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b27dd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b27dd-108">Syntax</span></span>

``` vb
'Declaration
Public Property PreferredVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PreferredVerPages

instance.PreferredVerPages = value
```

``` csharp
public int PreferredVerPages { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b27dd-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b27dd-109">Property value</span></span>

<span data-ttu-id="b27dd-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b27dd-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b27dd-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b27dd-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b27dd-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b27dd-112">Reference</span></span>

[<span data-ttu-id="b27dd-113">InstanceParameters, classe</span><span class="sxs-lookup"><span data-stu-id="b27dd-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="b27dd-114">Membres InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="b27dd-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="b27dd-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b27dd-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
