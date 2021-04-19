---
description: La propriété SourcePath de l’objet session est une propriété en lecture seule qui fournit le chemin d’accès complet au dossier désigné sur le média source ou l’image serveur.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Session. SourcePath, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541515"
---
# <a name="sessionsourcepath-property"></a><span data-ttu-id="c57ae-103">Session. SourcePath, propriété</span><span class="sxs-lookup"><span data-stu-id="c57ae-103">Session.SourcePath property</span></span>

<span data-ttu-id="c57ae-104">La propriété **SourcePath** de l’objet [**session**](session-object.md) est une propriété en lecture seule qui fournit le chemin d’accès complet au dossier désigné sur le média source ou l’image serveur.</span><span class="sxs-lookup"><span data-stu-id="c57ae-104">The **SourcePath** property of the [**Session**](session-object.md) object is a read-only property that provides the full path to the designated folder on the source media or server image.</span></span>

<span data-ttu-id="c57ae-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c57ae-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57ae-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c57ae-106">Syntax</span></span>


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a><span data-ttu-id="c57ae-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c57ae-107">Property value</span></span>

<span data-ttu-id="c57ae-108">Nom d’une propriété de dossier obligatoire et sensible à la casse, comme spécifié par une clé primaire de la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="c57ae-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="c57ae-109">Une erreur est générée si le dossier n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c57ae-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="c57ae-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c57ae-110">Remarks</span></span>

<span data-ttu-id="c57ae-111">Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="c57ae-111">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57ae-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c57ae-112">Requirements</span></span>



| <span data-ttu-id="c57ae-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c57ae-113">Requirement</span></span> | <span data-ttu-id="c57ae-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c57ae-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57ae-115">Version</span><span class="sxs-lookup"><span data-stu-id="c57ae-115">Version</span></span><br/> | <span data-ttu-id="c57ae-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c57ae-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c57ae-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c57ae-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c57ae-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="c57ae-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c57ae-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c57ae-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="c57ae-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c57ae-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c57ae-121">IID</span><span class="sxs-lookup"><span data-stu-id="c57ae-121">IID</span></span><br/>     | <span data-ttu-id="c57ae-122">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c57ae-122">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




