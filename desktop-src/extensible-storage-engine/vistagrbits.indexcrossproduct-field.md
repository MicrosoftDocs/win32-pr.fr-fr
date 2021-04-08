---
description: 'En savoir plus sur : champ VistaGrbits. IndexCrossProduct'
title: Champ VistaGrbits. IndexCrossProduct (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1b16f741c63d455d18a887331505080aef62990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953201"
---
# <a name="vistagrbitsindexcrossproduct-field"></a><span data-ttu-id="55686-103">Champ VistaGrbits. IndexCrossProduct</span><span class="sxs-lookup"><span data-stu-id="55686-103">VistaGrbits.IndexCrossProduct field</span></span>

<span data-ttu-id="55686-104">La spécification de cet indicateur pour un index qui a plusieurs colonnes clés qui est une colonne à plusieurs valeurs entraîne la création d’une entrée d’index pour chaque résultat d’un produit croisé de toutes les valeurs dans ces colonnes clés.</span><span class="sxs-lookup"><span data-stu-id="55686-104">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="55686-105">Dans le cas contraire, l’index comporte une seule entrée pour chaque valeur multiple dans la colonne clé la plus significative qui est une colonne à valeurs multiples et chacune de ces entrées d’index utilise la première valeur multiple de toutes les autres colonnes clés qui sont des colonnes à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="55686-105">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="55686-106">Par exemple, si vous avez spécifié cet indicateur pour un index sur la colonne a qui a les valeurs « Red » et « Blue » et sur la colonne B qui a les valeurs « 1 » et « 2 », les entrées d’index suivantes sont créées : « Red », « 1 »; « Red », « 2 »; "Blue", "1"; « Blue », « 2 ».</span><span class="sxs-lookup"><span data-stu-id="55686-106">For example, if you specified this flag for an index over column A that has the values "red" and "blue" and over column B that has the values "1" and "2" then the following index entries would be created: "red", "1"; "red", "2"; "blue", "1"; "blue", "2".</span></span> <span data-ttu-id="55686-107">Dans le cas contraire, les entrées d’index suivantes sont créées : « Red », « 1 »; « Blue », « 1 ».</span><span class="sxs-lookup"><span data-stu-id="55686-107">Otherwise, the following index entries would be created: "red", "1"; "blue", "1".</span></span>

<span data-ttu-id="55686-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55686-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="55686-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55686-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55686-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55686-110">Syntax</span></span>

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a><span data-ttu-id="55686-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55686-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55686-112">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="55686-112">Reference</span></span>

[<span data-ttu-id="55686-113">VistaGrbits, classe</span><span class="sxs-lookup"><span data-stu-id="55686-113">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="55686-114">Membres VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="55686-114">VistaGrbits members</span></span>](./vistagrbits-members.md)

[<span data-ttu-id="55686-115">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="55686-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
