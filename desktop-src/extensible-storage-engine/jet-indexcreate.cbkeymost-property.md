---
description: 'En savoir plus sur : propriété JET_INDEXCREATE. cbKeyMost'
title: JET_INDEXCREATE. cbKeyMost, propriété
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866846"
---
# <a name="jet_indexcreatecbkeymost-property"></a><span data-ttu-id="16c52-103">JET_INDEXCREATE. cbKeyMost, propriété</span><span class="sxs-lookup"><span data-stu-id="16c52-103">JET_INDEXCREATE.cbKeyMost property</span></span>

<span data-ttu-id="16c52-104">Obtient ou définit la taille maximale autorisée, en octets, pour les clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="16c52-104">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="16c52-105">La taille de clé maximale prise en charge minimale est JET_cbKeyMostMin (255) qui est la taille de clé maximale héritée.</span><span class="sxs-lookup"><span data-stu-id="16c52-105">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="16c52-106">La taille de clé maximale dépend de la taille de page de la base de données [DatabasePageSize](./jet-param-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="16c52-106">The maximum key size is dependent on the database page size [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="16c52-107">La [taille de clé](./systemparameters.keymost-property.md)maximale peut être récupérée avec.</span><span class="sxs-lookup"><span data-stu-id="16c52-107">The maximum key size can be retrieved with [KeyMost](./systemparameters.keymost-property.md).</span></span> <span data-ttu-id="16c52-108">Ce paramètre est ignoré sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="16c52-108">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="16c52-109">Contrairement à l’API non managée, **IndexKeyMost ()** (JET_bitIndexKeyMost) n’est pas nécessaire, elle est ajoutée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="16c52-109">Unlike the unmanaged API, **IndexKeyMost()** (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span>

<span data-ttu-id="16c52-110">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="16c52-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="16c52-111">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="16c52-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="16c52-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16c52-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="16c52-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="16c52-113">Property value</span></span>

<span data-ttu-id="16c52-114">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="16c52-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="16c52-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16c52-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="16c52-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="16c52-116">Reference</span></span>

[<span data-ttu-id="16c52-117">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="16c52-117">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="16c52-118">Membres JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="16c52-118">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="16c52-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="16c52-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
