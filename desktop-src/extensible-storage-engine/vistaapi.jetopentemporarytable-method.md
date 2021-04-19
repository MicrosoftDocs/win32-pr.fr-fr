---
description: 'En savoir plus sur : méthode VistaApi. JetOpenTemporaryTable'
title: Méthode VistaApi. JetOpenTemporaryTable (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a261494cf8b12039371c445a4cf2124f3ec1c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521479"
---
# <a name="vistaapijetopentemporarytable-method"></a><span data-ttu-id="9486a-103">Méthode VistaApi. JetOpenTemporaryTable</span><span class="sxs-lookup"><span data-stu-id="9486a-103">VistaApi.JetOpenTemporaryTable method</span></span>

<span data-ttu-id="9486a-104">Crée une table temporaire avec un index unique.</span><span class="sxs-lookup"><span data-stu-id="9486a-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="9486a-105">Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="9486a-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="9486a-106">Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile.</span><span class="sxs-lookup"><span data-stu-id="9486a-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="9486a-107">Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.</span><span class="sxs-lookup"><span data-stu-id="9486a-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="9486a-108">Consultez également [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="9486a-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span>

<span data-ttu-id="9486a-109">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9486a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="9486a-110">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9486a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9486a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9486a-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="9486a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9486a-112">Parameters</span></span>

  - <span data-ttu-id="9486a-113">sesid</span><span class="sxs-lookup"><span data-stu-id="9486a-113">sesid</span></span>  
    <span data-ttu-id="9486a-114">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9486a-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9486a-115">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9486a-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9486a-116">temporarytable</span><span class="sxs-lookup"><span data-stu-id="9486a-116">temporarytable</span></span>  
    <span data-ttu-id="9486a-117">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="9486a-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="9486a-118">Description de la table temporaire à créer en entrée.</span><span class="sxs-lookup"><span data-stu-id="9486a-118">Description of the temporary table to create on input.</span></span> <span data-ttu-id="9486a-119">Après un appel réussi, la structure contient le handle vers les identifications de la table et de la colonne temporaires.</span><span class="sxs-lookup"><span data-stu-id="9486a-119">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="9486a-120">Utilisez [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) pour libérer la table temporaire lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="9486a-120">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="9486a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="9486a-121">Remarks</span></span>

<span data-ttu-id="9486a-122">Introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9486a-122">Introduced in Windows Vista.</span></span> <span data-ttu-id="9486a-123">Utilisez [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md) pour les versions antérieures d’esent.</span><span class="sxs-lookup"><span data-stu-id="9486a-123">Use [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="9486a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9486a-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9486a-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="9486a-125">Reference</span></span>

[<span data-ttu-id="9486a-126">VistaApi, classe</span><span class="sxs-lookup"><span data-stu-id="9486a-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="9486a-127">Membres VistaApi</span><span class="sxs-lookup"><span data-stu-id="9486a-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="9486a-128">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="9486a-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
