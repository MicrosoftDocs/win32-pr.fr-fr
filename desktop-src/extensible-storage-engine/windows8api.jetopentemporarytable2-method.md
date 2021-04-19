---
description: 'En savoir plus sur : méthode Windows8Api. JetOpenTemporaryTable2'
title: Méthode Windows8Api. JetOpenTemporaryTable2 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetOpenTemporaryTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetopentemporarytable2(v=EXCHG.10)
ms:contentKeyID: 55107829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ebb96af18e655c9f9304e2fe7a339663c0206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521442"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="8e282-103">Méthode Windows8Api. JetOpenTemporaryTable2</span><span class="sxs-lookup"><span data-stu-id="8e282-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="8e282-104">Crée une table temporaire avec un index unique.</span><span class="sxs-lookup"><span data-stu-id="8e282-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="8e282-105">Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="8e282-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="8e282-106">Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="8e282-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="8e282-107">Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="8e282-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="8e282-108">Consultez également [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), "API. JetOpenTempTable2", [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="8e282-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="8e282-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="8e282-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="8e282-110">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e282-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="8e282-111">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8e282-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e282-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e282-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable2 ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEWindows8Api.JetOpenTemporaryTable2(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable2(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="8e282-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e282-113">Parameters</span></span>

  - <span data-ttu-id="8e282-114">sesid</span><span class="sxs-lookup"><span data-stu-id="8e282-114">sesid</span></span>  
    <span data-ttu-id="8e282-115">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e282-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8e282-116">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8e282-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e282-117">temporarytable</span><span class="sxs-lookup"><span data-stu-id="8e282-117">temporarytable</span></span>  
    <span data-ttu-id="8e282-118">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="8e282-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="8e282-119">Description de la table temporaire à créer en entrée.</span><span class="sxs-lookup"><span data-stu-id="8e282-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="8e282-120">Après un appel réussi, la structure contient le handle vers les identifications de la table et de la colonne temporaires.</span><span class="sxs-lookup"><span data-stu-id="8e282-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="8e282-121">Utilisez [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) pour libérer la table temporaire lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="8e282-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e282-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8e282-122">Remarks</span></span>

<span data-ttu-id="8e282-123">Utilisez [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) pour les versions antérieures d’esent.</span><span class="sxs-lookup"><span data-stu-id="8e282-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e282-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e282-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e282-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="8e282-125">Reference</span></span>

[<span data-ttu-id="8e282-126">Windows8Api, classe</span><span class="sxs-lookup"><span data-stu-id="8e282-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="8e282-127">Membres Windows8Api</span><span class="sxs-lookup"><span data-stu-id="8e282-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="8e282-128">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="8e282-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
