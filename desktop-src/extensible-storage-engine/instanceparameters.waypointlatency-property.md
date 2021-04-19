---
description: 'En savoir plus sur : InstanceParameters. WaypointLatency, propriété'
title: InstanceParameters. WaypointLatency, propriété
TOCTitle: 'WaypointLatency property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55103325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_WaypointLatency
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d7d837d7fff804926529ec67780e319d85031f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543540"
---
# <a name="instanceparameterswaypointlatency-property"></a><span data-ttu-id="c0071-103">InstanceParameters. WaypointLatency, propriété</span><span class="sxs-lookup"><span data-stu-id="c0071-103">InstanceParameters.WaypointLatency property</span></span>

<span data-ttu-id="c0071-104">Obtient ou définit le nombre de journaux pour lesquels esent diffère le vidage de base de données.</span><span class="sxs-lookup"><span data-stu-id="c0071-104">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="c0071-105">Cela peut être utilisé pour augmenter la capacité de récupération de base de données en cas de perte de fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="c0071-105">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="c0071-106">Pris en charge sur Windows 7 et les autres.</span><span class="sxs-lookup"><span data-stu-id="c0071-106">Supported on Windows 7 and up.</span></span> <span data-ttu-id="c0071-107">Ignoré sur Windows XP, Windows Server 2003, Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c0071-107">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="c0071-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c0071-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c0071-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c0071-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c0071-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0071-110">Syntax</span></span>

``` vb
'Declaration
Public Property WaypointLatency As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.WaypointLatency

instance.WaypointLatency = value
```

``` csharp
public int WaypointLatency { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c0071-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c0071-111">Property value</span></span>

<span data-ttu-id="c0071-112">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c0071-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c0071-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0071-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c0071-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c0071-114">Reference</span></span>

[<span data-ttu-id="c0071-115">InstanceParameters, classe</span><span class="sxs-lookup"><span data-stu-id="c0071-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="c0071-116">Membres InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="c0071-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="c0071-117">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c0071-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
