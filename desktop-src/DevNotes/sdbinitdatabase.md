---
description: Ouvre la base de données de shims.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: SdbInitDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482896"
---
# <a name="sdbinitdatabase-function"></a><span data-ttu-id="53c4f-103">SdbInitDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="53c4f-103">SdbInitDatabase function</span></span>

<span data-ttu-id="53c4f-104">Ouvre la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="53c4f-104">Opens the shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c4f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53c4f-105">Syntax</span></span>


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="53c4f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53c4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c4f-107">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53c4f-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53c4f-108">Ce paramètre spécifie le format du chemin d’accès dans le paramètre *pszDatabasePath* .</span><span class="sxs-lookup"><span data-stu-id="53c4f-108">This parameter specifies the format of the path in the *pszDatabasePath* parameter.</span></span> <span data-ttu-id="53c4f-109">Il peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="53c4f-109">It can be one of the following values.</span></span>



| <span data-ttu-id="53c4f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="53c4f-110">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="53c4f-111">Signification</span><span class="sxs-lookup"><span data-stu-id="53c4f-111">Meaning</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <span data-ttu-id="53c4f-112"><dt>**HID \_ \_Chemins dos**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="53c4f-112"><dt>**HID\_DOS\_PATHS**</dt> <dt>0x00000001</dt></span></span> </dl>                             | <span data-ttu-id="53c4f-113">Un chemin d’accès de style MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="53c4f-113">An MS-DOS style path.</span></span><br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <span data-ttu-id="53c4f-114"><dt>**HID \_ BASE de données \_ FullPath**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="53c4f-114"><dt>**HID\_DATABASE\_FULLPATH**</dt> <dt>0x00000002</dt></span></span> </dl>     | <span data-ttu-id="53c4f-115">Chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="53c4f-115">A full path.</span></span><br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <span data-ttu-id="53c4f-116"><dt>**HID \_ AUCUNE \_ base de données**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="53c4f-116"><dt>**HID\_NO\_DATABASE**</dt> <dt>0x00000004</dt></span></span> </dl>                       | <span data-ttu-id="53c4f-117">Le paramètre *pszDatabasePath* est ignoré et aucune base de données n’est ouverte.</span><span class="sxs-lookup"><span data-stu-id="53c4f-117">The *pszDatabasePath* parameter is ignored and no database is opened.</span></span><br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <span data-ttu-id="53c4f-118"><dt>**HID \_ \_ \_ Masque de type de base de données**</dt> <dt>0xF00F0000</dt></span><span class="sxs-lookup"><span data-stu-id="53c4f-118"><dt>**HID\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF00F0000</dt></span></span> </dl> | <span data-ttu-id="53c4f-119">Ce paramètre spécifie une base de données prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="53c4f-119">This parameter specifies a predefined database.</span></span> <span data-ttu-id="53c4f-120">Le paramètre *pszDatabasePath* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="53c4f-120">The *pszDatabasePath* parameter is ignored.</span></span><br/> |



 

<span data-ttu-id="53c4f-121">Si *dwFlags* contient **un \_ \_ \_ masque de type de données HID**, ce paramètre peut également inclure l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="53c4f-121">If *dwFlags* contains **HID\_DATA\_TYPE\_MASK**, this parameter can also include one of the following values.</span></span>



| <span data-ttu-id="53c4f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="53c4f-122">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="53c4f-123">Signification</span><span class="sxs-lookup"><span data-stu-id="53c4f-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="53c4f-124"><dt>**Sdb \_ 0x80030000 \_ de \_ shim principal de base de données**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="53c4f-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt> <dt>0x80030000</dt></span></span> </dl>          | <span data-ttu-id="53c4f-125">Base de données de shims d’application.</span><span class="sxs-lookup"><span data-stu-id="53c4f-125">Application shim database.</span></span><br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="53c4f-126"><dt>**Sdb \_ BASE de données \_ principale \_ MSI**</dt> <dt>0x80020000</dt></span><span class="sxs-lookup"><span data-stu-id="53c4f-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt> <dt>0x80020000</dt></span></span> </dl>             | <span data-ttu-id="53c4f-127">Base de données MSI.</span><span class="sxs-lookup"><span data-stu-id="53c4f-127">MSI database.</span></span><br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="53c4f-128"><dt>**Sdb \_ \_ \_ Pilotes principaux de base de données**</dt> <dt>0x80040000</dt></span><span class="sxs-lookup"><span data-stu-id="53c4f-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt> <dt>0x80040000</dt></span></span> </dl> | <span data-ttu-id="53c4f-129">Base de données des pilotes à bloquer.</span><span class="sxs-lookup"><span data-stu-id="53c4f-129">Database of drivers to be blocked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53c4f-130">*pszDatabasePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53c4f-130">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53c4f-131">Chemin d’accès à la base de données.</span><span class="sxs-lookup"><span data-stu-id="53c4f-131">The path to the database.</span></span> <span data-ttu-id="53c4f-132">Ce paramètre peut avoir la **valeur null** si le paramètre *dwFlags* spécifie une base de données prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="53c4f-132">This parameter can be **NULL** if the *dwFlags* parameter specifies a predefined database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c4f-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53c4f-133">Return value</span></span>

<span data-ttu-id="53c4f-134">La fonction retourne un descripteur à la base de données ouverte.</span><span class="sxs-lookup"><span data-stu-id="53c4f-134">The function returns a handle to the opened database.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c4f-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53c4f-135">Requirements</span></span>



| <span data-ttu-id="53c4f-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53c4f-136">Requirement</span></span> | <span data-ttu-id="53c4f-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="53c4f-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53c4f-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53c4f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="53c4f-139">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53c4f-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="53c4f-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53c4f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="53c4f-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53c4f-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="53c4f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="53c4f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53c4f-143"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53c4f-143"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c4f-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53c4f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c4f-145">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="53c4f-145">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
</dt> <dt>

[<span data-ttu-id="53c4f-146">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="53c4f-146">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="53c4f-147">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="53c4f-147">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> <dt>

[<span data-ttu-id="53c4f-148">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="53c4f-148">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




