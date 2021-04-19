---
description: La méthode OpenView de l’objet Database retourne un objet View qui représente la requête spécifiée par une chaîne SQL.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Database. OpenView, méthode (certview. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525647"
---
# <a name="databaseopenview-method"></a><span data-ttu-id="31950-103">Database. OpenView, méthode</span><span class="sxs-lookup"><span data-stu-id="31950-103">Database.OpenView method</span></span>

<span data-ttu-id="31950-104">La méthode **OpenView** de l’objet [**Database**](database-object.md) retourne un objet [**View**](view-object.md) qui représente la requête spécifiée par une chaîne SQL.</span><span class="sxs-lookup"><span data-stu-id="31950-104">The **OpenView** method of the [**Database**](database-object.md) object returns a [**View**](view-object.md) object that represents the query specified by a SQL string.</span></span>

## <a name="syntax"></a><span data-ttu-id="31950-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31950-105">Syntax</span></span>


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a><span data-ttu-id="31950-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31950-107">*sql*</span><span class="sxs-lookup"><span data-stu-id="31950-107">*sql*</span></span> 
</dt> <dd>

<span data-ttu-id="31950-108">Chaîne de requête SQL requise.</span><span class="sxs-lookup"><span data-stu-id="31950-108">Required SQL query string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31950-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31950-109">Return value</span></span>

<span data-ttu-id="31950-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="31950-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31950-111">Notes</span><span class="sxs-lookup"><span data-stu-id="31950-111">Remarks</span></span>

<span data-ttu-id="31950-112">Pour plus d’informations sur la syntaxe SQL implémentée dans le programme d’installation, consultez [syntaxe SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="31950-112">For information about SQL syntax implemented in the installer, see [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="31950-113">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="31950-113">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="31950-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31950-114">Requirements</span></span>



| <span data-ttu-id="31950-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31950-115">Requirement</span></span> | <span data-ttu-id="31950-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="31950-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31950-117">Version</span><span class="sxs-lookup"><span data-stu-id="31950-117">Version</span></span><br/> | <span data-ttu-id="31950-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="31950-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="31950-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31950-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="31950-120">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="31950-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="31950-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="31950-121">Header</span></span><br/>  | <dl> <span data-ttu-id="31950-122"><dt>Certview. h</dt></span><span class="sxs-lookup"><span data-stu-id="31950-122"><dt>Certview.h</dt></span></span> </dl>                                                                                                                                                                   |
| <span data-ttu-id="31950-123">DLL</span><span class="sxs-lookup"><span data-stu-id="31950-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="31950-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31950-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="31950-125">IID</span><span class="sxs-lookup"><span data-stu-id="31950-125">IID</span></span><br/>     | <span data-ttu-id="31950-126">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="31950-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="31950-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31950-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31950-128">**Base de données**</span><span class="sxs-lookup"><span data-stu-id="31950-128">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="31950-129">Syntaxe SQL</span><span class="sxs-lookup"><span data-stu-id="31950-129">SQL Syntax</span></span>](sql-syntax.md)
</dt> </dl>

 

 




