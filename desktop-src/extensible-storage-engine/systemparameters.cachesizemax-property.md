---
description: 'En savoir plus sur : SystemParameters. CacheSizeMax, propriété'
title: Propriété SystemParameters. CacheSizeMax
TOCTitle: 'CacheSizeMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesizemax(v=EXCHG.10)
ms:contentKeyID: 55104037
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7b03df288a0263cf6b79281f5ed79330dfd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210375"
---
# <a name="systemparameterscachesizemax-property"></a><span data-ttu-id="09e85-103">Propriété SystemParameters. CacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="09e85-103">SystemParameters.CacheSizeMax property</span></span>

<span data-ttu-id="09e85-104">Obtient ou définit la taille maximale du cache de la page de base de données.</span><span class="sxs-lookup"><span data-stu-id="09e85-104">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="09e85-105">La taille est dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="09e85-105">The size is in database pages.</span></span> <span data-ttu-id="09e85-106">Si ce paramètre est laissé à sa valeur par défaut, la taille maximale du cache sera définie sur la taille de la mémoire physique lors de l’appel de JetInit.</span><span class="sxs-lookup"><span data-stu-id="09e85-106">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span>

<span data-ttu-id="09e85-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09e85-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="09e85-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="09e85-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09e85-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09e85-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSizeMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSizeMax

SystemParameters.CacheSizeMax = value
```

``` csharp
public static int CacheSizeMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="09e85-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="09e85-110">Property value</span></span>

<span data-ttu-id="09e85-111">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="09e85-111">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="09e85-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09e85-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09e85-113">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="09e85-113">Reference</span></span>

[<span data-ttu-id="09e85-114">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="09e85-114">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="09e85-115">Membres SystemParameters</span><span class="sxs-lookup"><span data-stu-id="09e85-115">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="09e85-116">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="09e85-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
