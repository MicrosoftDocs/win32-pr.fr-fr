---
description: 'En savoir plus sur : propriété JET_OPENTEMPORARYTABLE. pidxunicode'
title: JET_OPENTEMPORARYTABLE. pidxunicode, propriété (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e5beb4f4523f5e6a6da37a999b6c0a2ab7b4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520757"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a><span data-ttu-id="7beb3-103">JET_OPENTEMPORARYTABLE. pidxunicode, propriété</span><span class="sxs-lookup"><span data-stu-id="7beb3-103">JET_OPENTEMPORARYTABLE.pidxunicode property</span></span>

<span data-ttu-id="7beb3-104">Obtient ou définit les indicateurs de normalisation et l’ID de paramètres régionaux à utiliser pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="7beb3-104">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="7beb3-105">Lorsque ce paramètre a la valeur null, le LCID par défaut est utilisé pour comparer les colonnes clés Unicode de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="7beb3-105">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="7beb3-106">Le LCID par défaut est le paramètre régional anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="7beb3-106">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="7beb3-107">Lorsque ce paramètre a la valeur null, les indicateurs de normalisation par défaut sont utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="7beb3-107">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="7beb3-108">Les indicateurs de normalisation par défaut sont les suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="7beb3-108">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="7beb3-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7beb3-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="7beb3-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7beb3-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7beb3-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7beb3-111">Syntax</span></span>

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="7beb3-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7beb3-112">Property value</span></span>

<span data-ttu-id="7beb3-113">Type : [Microsoft.ISAM.esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="7beb3-113">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7beb3-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7beb3-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7beb3-115">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7beb3-115">Reference</span></span>

[<span data-ttu-id="7beb3-116">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="7beb3-116">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="7beb3-117">Membres JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="7beb3-117">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="7beb3-118">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="7beb3-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
