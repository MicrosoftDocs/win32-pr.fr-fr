---
description: La méthode Persist de l’objet SummaryInfo met en forme et écrit les propriétés précédemment stockées dans le flux SummaryInformation standard.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. Persist, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530325"
---
# <a name="summaryinfopersist-method"></a><span data-ttu-id="03725-103">SummaryInfo. Persist, méthode</span><span class="sxs-lookup"><span data-stu-id="03725-103">SummaryInfo.Persist method</span></span>

<span data-ttu-id="03725-104">La méthode **Persist** de l’objet [**SummaryInfo**](summaryinfo-object.md) met en forme et écrit les propriétés précédemment stockées dans le flux SummaryInformation standard.</span><span class="sxs-lookup"><span data-stu-id="03725-104">The **Persist** method of the [**SummaryInfo**](summaryinfo-object.md) object formats and writes the previously stored properties into the standard SummaryInformation stream.</span></span> <span data-ttu-id="03725-105">Elle génère une erreur si le flux ne peut pas être correctement écrit.</span><span class="sxs-lookup"><span data-stu-id="03725-105">It generates an error if the stream cannot be successfully written.</span></span> <span data-ttu-id="03725-106">Cette méthode ne peut être appelée qu’une seule fois après que toutes les valeurs de propriété ont été définies.</span><span class="sxs-lookup"><span data-stu-id="03725-106">This method may only be called once after all the property values have been set.</span></span> <span data-ttu-id="03725-107">Les propriétés peuvent toujours être lues après l’écriture du flux.</span><span class="sxs-lookup"><span data-stu-id="03725-107">Properties may still be read after the stream is written.</span></span>

## <a name="syntax"></a><span data-ttu-id="03725-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03725-108">Syntax</span></span>


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a><span data-ttu-id="03725-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03725-109">Parameters</span></span>

<span data-ttu-id="03725-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="03725-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03725-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03725-111">Return value</span></span>

<span data-ttu-id="03725-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="03725-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03725-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03725-113">Requirements</span></span>



| <span data-ttu-id="03725-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03725-114">Requirement</span></span> | <span data-ttu-id="03725-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="03725-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03725-116">Version</span><span class="sxs-lookup"><span data-stu-id="03725-116">Version</span></span><br/> | <span data-ttu-id="03725-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03725-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="03725-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="03725-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="03725-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="03725-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="03725-120">DLL</span><span class="sxs-lookup"><span data-stu-id="03725-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="03725-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03725-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="03725-122">IID</span><span class="sxs-lookup"><span data-stu-id="03725-122">IID</span></span><br/>     | <span data-ttu-id="03725-123">IID \_ ISummaryInfo est défini en tant que 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="03725-123">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



 

 




