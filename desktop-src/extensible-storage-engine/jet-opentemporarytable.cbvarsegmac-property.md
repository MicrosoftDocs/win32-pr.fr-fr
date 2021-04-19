---
description: 'En savoir plus sur : propriété JET_OPENTEMPORARYTABLE. cbVarSegMac'
title: JET_OPENTEMPORARYTABLE. cbVarSegMac, propriété (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'cbVarSegMac property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbvarsegmac(v=EXCHG.10)
ms:contentKeyID: 55104115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbVarSegMac
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37fe218a9741235410d2452f04f082dc6673eaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531984"
---
# <a name="jet_opentemporarytablecbvarsegmac-property"></a><span data-ttu-id="cb92b-103">JET_OPENTEMPORARYTABLE. cbVarSegMac, propriété</span><span class="sxs-lookup"><span data-stu-id="cb92b-103">JET_OPENTEMPORARYTABLE.cbVarSegMac property</span></span>

<span data-ttu-id="cb92b-104">Obtient ou définit la quantité maximale de données qui seront utilisées à partir de n’importe quelle variable lengthcolumn pour construire une clé pour une ligne donnée.</span><span class="sxs-lookup"><span data-stu-id="cb92b-104">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="cb92b-105">Ce paramètre peut être utilisé pour contrôler la quantité d’espace clé consommée par une colonne clé donnée.</span><span class="sxs-lookup"><span data-stu-id="cb92b-105">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="cb92b-106">Cette limite est en octets.</span><span class="sxs-lookup"><span data-stu-id="cb92b-106">This limit is in bytes.</span></span> <span data-ttu-id="cb92b-107">Si ce paramètre est égal à zéro ou est identique à la propriété [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) , aucune limite n’est appliquée.</span><span class="sxs-lookup"><span data-stu-id="cb92b-107">If this parameter is zero or is the same as the [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) property then no limit is in effect.</span></span>

<span data-ttu-id="cb92b-108">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb92b-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="cb92b-109">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb92b-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb92b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb92b-110">Syntax</span></span>

``` vb
'Declaration
Public Property cbVarSegMac As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbVarSegMac

instance.cbVarSegMac = value
```

``` csharp
public int cbVarSegMac { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="cb92b-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cb92b-111">Property value</span></span>

<span data-ttu-id="cb92b-112">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cb92b-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="cb92b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb92b-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb92b-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="cb92b-114">Reference</span></span>

[<span data-ttu-id="cb92b-115">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="cb92b-115">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="cb92b-116">Membres JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="cb92b-116">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="cb92b-117">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="cb92b-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
