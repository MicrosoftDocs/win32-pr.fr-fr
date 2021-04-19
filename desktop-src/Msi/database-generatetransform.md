---
description: La méthode GenerateTransform de l’objet Database crée une transformation qui, lorsqu’elle est appliquée à la base de données Object, produit la base de données de référence. La transformation est stockée dans l’objet de stockage.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Database. GenerateTransform, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528794"
---
# <a name="databasegeneratetransform-method"></a><span data-ttu-id="eef98-104">Database. GenerateTransform, méthode</span><span class="sxs-lookup"><span data-stu-id="eef98-104">Database.GenerateTransform method</span></span>

<span data-ttu-id="eef98-105">La méthode **GenerateTransform** de l’objet [**Database**](database-object.md) crée une [*transformation*](t-gly.md) qui, lorsqu’elle est appliquée à la base de données Object, produit la base de données de référence.</span><span class="sxs-lookup"><span data-stu-id="eef98-105">The **GenerateTransform** method of the [**Database**](database-object.md) object creates a [*transform*](t-gly.md) that, when applied to the object database, results in the reference database.</span></span> <span data-ttu-id="eef98-106">La transformation est stockée dans l’objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="eef98-106">The transform is stored in the storage object.</span></span>

<span data-ttu-id="eef98-107">Si la transformation doit être appliquée au cours d’une installation, vous devez utiliser la méthode [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) pour renseigner le flux d’informations de synthèse.</span><span class="sxs-lookup"><span data-stu-id="eef98-107">If the transform is to be applied during an installation you must use the [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) method to populate the summary information stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef98-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eef98-108">Syntax</span></span>


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a><span data-ttu-id="eef98-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eef98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef98-110">*reference*</span><span class="sxs-lookup"><span data-stu-id="eef98-110">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="eef98-111">Base de données requise qui n’inclut pas les modifications.</span><span class="sxs-lookup"><span data-stu-id="eef98-111">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="eef98-112">*storage*</span><span class="sxs-lookup"><span data-stu-id="eef98-112">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="eef98-113">Nom du fichier de transformation généré.</span><span class="sxs-lookup"><span data-stu-id="eef98-113">The name of the generated transform file.</span></span> <span data-ttu-id="eef98-114">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="eef98-114">This is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef98-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eef98-115">Return value</span></span>

<span data-ttu-id="eef98-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="eef98-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eef98-117">Notes</span><span class="sxs-lookup"><span data-stu-id="eef98-117">Remarks</span></span>

<span data-ttu-id="eef98-118">Une transformation peut ajouter des colonnes clés non primaires à la fin d’une table.</span><span class="sxs-lookup"><span data-stu-id="eef98-118">A transform can add non-primary key columns to the end of a table.</span></span> <span data-ttu-id="eef98-119">Impossible de créer une transformation qui ajoute des colonnes clés primaires à une table.</span><span class="sxs-lookup"><span data-stu-id="eef98-119">A transform cannot be created that adds primary key columns to a table.</span></span> <span data-ttu-id="eef98-120">Impossible de créer une transformation qui modifie l’ordre, les noms ou les définitions des colonnes.</span><span class="sxs-lookup"><span data-stu-id="eef98-120">A transform cannot be created that changes the order, names, or definitions of columns.</span></span>

<span data-ttu-id="eef98-121">Cette méthode retourne une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="eef98-121">This method returns a Boolean value.</span></span> <span data-ttu-id="eef98-122">Elle retourne la valeur TRUE si une transformation est générée.</span><span class="sxs-lookup"><span data-stu-id="eef98-122">It returns TRUE if a transform is generated.</span></span> <span data-ttu-id="eef98-123">Elle retourne la valeur FALSe si aucune transformation n’est générée, car il n’existe aucune différence entre les deux bases de données.</span><span class="sxs-lookup"><span data-stu-id="eef98-123">It returns FALSE if a transform is not generated because there are no differences between the two databases.</span></span> <span data-ttu-id="eef98-124">Si la méthode échoue, elle génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="eef98-124">If the method fails, it generates an error.</span></span>

<span data-ttu-id="eef98-125">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="eef98-125">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eef98-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eef98-126">Requirements</span></span>



| <span data-ttu-id="eef98-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eef98-127">Requirement</span></span> | <span data-ttu-id="eef98-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="eef98-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef98-129">Version</span><span class="sxs-lookup"><span data-stu-id="eef98-129">Version</span></span><br/> | <span data-ttu-id="eef98-130">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eef98-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eef98-131">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eef98-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eef98-132">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="eef98-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="eef98-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eef98-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="eef98-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eef98-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="eef98-135">IID</span><span class="sxs-lookup"><span data-stu-id="eef98-135">IID</span></span><br/>     | <span data-ttu-id="eef98-136">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="eef98-136">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="eef98-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eef98-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef98-138">**Base de données**</span><span class="sxs-lookup"><span data-stu-id="eef98-138">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="eef98-139">Transformations de base de données</span><span class="sxs-lookup"><span data-stu-id="eef98-139">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




