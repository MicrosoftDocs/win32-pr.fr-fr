---
description: La méthode d’exportation de l’objet de base de données copie la structure et les données d’une table spécifiée dans un fichier d’archive de texte.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Database. Export, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545413"
---
# <a name="databaseexport-method"></a><span data-ttu-id="acbb1-103">Database. Export, méthode</span><span class="sxs-lookup"><span data-stu-id="acbb1-103">Database.Export method</span></span>

<span data-ttu-id="acbb1-104">La méthode d' **exportation** de l’objet [**de base de données**](database-object.md) copie la structure et les données d’une table spécifiée dans un [fichier d’archive de texte](text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="acbb1-104">The **Export** method of the [**Database**](database-object.md) object copies the structure and data from a specified table to a [text archive file](text-archive-files.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="acbb1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acbb1-105">Syntax</span></span>


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="acbb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acbb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acbb1-107">*table*</span><span class="sxs-lookup"><span data-stu-id="acbb1-107">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="acbb1-108">Nom requis de la table de base de données.</span><span class="sxs-lookup"><span data-stu-id="acbb1-108">Required name of the database table.</span></span> <span data-ttu-id="acbb1-109">Respecte la casse si vous utilisez la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="acbb1-109">Case-sensitive if using the installer database.</span></span>

</dd> <dt>

<span data-ttu-id="acbb1-110">*path*</span><span class="sxs-lookup"><span data-stu-id="acbb1-110">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="acbb1-111">Chaîne obligatoire qui correspond au chemin d’accès au dossier dans lequel le fichier texte est placé.</span><span class="sxs-lookup"><span data-stu-id="acbb1-111">Required string that is the path to the folder where the text file is placed.</span></span>

</dd> <dt>

<span data-ttu-id="acbb1-112">*file*</span><span class="sxs-lookup"><span data-stu-id="acbb1-112">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="acbb1-113">Nom requis du fichier à créer.</span><span class="sxs-lookup"><span data-stu-id="acbb1-113">Required name of the file to be created.</span></span> <span data-ttu-id="acbb1-114">Cela n’inclut pas le dossier, car il doit être défini dans l’objet Path.</span><span class="sxs-lookup"><span data-stu-id="acbb1-114">This does not include the folder, as that must be set in the path object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acbb1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acbb1-115">Return value</span></span>

<span data-ttu-id="acbb1-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="acbb1-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acbb1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="acbb1-117">Remarks</span></span>

<span data-ttu-id="acbb1-118">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="acbb1-118">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="acbb1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acbb1-119">Requirements</span></span>



| <span data-ttu-id="acbb1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acbb1-120">Requirement</span></span> | <span data-ttu-id="acbb1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="acbb1-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acbb1-122">Version</span><span class="sxs-lookup"><span data-stu-id="acbb1-122">Version</span></span><br/> | <span data-ttu-id="acbb1-123">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="acbb1-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="acbb1-124">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="acbb1-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="acbb1-125">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="acbb1-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="acbb1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="acbb1-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="acbb1-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acbb1-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="acbb1-128">IID</span><span class="sxs-lookup"><span data-stu-id="acbb1-128">IID</span></span><br/>     | <span data-ttu-id="acbb1-129">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="acbb1-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




