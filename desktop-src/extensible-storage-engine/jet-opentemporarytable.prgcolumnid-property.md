---
description: 'En savoir plus sur : propriété JET_OPENTEMPORARYTABLE. prgcolumnid'
title: JET_OPENTEMPORARYTABLE. prgcolumnid, propriété (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'prgcolumnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.prgcolumnid(v=EXCHG.10)
ms:contentKeyID: 55104133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd6516e01d08de32f7962a48d2caca69ddbf0427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952932"
---
# <a name="jet_opentemporarytableprgcolumnid-property"></a><span data-ttu-id="51de1-103">JET_OPENTEMPORARYTABLE. prgcolumnid, propriété</span><span class="sxs-lookup"><span data-stu-id="51de1-103">JET_OPENTEMPORARYTABLE.prgcolumnid property</span></span>

<span data-ttu-id="51de1-104">Obtient ou définit la mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés pendant la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="51de1-104">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="51de1-105">Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="51de1-105">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="51de1-106">Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille de [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md).</span><span class="sxs-lookup"><span data-stu-id="51de1-106">As a result, the size of this buffer must correspond to the size of [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md).</span></span>

<span data-ttu-id="51de1-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="51de1-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="51de1-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="51de1-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="51de1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51de1-109">Syntax</span></span>

``` vb
'Declaration
Public Property prgcolumnid As JET_COLUMNID()
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_COLUMNID()

value = instance.prgcolumnid

instance.prgcolumnid = value
```

``` csharp
public JET_COLUMNID[] prgcolumnid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="51de1-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="51de1-110">Property value</span></span>

<span data-ttu-id="51de1-111">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="51de1-111">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="51de1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51de1-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="51de1-113">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="51de1-113">Reference</span></span>

[<span data-ttu-id="51de1-114">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="51de1-114">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="51de1-115">Membres JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="51de1-115">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="51de1-116">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="51de1-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
