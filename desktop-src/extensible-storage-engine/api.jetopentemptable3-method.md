---
description: 'En savoir plus sur : méthode API. JetOpenTempTable3'
title: Méthode Api.JetOpenTempTable3
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534136"
---
# <a name="apijetopentemptable3-method"></a><span data-ttu-id="9baa6-103">Méthode Api.JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="9baa6-103">Api.JetOpenTempTable3 method</span></span>

<span data-ttu-id="9baa6-104">Crée une table temporaire avec un index unique.</span><span class="sxs-lookup"><span data-stu-id="9baa6-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="9baa6-105">Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="9baa6-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="9baa6-106">Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="9baa6-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="9baa6-107">Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="9baa6-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="9baa6-108">Consultez également [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="9baa6-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="9baa6-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9baa6-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9baa6-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9baa6-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9baa6-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9baa6-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="9baa6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9baa6-112">Parameters</span></span>

  - <span data-ttu-id="9baa6-113">sesid</span><span class="sxs-lookup"><span data-stu-id="9baa6-113">sesid</span></span>  
    <span data-ttu-id="9baa6-114">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9baa6-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9baa6-115">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9baa6-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9baa6-116">colonnes</span><span class="sxs-lookup"><span data-stu-id="9baa6-116">columns</span></span>  
    <span data-ttu-id="9baa6-117">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="9baa6-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="9baa6-118">Définitions de colonne pour les colonnes créées dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="9baa6-118">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="9baa6-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="9baa6-119">numColumns</span></span>  
    <span data-ttu-id="9baa6-120">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9baa6-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9baa6-121">Nombre de définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="9baa6-121">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="9baa6-122">unicodeindex</span><span class="sxs-lookup"><span data-stu-id="9baa6-122">unicodeindex</span></span>  
    <span data-ttu-id="9baa6-123">Type : [Microsoft.ISAM.esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="9baa6-123">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  
    
    <span data-ttu-id="9baa6-124">ID de paramètres régionaux et indicateurs de normalisation qui seront utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="9baa6-124">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="9baa6-125">Si ce n’est pas le cas, les options par défaut sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="9baa6-125">When this is not present then the default options are used.</span></span>

<!-- end list -->

  - <span data-ttu-id="9baa6-126">grbit</span><span class="sxs-lookup"><span data-stu-id="9baa6-126">grbit</span></span>  
    <span data-ttu-id="9baa6-127">Type : [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9baa6-127">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9baa6-128">Options de création de table.</span><span class="sxs-lookup"><span data-stu-id="9baa6-128">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="9baa6-129">TableID</span><span class="sxs-lookup"><span data-stu-id="9baa6-129">tableid</span></span>  
    <span data-ttu-id="9baa6-130">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9baa6-130">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9baa6-131">Retourne l’TableID de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="9baa6-131">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="9baa6-132">La fermeture de ce TableID avec [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libère les ressources associées à la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="9baa6-132">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="9baa6-133">columnids</span><span class="sxs-lookup"><span data-stu-id="9baa6-133">columnids</span></span>  
    <span data-ttu-id="9baa6-134">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="9baa6-134">Type: \[\]</span></span>  
    
    <span data-ttu-id="9baa6-135">Mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés au cours de la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="9baa6-135">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="9baa6-136">Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="9baa6-136">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="9baa6-137">Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9baa6-137">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="9baa6-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9baa6-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9baa6-139">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9baa6-139">Reference</span></span>

[<span data-ttu-id="9baa6-140">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="9baa6-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9baa6-141">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="9baa6-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9baa6-142">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9baa6-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
