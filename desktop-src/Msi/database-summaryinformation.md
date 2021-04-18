---
description: La propriété SummaryInformation de l’objet de base de données retourne un objet SummaryInfo qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d’informations de synthèse.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Propriété Database. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543341"
---
# <a name="databasesummaryinformation-property"></a><span data-ttu-id="7bd54-103">Propriété Database. SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="7bd54-103">Database.SummaryInformation property</span></span>

<span data-ttu-id="7bd54-104">La propriété **SummaryInformation** de l’objet [**de base de données**](database-object.md) retourne un objet [**SummaryInfo**](summaryinfo-object.md) qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d' [informations de synthèse](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="7bd54-104">The **SummaryInformation** property of the [**Database**](database-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the [summary information stream](summary-information-stream.md).</span></span>

<span data-ttu-id="7bd54-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7bd54-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd54-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bd54-106">Syntax</span></span>


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="7bd54-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7bd54-107">Property value</span></span>

<span data-ttu-id="7bd54-108">Nombre maximal de propriétés à ajouter ou à modifier.</span><span class="sxs-lookup"><span data-stu-id="7bd54-108">The maximum number of properties to be added or modified.</span></span> <span data-ttu-id="7bd54-109">Ce paramètre est obligatoire et utilisé pour allouer une quantité de mémoire de travail suffisante pendant la génération du flux.</span><span class="sxs-lookup"><span data-stu-id="7bd54-109">This parameter is required and used to allocate sufficient working memory during the stream generation.</span></span> <span data-ttu-id="7bd54-110">Il n’est pas nécessaire de stocker ce nombre de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7bd54-110">It is not required to store this number of properties.</span></span> <span data-ttu-id="7bd54-111">La valeur zéro doit être utilisée si la base de données est ouverte en lecture seule pour empêcher la mise à jour du flux.</span><span class="sxs-lookup"><span data-stu-id="7bd54-111">A value of zero must be used if the database is opened read-only to prevent the stream from being updated.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bd54-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7bd54-112">Remarks</span></span>

<span data-ttu-id="7bd54-113">Si une valeur de *maxProperties* supérieure à 0 est utilisée pour ouvrir un flux d’informations de résumé existant, la méthode [**Persist**](summaryinfo-persist.md) doit être appelée avant la fermeture de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7bd54-113">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="7bd54-114">Si vous ne le faites pas, les informations de flux existantes seront perdues.</span><span class="sxs-lookup"><span data-stu-id="7bd54-114">Failing to do this will lose the existing stream information.</span></span>

<span data-ttu-id="7bd54-115">Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="7bd54-115">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bd54-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bd54-116">Requirements</span></span>



| <span data-ttu-id="7bd54-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bd54-117">Requirement</span></span> | <span data-ttu-id="7bd54-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bd54-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd54-119">Version</span><span class="sxs-lookup"><span data-stu-id="7bd54-119">Version</span></span><br/> | <span data-ttu-id="7bd54-120">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7bd54-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7bd54-121">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7bd54-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7bd54-122">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="7bd54-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7bd54-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7bd54-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="7bd54-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bd54-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7bd54-125">IID</span><span class="sxs-lookup"><span data-stu-id="7bd54-125">IID</span></span><br/>     | <span data-ttu-id="7bd54-126">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7bd54-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




