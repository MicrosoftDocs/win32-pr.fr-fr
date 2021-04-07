---
description: 'En savoir plus sur : classe JET_CONDITIONALCOLUMN'
title: Classe JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn(v=EXCHG.10)
ms:contentKeyID: 55107506
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23b116ce88b24702711d74f610c208a72c44addf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952455"
---
# <a name="jet_conditionalcolumn-class"></a><span data-ttu-id="8fb5a-103">Classe JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8fb5a-103">JET_CONDITIONALCOLUMN class</span></span>

<span data-ttu-id="8fb5a-104">Définit le mode d’exécution de l’indexation conditionnelle pour un index donné.</span><span class="sxs-lookup"><span data-stu-id="8fb5a-104">Defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="8fb5a-105">Un index conditionnel contient une entrée d’index uniquement pour les lignes qui correspondent à la condition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8fb5a-105">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="8fb5a-106">Toutefois, la colonne conditionnelle ne fait pas partie de la clé de l’index, elle contrôle uniquement la présence de l’entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="8fb5a-106">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8fb5a-107">Hiérarchie d’héritage</span><span class="sxs-lookup"><span data-stu-id="8fb5a-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="8fb5a-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="8fb5a-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="8fb5a-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8fb5a-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span></span>  

<span data-ttu-id="8fb5a-110">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8fb5a-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8fb5a-111">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8fb5a-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb5a-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fb5a-112">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_CONDITIONALCOLUMN _
    Implements IContentEquatable(Of JET_CONDITIONALCOLUMN), IDeepCloneable(Of JET_CONDITIONALCOLUMN)
'Usage
Dim instance As JET_CONDITIONALCOLUMN
```

``` csharp
[SerializableAttribute]
public sealed class JET_CONDITIONALCOLUMN : IContentEquatable<JET_CONDITIONALCOLUMN>, 
    IDeepCloneable<JET_CONDITIONALCOLUMN>
```

## <a name="thread-safety"></a><span data-ttu-id="8fb5a-113">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="8fb5a-113">Thread safety</span></span>

<span data-ttu-id="8fb5a-114">Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8fb5a-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8fb5a-115">Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8fb5a-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fb5a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fb5a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8fb5a-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8fb5a-117">Reference</span></span>

[<span data-ttu-id="8fb5a-118">Membres JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8fb5a-118">JET_CONDITIONALCOLUMN members</span></span>](./jet-conditionalcolumn-members.md)

[<span data-ttu-id="8fb5a-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8fb5a-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
