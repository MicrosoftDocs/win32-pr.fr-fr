---
description: La méthode SetStream de l’objet record copie le contenu du fichier spécifié dans le champ d’enregistrement désigné en tant que données de flux. Les données de flux ne peuvent pas être insérées dans les champs temporaires.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Record. SetStream, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521654"
---
# <a name="recordsetstream-method"></a><span data-ttu-id="89e3a-104">Record. SetStream, méthode</span><span class="sxs-lookup"><span data-stu-id="89e3a-104">Record.SetStream method</span></span>

<span data-ttu-id="89e3a-105">La méthode **SetStream** de l’objet [**Record**](record-object.md) copie le contenu du fichier spécifié dans le champ d’enregistrement désigné en tant que données de flux.</span><span class="sxs-lookup"><span data-stu-id="89e3a-105">The **SetStream** method of the [**Record**](record-object.md) object copies the content of the specified file into the designated record field as stream data.</span></span> <span data-ttu-id="89e3a-106">Les données de flux ne peuvent pas être insérées dans les champs temporaires.</span><span class="sxs-lookup"><span data-stu-id="89e3a-106">Stream data cannot be inserted into temporary fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e3a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89e3a-107">Syntax</span></span>


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a><span data-ttu-id="89e3a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89e3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89e3a-109">*case*</span><span class="sxs-lookup"><span data-stu-id="89e3a-109">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="89e3a-110">Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.</span><span class="sxs-lookup"><span data-stu-id="89e3a-110">Required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="89e3a-111">*cheminfichier*</span><span class="sxs-lookup"><span data-stu-id="89e3a-111">*filePath*</span></span> 
</dt> <dd>

<span data-ttu-id="89e3a-112">Emplacement du fichier à copier.</span><span class="sxs-lookup"><span data-stu-id="89e3a-112">The location of the file to copy.</span></span> <span data-ttu-id="89e3a-113">Aucune traduction de tout type n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="89e3a-113">No translation of any type is performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89e3a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89e3a-114">Return value</span></span>

<span data-ttu-id="89e3a-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="89e3a-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89e3a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="89e3a-116">Remarks</span></span>

<span data-ttu-id="89e3a-117">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="89e3a-117">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="89e3a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89e3a-118">Requirements</span></span>



| <span data-ttu-id="89e3a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89e3a-119">Requirement</span></span> | <span data-ttu-id="89e3a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="89e3a-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89e3a-121">Version</span><span class="sxs-lookup"><span data-stu-id="89e3a-121">Version</span></span><br/> | <span data-ttu-id="89e3a-122">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89e3a-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="89e3a-123">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="89e3a-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="89e3a-124">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="89e3a-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="89e3a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="89e3a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="89e3a-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89e3a-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="89e3a-127">IID</span><span class="sxs-lookup"><span data-stu-id="89e3a-127">IID</span></span><br/>     | <span data-ttu-id="89e3a-128">IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="89e3a-128">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




