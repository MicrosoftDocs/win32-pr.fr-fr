---
description: 'En savoir plus sur : InstanceParameters. MaxTemporaryTables, propriété'
title: InstanceParameters. MaxTemporaryTables, propriété
TOCTitle: 'MaxTemporaryTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtemporarytables(v=EXCHG.10)
ms:contentKeyID: 55103560
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTemporaryTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5802e512a4ea6a4916ae54c24357dbdad057540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520641"
---
# <a name="instanceparametersmaxtemporarytables-property"></a><span data-ttu-id="3de0f-103">InstanceParameters. MaxTemporaryTables, propriété</span><span class="sxs-lookup"><span data-stu-id="3de0f-103">InstanceParameters.MaxTemporaryTables property</span></span>

<span data-ttu-id="3de0f-104">Obtient ou définit le nombre de ressources de table temporaire à utiliser par une instance.</span><span class="sxs-lookup"><span data-stu-id="3de0f-104">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="3de0f-105">Ce paramètre affecte le nombre de tables temporaires qui peuvent être utilisées en même temps.</span><span class="sxs-lookup"><span data-stu-id="3de0f-105">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="3de0f-106">Si ce paramètre système est défini à zéro, aucune base de données temporaire n’est créée et toute activité nécessitant l’utilisation de la base de données temporaire échoue.</span><span class="sxs-lookup"><span data-stu-id="3de0f-106">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="3de0f-107">Ce paramètre peut être utile pour éviter les e/s nécessaires à la création de la base de données temporaire si elle est connue qu’elle ne sera pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="3de0f-107">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="3de0f-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3de0f-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3de0f-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3de0f-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3de0f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3de0f-110">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTemporaryTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTemporaryTables

instance.MaxTemporaryTables = value
```

``` csharp
public int MaxTemporaryTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3de0f-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3de0f-111">Property value</span></span>

<span data-ttu-id="3de0f-112">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3de0f-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="remarks"></a><span data-ttu-id="3de0f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3de0f-113">Remarks</span></span>

<span data-ttu-id="3de0f-114">L’utilisation d’une table temporaire requiert également une ressource curseur.</span><span class="sxs-lookup"><span data-stu-id="3de0f-114">The use of a temporary table also requires a cursor resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="3de0f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3de0f-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3de0f-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3de0f-116">Reference</span></span>

[<span data-ttu-id="3de0f-117">InstanceParameters, classe</span><span class="sxs-lookup"><span data-stu-id="3de0f-117">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="3de0f-118">Membres InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="3de0f-118">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="3de0f-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3de0f-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
