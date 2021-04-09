---
description: 'En savoir plus sur : structure JET_DBID'
title: Structure JET_DBID
TOCTitle: JET_DBID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DBID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid(v=EXCHG.10)
ms:contentKeyID: 39515255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e92373015b64593936ee8d447b619932d168157c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865873"
---
# <a name="jet_dbid-structure"></a><span data-ttu-id="0ebb5-103">Structure JET_DBID</span><span class="sxs-lookup"><span data-stu-id="0ebb5-103">JET_DBID structure</span></span>

<span data-ttu-id="0ebb5-104">Un JET_DBID contient le descripteur de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-104">A JET_DBID contains the handle to the database.</span></span> <span data-ttu-id="0ebb5-105">Un descripteur de base de données est utilisé pour gérer le schéma d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-105">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="0ebb5-106">Il peut également être utilisé pour gérer les tables à l’intérieur de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-106">It can also be used to manage the tables inside of that database.</span></span>

<span data-ttu-id="0ebb5-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0ebb5-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0ebb5-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0ebb5-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebb5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ebb5-109">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_DBID _
    Implements IEquatable(Of JET_DBID), IFormattable
'Usage
Dim instance As JET_DBID
```

``` csharp
public struct JET_DBID : IEquatable<JET_DBID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="0ebb5-110">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="0ebb5-110">Thread safety</span></span>

<span data-ttu-id="0ebb5-111">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-111">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0ebb5-112">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0ebb5-112">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ebb5-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ebb5-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0ebb5-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="0ebb5-114">Reference</span></span>

[<span data-ttu-id="0ebb5-115">Membres JET_DBID</span><span class="sxs-lookup"><span data-stu-id="0ebb5-115">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="0ebb5-116">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0ebb5-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
