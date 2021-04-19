---
description: La propriété Property de l’objet session est une propriété en lecture-écriture qui représente la valeur de chaîne d’une propriété de programme d’installation nommée, telle qu’elle est gérée par l’objet de session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Session. Property, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528835"
---
# <a name="sessionproperty-property"></a><span data-ttu-id="83c0d-103">Session. Property, propriété</span><span class="sxs-lookup"><span data-stu-id="83c0d-103">Session.Property property</span></span>

<span data-ttu-id="83c0d-104">La propriété **Property** de l’objet [**session**](session-object.md) est une propriété en lecture-écriture qui représente la valeur de chaîne d’une propriété de programme d’installation nommée, telle qu’elle est gérée par l’objet de **session** dans la table de propriétés en mémoire ou, si elle est précédée d’un signe de pourcentage (%), de la valeur d’une variable d’environnement système pour le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="83c0d-104">The **Property** property of the [**Session**](session-object.md) object is a read-write property that represents the string value of a named installer property, as maintained by the **Session** object in the in-memory Property table, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="83c0d-105">Des valeurs de type chaîne ou entier peuvent être fournies.</span><span class="sxs-lookup"><span data-stu-id="83c0d-105">Either string or integer values may be supplied.</span></span> <span data-ttu-id="83c0d-106">Une variable d’environnement ou une propriété inexistante équivaut à une valeur null.</span><span class="sxs-lookup"><span data-stu-id="83c0d-106">A non-existent property or environment variable is equivalent to its value being Null.</span></span>

<span data-ttu-id="83c0d-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="83c0d-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c0d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83c0d-108">Syntax</span></span>


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="83c0d-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="83c0d-109">Property value</span></span>

<span data-ttu-id="83c0d-110">Nom de propriété obligatoire qui respecte la casse ou un nom qui ne respecte pas la casse d’une variable d’environnement préfixée par un signe de pourcentage (%).</span><span class="sxs-lookup"><span data-stu-id="83c0d-110">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="83c0d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83c0d-111">Requirements</span></span>



| <span data-ttu-id="83c0d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83c0d-112">Requirement</span></span> | <span data-ttu-id="83c0d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="83c0d-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c0d-114">Version</span><span class="sxs-lookup"><span data-stu-id="83c0d-114">Version</span></span><br/> | <span data-ttu-id="83c0d-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="83c0d-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="83c0d-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="83c0d-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="83c0d-117">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="83c0d-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="83c0d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="83c0d-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="83c0d-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83c0d-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="83c0d-120">IID</span><span class="sxs-lookup"><span data-stu-id="83c0d-120">IID</span></span><br/>     | <span data-ttu-id="83c0d-121">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="83c0d-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




