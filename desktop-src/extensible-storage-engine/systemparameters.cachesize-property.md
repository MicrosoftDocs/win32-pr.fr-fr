---
description: 'En savoir plus sur : SystemParameters. CacheSize, propriété'
title: SystemParameters. CacheSize, propriété
TOCTitle: 'CacheSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesize(v=EXCHG.10)
ms:contentKeyID: 55104109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0981f02df3b807ab56fa20922d1e245f00c2df34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210497"
---
# <a name="systemparameterscachesize-property"></a><span data-ttu-id="f0037-103">SystemParameters. CacheSize, propriété</span><span class="sxs-lookup"><span data-stu-id="f0037-103">SystemParameters.CacheSize property</span></span>

<span data-ttu-id="f0037-104">Obtient ou définit la taille du cache de base de données dans les pages.</span><span class="sxs-lookup"><span data-stu-id="f0037-104">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="f0037-105">Par défaut, le cache de base de données ajuste automatiquement sa taille, la définition de cette propriété sur une valeur différente de zéro entraîne l’ajustement du cache à la taille cible.</span><span class="sxs-lookup"><span data-stu-id="f0037-105">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span>

<span data-ttu-id="f0037-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f0037-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f0037-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f0037-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f0037-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0037-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSize As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSize

SystemParameters.CacheSize = value
```

``` csharp
public static int CacheSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="f0037-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f0037-109">Property value</span></span>

<span data-ttu-id="f0037-110">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f0037-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0037-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0037-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f0037-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f0037-112">Reference</span></span>

[<span data-ttu-id="f0037-113">SystemParameters (classe)</span><span class="sxs-lookup"><span data-stu-id="f0037-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="f0037-114">Membres SystemParameters</span><span class="sxs-lookup"><span data-stu-id="f0037-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="f0037-115">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f0037-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
