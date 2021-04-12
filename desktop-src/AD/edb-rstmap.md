---
title: Structure EDB_RSTMAP (ntdsbcli. h)
description: Utilisé avec la fonction DsRestoreRegister pour mapper une base de données sauvegardée à une nouvelle base de données.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP structure Active Directory
- Pointeur de structure PEDB_RSTMAP Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032977"
---
# <a name="edb_rstmap-structure"></a><span data-ttu-id="10cef-105">\_Structure RSTMAP edb</span><span class="sxs-lookup"><span data-stu-id="10cef-105">EDB\_RSTMAP structure</span></span>

<span data-ttu-id="10cef-106">La **structure \_ RSTMAP edb** est utilisée avec la fonction [**DsRestoreRegister**](dsrestoreregister.md) pour mapper une base de données sauvegardée à une nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="10cef-106">The **EDB\_RSTMAP** structure is used with the [**DsRestoreRegister**](dsrestoreregister.md) function to map a backed up database to a new database.</span></span>

## <a name="syntax"></a><span data-ttu-id="10cef-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10cef-107">Syntax</span></span>


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a><span data-ttu-id="10cef-108">Membres</span><span class="sxs-lookup"><span data-stu-id="10cef-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="10cef-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="10cef-109">**szDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="10cef-110">Pointeur vers une chaîne se terminant par un caractère null qui contient le nom de la base de données lors de sa sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="10cef-110">Pointer to a null-terminated string that contains the name of the database when it was backed up.</span></span>

</dd> <dt>

<span data-ttu-id="10cef-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="10cef-111">**szNewDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="10cef-112">Pointeur vers une chaîne se terminant par un caractère null qui contient le nouveau nom de la base de données, y compris son nouvel emplacement, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="10cef-112">Pointer to a null-terminated string that contains the new name of the database, including its new location, when applicable.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10cef-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10cef-113">Requirements</span></span>



| <span data-ttu-id="10cef-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10cef-114">Requirement</span></span> | <span data-ttu-id="10cef-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="10cef-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10cef-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10cef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="10cef-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10cef-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="10cef-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10cef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="10cef-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10cef-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="10cef-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="10cef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="10cef-121"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="10cef-121"><dt>Ntdsbcli.h</dt></span></span> </dl> |
| <span data-ttu-id="10cef-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="10cef-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="10cef-123">**Edb \_ RSTMAPW** (Unicode) et **edb \_ RSTMAPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="10cef-123">**EDB\_RSTMAPW** (Unicode) and **EDB\_RSTMAPA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="10cef-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10cef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10cef-125">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="10cef-125">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="10cef-126">Structures de sauvegarde d’annuaire</span><span class="sxs-lookup"><span data-stu-id="10cef-126">Directory Backup Structures</span></span>](directory-backup-structures.md)
</dt> </dl>

 

 





