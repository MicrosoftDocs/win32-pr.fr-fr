---
description: 'En savoir plus sur : SystemParameters. OutstandingIOMax, propriété'
title: Propriété SystemParameters. OutstandingIOMax
TOCTitle: 'OutstandingIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.outstandingiomax(v=EXCHG.10)
ms:contentKeyID: 55104045
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.set_OutstandingIOMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7faf7af3aec16bc81fada5c8742b4c60595bedad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529284"
---
# <a name="systemparametersoutstandingiomax-property"></a><span data-ttu-id="32e90-103">Propriété SystemParameters. OutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="32e90-103">SystemParameters.OutstandingIOMax property</span></span>

<span data-ttu-id="32e90-104">Ce paramètre contrôle le nombre d’e/s de fichier de base de données qui peuvent être mises en file d’attente par disque dans le système d’exploitation hôte à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="32e90-104">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="32e90-105">Une valeur plus élevée pour ce paramètre peut améliorer considérablement les performances d’une application de base de données volumineuse.</span><span class="sxs-lookup"><span data-stu-id="32e90-105">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="32e90-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="32e90-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="32e90-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="32e90-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="32e90-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32e90-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property OutstandingIOMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.OutstandingIOMax

SystemParameters.OutstandingIOMax = value
```

``` csharp
public static int OutstandingIOMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="32e90-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="32e90-109">Property value</span></span>

<span data-ttu-id="32e90-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="32e90-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="32e90-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32e90-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="32e90-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="32e90-112">Reference</span></span>

[<span data-ttu-id="32e90-113">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="32e90-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="32e90-114">Membres SystemParameters</span><span class="sxs-lookup"><span data-stu-id="32e90-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="32e90-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="32e90-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
