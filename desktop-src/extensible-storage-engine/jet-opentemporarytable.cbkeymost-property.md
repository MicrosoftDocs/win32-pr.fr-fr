---
description: 'En savoir plus sur : propriété JET_OPENTEMPORARYTABLE. cbKeyMost'
title: JET_OPENTEMPORARYTABLE. cbKeyMost, propriété (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e608d1419cd381c507874bf1f1c334d192ae2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534118"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a><span data-ttu-id="68926-103">JET_OPENTEMPORARYTABLE. cbKeyMost, propriété</span><span class="sxs-lookup"><span data-stu-id="68926-103">JET_OPENTEMPORARYTABLE.cbKeyMost property</span></span>

<span data-ttu-id="68926-104">Obtient ou définit la taille maximale d’une clé représentant une ligne donnée.</span><span class="sxs-lookup"><span data-stu-id="68926-104">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="68926-105">La taille de clé maximale peut être définie pour contrôler la façon dont les clés sont tronquées.</span><span class="sxs-lookup"><span data-stu-id="68926-105">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="68926-106">La troncation de clé est importante, car elle peut affecter le moment où les lignes sont considérées comme distinctes.</span><span class="sxs-lookup"><span data-stu-id="68926-106">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="68926-107">Si ce paramètre a la valeur 0 ou 255, la taille maximale de la clé et sa sémantique restent identiques à la taille de clé maximale prise en charge par Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="68926-107">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="68926-108">Ce paramètre peut également être défini sur une valeur supérieure en fonction de la taille de page de la base de données pour l’instance [DatabasePageSize](./jet-param-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="68926-108">This parameter may also be set to a larger value as a function of the database page size for the instance [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="68926-109">Pour [plus](./vistaparam.keymost-field.md) d’informations, consultez.</span><span class="sxs-lookup"><span data-stu-id="68926-109">See [KeyMost](./vistaparam.keymost-field.md) for more information.</span></span>

<span data-ttu-id="68926-110">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68926-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="68926-111">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="68926-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68926-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68926-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="68926-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="68926-113">Property value</span></span>

<span data-ttu-id="68926-114">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="68926-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="68926-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68926-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68926-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="68926-116">Reference</span></span>

[<span data-ttu-id="68926-117">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="68926-117">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="68926-118">Membres JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="68926-118">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="68926-119">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="68926-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
