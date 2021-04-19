---
description: 'En savoir plus sur : méthode API. JetRetrieveColumns'
title: API. JetRetrieveColumns, méthode
TOCTitle: 'JetRetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100797
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3fd4db2ce8cbcad5f74db7d4c95363aa68e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517468"
---
# <a name="apijetretrievecolumns-method"></a><span data-ttu-id="a85bf-103">API. JetRetrieveColumns, méthode</span><span class="sxs-lookup"><span data-stu-id="a85bf-103">Api.JetRetrieveColumns method</span></span>

<span data-ttu-id="a85bf-104">Récupère plusieurs valeurs de colonne de l’enregistrement actuel en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="a85bf-104">Retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="a85bf-105">Un tableau de structures de JET_RETRIEVECOLUMN est utilisé pour décrire l’ensemble des valeurs de colonne à récupérer et pour décrire les mémoires tampons de sortie pour chaque valeur de colonne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="a85bf-105">An array of JET_RETRIEVECOLUMN structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

<span data-ttu-id="a85bf-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a85bf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a85bf-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a85bf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a85bf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a85bf-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    retrievecolumns As JET_RETRIEVECOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim retrievecolumns As JET_RETRIEVECOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumns(sesid, _
    tableid, retrievecolumns, numColumns)
```

``` csharp
public static JET_wrn JetRetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RETRIEVECOLUMN[] retrievecolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="a85bf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a85bf-109">Parameters</span></span>

  - <span data-ttu-id="a85bf-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a85bf-110">sesid</span></span>  
    <span data-ttu-id="a85bf-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a85bf-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a85bf-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a85bf-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a85bf-113">TableID</span><span class="sxs-lookup"><span data-stu-id="a85bf-113">tableid</span></span>  
    <span data-ttu-id="a85bf-114">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a85bf-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a85bf-115">Curseur à partir duquel récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="a85bf-115">The cursor to retrieve the data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="a85bf-116">retrievecolumns</span><span class="sxs-lookup"><span data-stu-id="a85bf-116">retrievecolumns</span></span>  
    <span data-ttu-id="a85bf-117">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="a85bf-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="a85bf-118">Tableau d’un ou plusieurs objets [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) décrivant les données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="a85bf-118">An array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) objects describing the data to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="a85bf-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="a85bf-119">numColumns</span></span>  
    <span data-ttu-id="a85bf-120">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a85bf-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a85bf-121">Nombre d’entrées dans le tableau de colonnes.</span><span class="sxs-lookup"><span data-stu-id="a85bf-121">The number of entries in the columns array.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a85bf-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a85bf-122">Return value</span></span>

<span data-ttu-id="a85bf-123">Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a85bf-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="a85bf-124">Si une colonne Récupérée est tronquée en raison d’une mémoire tampon de longueur insuffisante, l’API retourne [BufferTruncated](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="a85bf-124">If any column retrieved is truncated due to an insufficient length buffer, then the API will return [BufferTruncated](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="a85bf-125">Toutefois, d’autres erreurs JET_wrnColumnNull sont retournées uniquement dans le champ d’erreur de l’objet [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) .</span><span class="sxs-lookup"><span data-stu-id="a85bf-125">However other errors JET_wrnColumnNull are returned only in the error field of the [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) object.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a85bf-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a85bf-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a85bf-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a85bf-127">Reference</span></span>

[<span data-ttu-id="a85bf-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="a85bf-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a85bf-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="a85bf-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a85bf-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a85bf-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
