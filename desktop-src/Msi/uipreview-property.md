---
description: La propriété Property de l’objet UIPreview est une propriété en lecture-écriture qui représente la valeur de chaîne d’une propriété de programme d’installation nommée ou, si elle est précédée d’un signe de pourcentage (%), de la valeur d’une variable d’environnement système pour le processus en cours.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Propriété UIPreview. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541107"
---
# <a name="uipreviewproperty-property"></a><span data-ttu-id="07d01-103">Propriété UIPreview. Property</span><span class="sxs-lookup"><span data-stu-id="07d01-103">UIPreview.Property property</span></span>

<span data-ttu-id="07d01-104">La propriété **Property** de l’objet [**UIPreview**](uipreview-object.md) est une propriété en lecture-écriture qui représente la valeur de chaîne d’une propriété de programme d’installation nommée ou, si elle est précédée d’un signe de pourcentage (%), de la valeur d’une variable d’environnement système pour le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="07d01-104">The **Property** property of the [**UIPreview**](uipreview-object.md) object is a read-write property that represents the string value of a named installer property, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="07d01-105">Cette valeur est exposée pour permettre l’affichage correct des boîtes de dialogue qui sont dépendantes des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="07d01-105">This is exposed to allow proper display of dialog boxes that are dependent upon property values.</span></span> <span data-ttu-id="07d01-106">Des valeurs de type chaîne ou entier peuvent être fournies.</span><span class="sxs-lookup"><span data-stu-id="07d01-106">Either string or integer values may be supplied.</span></span> <span data-ttu-id="07d01-107">Une variable d’environnement ou une propriété inexistante équivaut à une valeur null.</span><span class="sxs-lookup"><span data-stu-id="07d01-107">A nonexistent property or environment variable is equivalent to its value being null.</span></span>

<span data-ttu-id="07d01-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="07d01-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d01-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07d01-109">Syntax</span></span>


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="07d01-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="07d01-110">Property value</span></span>

<span data-ttu-id="07d01-111">Nom de propriété obligatoire qui respecte la casse ou un nom qui ne respecte pas la casse d’une variable d’environnement préfixée par un signe de pourcentage (%).</span><span class="sxs-lookup"><span data-stu-id="07d01-111">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="07d01-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07d01-112">Requirements</span></span>



| <span data-ttu-id="07d01-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07d01-113">Requirement</span></span> | <span data-ttu-id="07d01-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="07d01-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d01-115">Version</span><span class="sxs-lookup"><span data-stu-id="07d01-115">Version</span></span><br/> | <span data-ttu-id="07d01-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="07d01-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="07d01-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="07d01-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="07d01-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="07d01-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="07d01-119">DLL</span><span class="sxs-lookup"><span data-stu-id="07d01-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="07d01-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d01-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="07d01-121">IID</span><span class="sxs-lookup"><span data-stu-id="07d01-121">IID</span></span><br/>     | <span data-ttu-id="07d01-122">IID \_ IUIPreview est défini en tant que 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="07d01-122">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




