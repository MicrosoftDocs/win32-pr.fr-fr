---
description: La méthode fetch de l’objet View récupère la ligne suivante de données de colonne si davantage de lignes sont disponibles dans le jeu de résultats, sinon elle a la valeur null. Appelez la méthode Execute avant la méthode fetch.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. Fetch, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532518"
---
# <a name="viewfetch-method"></a><span data-ttu-id="68f39-104">View. Fetch, méthode</span><span class="sxs-lookup"><span data-stu-id="68f39-104">View.Fetch method</span></span>

<span data-ttu-id="68f39-105">La méthode **Fetch** de l’objet [**View**](view-object.md) récupère la ligne suivante de données de colonne si davantage de lignes sont disponibles dans le jeu de résultats, sinon elle a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="68f39-105">The **Fetch** method of the [**View**](view-object.md) object retrieves the next row of column data if more rows are available in the result set, otherwise it is Null.</span></span> <span data-ttu-id="68f39-106">Appelez la méthode [**Execute**](view-execute.md) avant la méthode **Fetch** .</span><span class="sxs-lookup"><span data-stu-id="68f39-106">Call the [**Execute**](view-execute.md) method before the **Fetch** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f39-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68f39-107">Syntax</span></span>


```JScript
View.Fetch()
```



## <a name="parameters"></a><span data-ttu-id="68f39-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68f39-108">Parameters</span></span>

<span data-ttu-id="68f39-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="68f39-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68f39-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68f39-110">Return value</span></span>

<span data-ttu-id="68f39-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="68f39-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68f39-112">Notes</span><span class="sxs-lookup"><span data-stu-id="68f39-112">Remarks</span></span>

<span data-ttu-id="68f39-113">Le même objet d' [**enregistrement**](record-object.md) doit être utilisé pour récupérer les données dans plusieurs lignes, sinon l’objet doit être libéré en étant hors de portée.</span><span class="sxs-lookup"><span data-stu-id="68f39-113">The same [**Record**](record-object.md) object should be used to retrieve the data in multiple rows, or else the object should be released by going out of scope.</span></span> <span data-ttu-id="68f39-114">L’enregistrement peut être testé pour la fin du jeu de résultats à l’aide de la syntaxe « if FetchRecord Is Nothing ».</span><span class="sxs-lookup"><span data-stu-id="68f39-114">The record can be tested for the end of the result set using the syntax "If FetchRecord Is Nothing".</span></span>

## <a name="requirements"></a><span data-ttu-id="68f39-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68f39-115">Requirements</span></span>



| <span data-ttu-id="68f39-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68f39-116">Requirement</span></span> | <span data-ttu-id="68f39-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="68f39-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68f39-118">Version</span><span class="sxs-lookup"><span data-stu-id="68f39-118">Version</span></span><br/> | <span data-ttu-id="68f39-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="68f39-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="68f39-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="68f39-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="68f39-121">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="68f39-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="68f39-122">DLL</span><span class="sxs-lookup"><span data-stu-id="68f39-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="68f39-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f39-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="68f39-124">IID</span><span class="sxs-lookup"><span data-stu-id="68f39-124">IID</span></span><br/>     | <span data-ttu-id="68f39-125">L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="68f39-125">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




