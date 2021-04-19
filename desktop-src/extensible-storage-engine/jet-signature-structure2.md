---
description: 'En savoir plus sur : structure JET_SIGNATURE'
title: Structure JET_SIGNATURE
TOCTitle: JET_SIGNATURE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SIGNATURE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature(v=EXCHG.10)
ms:contentKeyID: 39511048
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5c8ce12b23194aea2a45c273e0207f88faad6f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514652"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="fd854-103">Structure JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="fd854-103">JET_SIGNATURE structure</span></span>

<span data-ttu-id="fd854-104">La structure JET_SIGNATURE contient des informations qui identifient de façon unique une séquence de base de données ou de fichier journal.</span><span class="sxs-lookup"><span data-stu-id="fd854-104">The JET_SIGNATURE structure contains information that uniquely identifies a database or logfile sequence.</span></span>

<span data-ttu-id="fd854-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fd854-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fd854-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fd854-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fd854-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd854-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_SIGNATURE _
    Implements IEquatable(Of JET_SIGNATURE)
'Usage
Dim instance As JET_SIGNATURE
```

``` csharp
[SerializableAttribute]
public struct JET_SIGNATURE : IEquatable<JET_SIGNATURE>
```

## <a name="thread-safety"></a><span data-ttu-id="fd854-108">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="fd854-108">Thread safety</span></span>

<span data-ttu-id="fd854-109">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="fd854-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fd854-110">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="fd854-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd854-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd854-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fd854-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="fd854-112">Reference</span></span>

[<span data-ttu-id="fd854-113">Membres JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="fd854-113">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="fd854-114">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fd854-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
