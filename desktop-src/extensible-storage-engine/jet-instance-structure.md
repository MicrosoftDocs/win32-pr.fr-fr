---
description: 'En savoir plus sur : structure JET_INSTANCE'
title: Structure JET_INSTANCE
TOCTitle: JET_INSTANCE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance(v=EXCHG.10)
ms:contentKeyID: 39510997
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a676c0815ba20b725da0216a7c9a145c1c1cfd68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203916"
---
# <a name="jet_instance-structure"></a><span data-ttu-id="4e103-103">Structure JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4e103-103">JET_INSTANCE structure</span></span>

<span data-ttu-id="4e103-104">Un JET_INSTANCE contient un descripteur de l’instance de la base de données à utiliser pour les appels à l’API JET.</span><span class="sxs-lookup"><span data-stu-id="4e103-104">A JET_INSTANCE contains a handle to the instance of the database to use for calls to the JET API.</span></span>

<span data-ttu-id="4e103-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4e103-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4e103-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4e103-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4e103-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e103-107">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INSTANCE _
    Implements IEquatable(Of JET_INSTANCE), IFormattable
'Usage
Dim instance As JET_INSTANCE
```

``` csharp
public struct JET_INSTANCE : IEquatable<JET_INSTANCE>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="4e103-108">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="4e103-108">Thread safety</span></span>

<span data-ttu-id="4e103-109">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4e103-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4e103-110">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4e103-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e103-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e103-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4e103-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4e103-112">Reference</span></span>

[<span data-ttu-id="4e103-113">Membres JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4e103-113">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="4e103-114">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4e103-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
