---
description: Représente les types de bases de données de shims principales et personnalisées.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Types de bases de données shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747676"
---
# <a name="shim-database-types"></a><span data-ttu-id="9b92b-103">Types de bases de données shim</span><span class="sxs-lookup"><span data-stu-id="9b92b-103">Shim Database Types</span></span>

<span data-ttu-id="9b92b-104">Représente les types de bases de données de shims principales et personnalisées.</span><span class="sxs-lookup"><span data-stu-id="9b92b-104">Represent the types for main and custom shim databases.</span></span>



| <span data-ttu-id="9b92b-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="9b92b-105">Constant/value</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="9b92b-106">Description</span><span class="sxs-lookup"><span data-stu-id="9b92b-106">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <span data-ttu-id="9b92b-107"><dt>**Sdb \_ BASE de données \_ principale**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-107"><dt>**SDB\_DATABASE\_MAIN**</dt> <dt>0x80000000</dt></span></span> </dl>                    | <span data-ttu-id="9b92b-108">Base de données principale.</span><span class="sxs-lookup"><span data-stu-id="9b92b-108">The main database.</span></span> <span data-ttu-id="9b92b-109">Si cet indicateur n’est pas présent, la base de données est une base de données personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9b92b-109">If this flag is not present, the database is a custom database.</span></span><br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <span data-ttu-id="9b92b-110"><dt>**Sdb \_ 0x00010000 \_ shim de base de données**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-110"><dt>**SDB\_DATABASE\_SHIM**</dt> <dt>0x00010000</dt></span></span> </dl>                    | <span data-ttu-id="9b92b-111">La base de données contient des entrées d’application à shim.</span><span class="sxs-lookup"><span data-stu-id="9b92b-111">The database contains application entries to be shimmed.</span></span><br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <span data-ttu-id="9b92b-112"><dt>**Sdb \_ BASE de données \_ MSI**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-112"><dt>**SDB\_DATABASE\_MSI**</dt> <dt>0x00020000</dt></span></span> </dl>                       | <span data-ttu-id="9b92b-113">La base de données contient des entrées MSI.</span><span class="sxs-lookup"><span data-stu-id="9b92b-113">The database contains MSI entries.</span></span><br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <span data-ttu-id="9b92b-114"><dt>**Sdb \_ \_Pilotes de base de données**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-114"><dt>**SDB\_DATABASE\_DRIVERS**</dt> <dt>0x00040000</dt></span></span> </dl>           | <span data-ttu-id="9b92b-115">La base de données contient des entrées de bloc de pilote.</span><span class="sxs-lookup"><span data-stu-id="9b92b-115">The database contains driver block entries.</span></span><br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <span data-ttu-id="9b92b-116"><dt>**Sdb \_ \_Détails de la base de données**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-116"><dt>**SDB\_DATABASE\_DETAILS**</dt> <dt>0x00080000</dt></span></span> </dl>           | <span data-ttu-id="9b92b-117">La base de données contient les détails du AppHelp.</span><span class="sxs-lookup"><span data-stu-id="9b92b-117">The database contains Apphelp details.</span></span><br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <span data-ttu-id="9b92b-118"><dt>**Sdb \_ \_ \_ Détails du SP de base de données**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-118"><dt>**SDB\_DATABASE\_SP\_DETAILS**</dt> <dt>0x00100000</dt></span></span> </dl> | <span data-ttu-id="9b92b-119">La base de données contient les détails du fournisseur de données SP.</span><span class="sxs-lookup"><span data-stu-id="9b92b-119">The database contains SP Apphelp details.</span></span><br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <span data-ttu-id="9b92b-120"><dt>**Sdb \_ \_Ressource de base de données**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-120"><dt>**SDB\_DATABASE\_RESOURCE**</dt> <dt>0x00200000</dt></span></span> </dl>        | <span data-ttu-id="9b92b-121">La DLL de ressource contient les détails du fichier AppHelp.</span><span class="sxs-lookup"><span data-stu-id="9b92b-121">The resource DLL contains Apphelp details.</span></span><br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <span data-ttu-id="9b92b-122"><dt>**Sdb \_ \_ \_ Masque de type de base de données**</dt> <dt>0xF02F0000</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-122"><dt>**SDB\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF02F0000</dt></span></span> </dl>    | <span data-ttu-id="9b92b-123">Masque utilisé pour extraire les informations de la base de données principale.</span><span class="sxs-lookup"><span data-stu-id="9b92b-123">A mask used to extract main database information.</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="9b92b-124"><dt>**\_shim principal de base de données sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt></span></span> </dl>                                                                    | <span data-ttu-id="9b92b-125">SDB \_ Database \_ shim \| sdb \_ base de données \_ MSI \| sdb base de données \_ \_ principale</span><span class="sxs-lookup"><span data-stu-id="9b92b-125">SDB\_DATABASE\_SHIM \| SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="9b92b-126"><dt>**fichier \_ \_ MSI principal de la base de données sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt></span></span> </dl>                                                                       | <span data-ttu-id="9b92b-127">SDB \_ base de données \_ MSI \| sdb \_ base de données \_ principale</span><span class="sxs-lookup"><span data-stu-id="9b92b-127">SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="9b92b-128"><dt>**\_pilotes principaux de la base de données sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt></span></span> </dl>                                                           | <span data-ttu-id="9b92b-129">SDB \_ Database \_ drivers \| sdb \_ Database \_ main</span><span class="sxs-lookup"><span data-stu-id="9b92b-129">SDB\_DATABASE\_DRIVERS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <span data-ttu-id="9b92b-130"><dt>**\_Détails principaux de la base de données sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-130"><dt>**SDB\_DATABASE\_MAIN\_DETAILS**</dt></span></span> </dl>                                                           | <span data-ttu-id="9b92b-131">\_informations de base de données sdb \_ \| sdb \_ base de données \_ principale</span><span class="sxs-lookup"><span data-stu-id="9b92b-131">SDB\_DATABASE\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <span data-ttu-id="9b92b-132"><dt>**\_Détails du \_ SP principal de la base de données sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-132"><dt>**SDB\_DATABASE\_MAIN\_SP\_DETAILS**</dt></span></span> </dl>                                                 | <span data-ttu-id="9b92b-133">SDB \_ base de données \_ SP \_ Détails \| sdb \_ base de données \_ principale</span><span class="sxs-lookup"><span data-stu-id="9b92b-133">SDB\_DATABASE\_SP\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <span data-ttu-id="9b92b-134"><dt>**\_ressource principale de base de données sdb \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b92b-134"><dt>**SDB\_DATABASE\_MAIN\_RESOURCE**</dt></span></span> </dl>                                                        | <span data-ttu-id="9b92b-135">SDB \_ Database \_ Resource \| sdb \_ Database \_ main</span><span class="sxs-lookup"><span data-stu-id="9b92b-135">SDB\_DATABASE\_RESOURCE \| SDB\_DATABASE\_MAIN</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="9b92b-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b92b-136">Requirements</span></span>



| <span data-ttu-id="9b92b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b92b-137">Requirement</span></span> | <span data-ttu-id="9b92b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b92b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9b92b-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b92b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9b92b-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b92b-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9b92b-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b92b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9b92b-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b92b-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b92b-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b92b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b92b-144">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="9b92b-144">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




