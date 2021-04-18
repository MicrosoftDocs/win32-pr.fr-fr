---
description: 'En savoir plus sur : méthode API. JetOpenTempTable'
title: API. JetOpenTempTable, méthode
TOCTitle: 'JetOpenTempTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable(v=EXCHG.10)
ms:contentKeyID: 55100773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa41ce62b8bc2d7f2429acb5de809ad0be44a609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526945"
---
# <a name="apijetopentemptable-method"></a><span data-ttu-id="361c6-103">API. JetOpenTempTable, méthode</span><span class="sxs-lookup"><span data-stu-id="361c6-103">Api.JetOpenTempTable method</span></span>

<span data-ttu-id="361c6-104">Crée une table temporaire avec un index unique.</span><span class="sxs-lookup"><span data-stu-id="361c6-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="361c6-105">Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="361c6-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="361c6-106">Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="361c6-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="361c6-107">Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="361c6-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="361c6-108">Consultez également [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="361c6-108">Also see [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="361c6-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="361c6-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="361c6-110">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="361c6-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="361c6-111">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="361c6-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="361c6-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="361c6-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable(sesid, columns, _
    numColumns, grbit, tableid, columnids)
```

``` csharp
public static void JetOpenTempTable(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="361c6-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="361c6-113">Parameters</span></span>

  - <span data-ttu-id="361c6-114">sesid</span><span class="sxs-lookup"><span data-stu-id="361c6-114">sesid</span></span>  
    <span data-ttu-id="361c6-115">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="361c6-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="361c6-116">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="361c6-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="361c6-117">colonnes</span><span class="sxs-lookup"><span data-stu-id="361c6-117">columns</span></span>  
    <span data-ttu-id="361c6-118">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="361c6-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="361c6-119">Définitions de colonne pour les colonnes créées dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="361c6-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="361c6-120">numColumns</span><span class="sxs-lookup"><span data-stu-id="361c6-120">numColumns</span></span>  
    <span data-ttu-id="361c6-121">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="361c6-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="361c6-122">Nombre de définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="361c6-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="361c6-123">grbit</span><span class="sxs-lookup"><span data-stu-id="361c6-123">grbit</span></span>  
    <span data-ttu-id="361c6-124">Type : [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="361c6-124">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="361c6-125">Options de création de table.</span><span class="sxs-lookup"><span data-stu-id="361c6-125">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="361c6-126">TableID</span><span class="sxs-lookup"><span data-stu-id="361c6-126">tableid</span></span>  
    <span data-ttu-id="361c6-127">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="361c6-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="361c6-128">Retourne l’TableID de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="361c6-128">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="361c6-129">La fermeture de ce TableID avec [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libère les ressources associées à la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="361c6-129">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="361c6-130">columnids</span><span class="sxs-lookup"><span data-stu-id="361c6-130">columnids</span></span>  
    <span data-ttu-id="361c6-131">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="361c6-131">Type: \[\]</span></span>  
    
    <span data-ttu-id="361c6-132">Mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés au cours de la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="361c6-132">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="361c6-133">Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="361c6-133">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="361c6-134">Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.</span><span class="sxs-lookup"><span data-stu-id="361c6-134">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="361c6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="361c6-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="361c6-136">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="361c6-136">Reference</span></span>

[<span data-ttu-id="361c6-137">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="361c6-137">Api class</span></span>](./api-class.md)

[<span data-ttu-id="361c6-138">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="361c6-138">Api members</span></span>](./api-members.md)

[<span data-ttu-id="361c6-139">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="361c6-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
