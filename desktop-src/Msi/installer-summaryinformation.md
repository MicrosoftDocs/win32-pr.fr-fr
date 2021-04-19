---
description: La propriété SummaryInformation de l’objet installer retourne un objet SummaryInfo qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d’informations de synthèse d’un package ou d’une transformation.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Installer. SummaryInformation, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541016"
---
# <a name="installersummaryinformation-property"></a><span data-ttu-id="a9b82-103">Installer. SummaryInformation, propriété</span><span class="sxs-lookup"><span data-stu-id="a9b82-103">Installer.SummaryInformation property</span></span>

<span data-ttu-id="a9b82-104">La propriété **SummaryInformation** de l’objet [**installer**](installer-object.md) retourne un objet [**SummaryInfo**](summaryinfo-object.md) qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d’informations de synthèse d’un package ou d’une transformation.</span><span class="sxs-lookup"><span data-stu-id="a9b82-104">The **SummaryInformation** property of the [**Installer**](installer-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream of a package or transform.</span></span>

<span data-ttu-id="a9b82-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a9b82-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b82-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9b82-106">Syntax</span></span>


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="a9b82-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a9b82-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b82-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a9b82-108">Remarks</span></span>

<span data-ttu-id="a9b82-109">Si une valeur de *maxProperties* supérieure à 0 est utilisée pour ouvrir un flux d’informations de résumé existant, la méthode [**Persist**](summaryinfo-persist.md) doit être appelée avant la fermeture de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a9b82-109">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="a9b82-110">Si ce n’est pas le cas, les informations de flux existantes sont perdues.</span><span class="sxs-lookup"><span data-stu-id="a9b82-110">Failing to do this loses the existing stream information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b82-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9b82-111">Requirements</span></span>



| <span data-ttu-id="a9b82-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9b82-112">Requirement</span></span> | <span data-ttu-id="a9b82-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9b82-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b82-114">Version</span><span class="sxs-lookup"><span data-stu-id="a9b82-114">Version</span></span><br/> | <span data-ttu-id="a9b82-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a9b82-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a9b82-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a9b82-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a9b82-117">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9b82-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a9b82-118">DLL</span><span class="sxs-lookup"><span data-stu-id="a9b82-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="a9b82-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9b82-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a9b82-120">IID</span><span class="sxs-lookup"><span data-stu-id="a9b82-120">IID</span></span><br/>     | <span data-ttu-id="a9b82-121">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a9b82-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




