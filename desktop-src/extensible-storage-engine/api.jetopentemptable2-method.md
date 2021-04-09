---
description: 'En savoir plus sur : méthode API. JetOpenTempTable2'
title: API. JetOpenTempTable2, méthode
TOCTitle: 'JetOpenTempTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable2(v=EXCHG.10)
ms:contentKeyID: 55100777
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fd3f0e04db6519fbcaa1c2d2fa9060d2d993d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210528"
---
# <a name="apijetopentemptable2-method"></a><span data-ttu-id="06564-103">API. JetOpenTempTable2, méthode</span><span class="sxs-lookup"><span data-stu-id="06564-103">Api.JetOpenTempTable2 method</span></span>

<span data-ttu-id="06564-104">Crée une table temporaire avec un index unique.</span><span class="sxs-lookup"><span data-stu-id="06564-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="06564-105">Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="06564-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="06564-106">Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="06564-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="06564-107">Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="06564-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="06564-108">Consultez également [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="06564-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="06564-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="06564-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="06564-110">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="06564-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="06564-111">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="06564-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="06564-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06564-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable2 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    lcid As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim lcid As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable2(sesid, columns, _
    numColumns, lcid, grbit, tableid, _
    columnids)
```

``` csharp
public static void JetOpenTempTable2(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    int lcid,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="06564-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06564-113">Parameters</span></span>

  - <span data-ttu-id="06564-114">sesid</span><span class="sxs-lookup"><span data-stu-id="06564-114">sesid</span></span>  
    <span data-ttu-id="06564-115">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="06564-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="06564-116">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="06564-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="06564-117">colonnes</span><span class="sxs-lookup"><span data-stu-id="06564-117">columns</span></span>  
    <span data-ttu-id="06564-118">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="06564-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="06564-119">Définitions de colonne pour les colonnes créées dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="06564-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="06564-120">numColumns</span><span class="sxs-lookup"><span data-stu-id="06564-120">numColumns</span></span>  
    <span data-ttu-id="06564-121">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="06564-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="06564-122">Nombre de définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="06564-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="06564-123">lcid</span><span class="sxs-lookup"><span data-stu-id="06564-123">lcid</span></span>  
    <span data-ttu-id="06564-124">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="06564-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="06564-125">ID de paramètres régionaux à utiliser pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="06564-125">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="06564-126">Les paramètres régionaux peuvent être utilisés tant que le module linguistique approprié a été installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="06564-126">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span>

<!-- end list -->

  - <span data-ttu-id="06564-127">grbit</span><span class="sxs-lookup"><span data-stu-id="06564-127">grbit</span></span>  
    <span data-ttu-id="06564-128">Type : [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="06564-128">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="06564-129">Options de création de table.</span><span class="sxs-lookup"><span data-stu-id="06564-129">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="06564-130">TableID</span><span class="sxs-lookup"><span data-stu-id="06564-130">tableid</span></span>  
    <span data-ttu-id="06564-131">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="06564-131">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="06564-132">Retourne l’TableID de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="06564-132">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="06564-133">La fermeture de ce TableID avec [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libère les ressources associées à la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="06564-133">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="06564-134">columnids</span><span class="sxs-lookup"><span data-stu-id="06564-134">columnids</span></span>  
    <span data-ttu-id="06564-135">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="06564-135">Type: \[\]</span></span>  
    
    <span data-ttu-id="06564-136">Mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés au cours de la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="06564-136">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="06564-137">Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="06564-137">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="06564-138">Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.</span><span class="sxs-lookup"><span data-stu-id="06564-138">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="06564-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06564-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="06564-140">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="06564-140">Reference</span></span>

[<span data-ttu-id="06564-141">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="06564-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="06564-142">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="06564-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="06564-143">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="06564-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
