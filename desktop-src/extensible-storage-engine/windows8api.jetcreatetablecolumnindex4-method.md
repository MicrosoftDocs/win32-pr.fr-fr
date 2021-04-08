---
description: 'En savoir plus sur : méthode Windows8Api. JetCreateTableColumnIndex4'
title: Méthode Windows8Api. JetCreateTableColumnIndex4 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetCreateTableColumnIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateTableColumnIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreatetablecolumnindex4(v=EXCHG.10)
ms:contentKeyID: 55107827
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateTableColumnIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateTableColumnIndex4
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1551c3e243ef45b7f261fd01a6b1c7926478437d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753636"
---
# <a name="windows8apijetcreatetablecolumnindex4-method"></a><span data-ttu-id="a5df2-103">Méthode Windows8Api. JetCreateTableColumnIndex4</span><span class="sxs-lookup"><span data-stu-id="a5df2-103">Windows8Api.JetCreateTableColumnIndex4 method</span></span>

<span data-ttu-id="a5df2-104">Crée une table, ajoute des colonnes et des index sur cette table.</span><span class="sxs-lookup"><span data-stu-id="a5df2-104">Creates a table, adds columns, and indices on that table.</span></span> [<span data-ttu-id="a5df2-105">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</span><span class="sxs-lookup"><span data-stu-id="a5df2-105">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</span></span>](./api.jetcreatetablecolumnindex3-method.md)

<span data-ttu-id="a5df2-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a5df2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="a5df2-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a5df2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a5df2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5df2-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTableColumnIndex4 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablecreate As JET_TABLECREATE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablecreate As JET_TABLECREATEWindows8Api.JetCreateTableColumnIndex4(sesid, _
    dbid, tablecreate)
```

``` csharp
public static void JetCreateTableColumnIndex4(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLECREATE tablecreate
)
```

#### <a name="parameters"></a><span data-ttu-id="a5df2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5df2-109">Parameters</span></span>

  - <span data-ttu-id="a5df2-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a5df2-110">sesid</span></span>  
    <span data-ttu-id="a5df2-111">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a5df2-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a5df2-112">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a5df2-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a5df2-113">dbid</span><span class="sxs-lookup"><span data-stu-id="a5df2-113">dbid</span></span>  
    <span data-ttu-id="a5df2-114">Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a5df2-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="a5df2-115">Base de données à laquelle ajouter la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="a5df2-115">The database to which to add the new table.</span></span>

<!-- end list -->

  - <span data-ttu-id="a5df2-116">tablecreate</span><span class="sxs-lookup"><span data-stu-id="a5df2-116">tablecreate</span></span>  
    <span data-ttu-id="a5df2-117">Type : [Microsoft.ISAM.esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="a5df2-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span></span>  
    
    <span data-ttu-id="a5df2-118">Objet décrivant la table à créer.</span><span class="sxs-lookup"><span data-stu-id="a5df2-118">Object describing the table to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5df2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5df2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a5df2-120">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a5df2-120">Reference</span></span>

[<span data-ttu-id="a5df2-121">Windows8Api, classe</span><span class="sxs-lookup"><span data-stu-id="a5df2-121">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="a5df2-122">Membres Windows8Api</span><span class="sxs-lookup"><span data-stu-id="a5df2-122">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="a5df2-123">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="a5df2-123">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
