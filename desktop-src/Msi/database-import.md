---
description: La méthode Import de l’objet Database importe une table de base de données à partir d’un fichier d’archive de texte, en supprimant toute table existante.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Database. Import, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539651"
---
# <a name="databaseimport-method"></a><span data-ttu-id="eec27-103">Database. Import, méthode</span><span class="sxs-lookup"><span data-stu-id="eec27-103">Database.Import method</span></span>

<span data-ttu-id="eec27-104">La méthode **Import** de l’objet [**Database**](database-object.md) importe une table de base de données à partir d’un fichier d' [Archive de texte](text-archive-files.md), en supprimant toute table existante.</span><span class="sxs-lookup"><span data-stu-id="eec27-104">The **Import** method of the [**Database**](database-object.md) object imports a database table from a [text archive files](text-archive-files.md), dropping any existing table.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eec27-105">Syntax</span></span>


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="eec27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eec27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec27-107">*path*</span><span class="sxs-lookup"><span data-stu-id="eec27-107">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="eec27-108">Dossier requis dans lequel se trouve le fichier texte.</span><span class="sxs-lookup"><span data-stu-id="eec27-108">Required folder where the text file is present.</span></span>

</dd> <dt>

<span data-ttu-id="eec27-109">*file*</span><span class="sxs-lookup"><span data-stu-id="eec27-109">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="eec27-110">Nom requis du fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="eec27-110">Required name of the file to be imported.</span></span> <span data-ttu-id="eec27-111">Cela n’inclut pas le dossier, car il doit être défini dans l’objet Path.</span><span class="sxs-lookup"><span data-stu-id="eec27-111">This does not include the folder, as that must be set in the path object.</span></span> <span data-ttu-id="eec27-112">Le nom de la table est spécifié dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="eec27-112">The table name is specified within the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec27-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eec27-113">Return value</span></span>

<span data-ttu-id="eec27-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="eec27-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec27-115">Notes</span><span class="sxs-lookup"><span data-stu-id="eec27-115">Remarks</span></span>

<span data-ttu-id="eec27-116">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="eec27-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec27-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eec27-117">Requirements</span></span>



| <span data-ttu-id="eec27-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eec27-118">Requirement</span></span> | <span data-ttu-id="eec27-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="eec27-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec27-120">Version</span><span class="sxs-lookup"><span data-stu-id="eec27-120">Version</span></span><br/> | <span data-ttu-id="eec27-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eec27-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eec27-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eec27-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eec27-123">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="eec27-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="eec27-124">DLL</span><span class="sxs-lookup"><span data-stu-id="eec27-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="eec27-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eec27-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="eec27-126">IID</span><span class="sxs-lookup"><span data-stu-id="eec27-126">IID</span></span><br/>     | <span data-ttu-id="eec27-127">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="eec27-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="eec27-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eec27-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec27-129">**Base de données**</span><span class="sxs-lookup"><span data-stu-id="eec27-129">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="eec27-130">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="eec27-130">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




