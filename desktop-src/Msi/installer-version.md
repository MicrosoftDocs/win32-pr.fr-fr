---
description: La propriété version de l’objet installer est une propriété en lecture seule qui est la représentation sous forme de chaîne de la version actuelle de Windows Installer. La chaîne est retournée sous la forme suivante.
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: Installer. version, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 29af85b8fc1afe468dc87d5516da9a528024c73a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526844"
---
# <a name="installerversion-property"></a><span data-ttu-id="9c7fb-104">Installer. version, propriété</span><span class="sxs-lookup"><span data-stu-id="9c7fb-104">Installer.Version property</span></span>

<span data-ttu-id="9c7fb-105">La propriété **version** de l’objet [**installer**](installer-object.md) est une propriété en lecture seule qui est la représentation sous forme de chaîne de la version actuelle de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9c7fb-105">The **Version** property of the [**Installer**](installer-object.md) object is a read-only property that is the string representation of the current version of Windows Installer.</span></span> <span data-ttu-id="9c7fb-106">La chaîne est retournée sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="9c7fb-106">The string is returned in the following form.</span></span>

<span data-ttu-id="9c7fb-107">*majeure*. *mineure*. *générer*. *mettre à jour*</span><span class="sxs-lookup"><span data-stu-id="9c7fb-107">*major*.*minor*.*build*.*update*</span></span>

<span data-ttu-id="9c7fb-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9c7fb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c7fb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c7fb-109">Syntax</span></span>


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a><span data-ttu-id="9c7fb-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9c7fb-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="9c7fb-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c7fb-111">Requirements</span></span>



| <span data-ttu-id="9c7fb-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c7fb-112">Requirement</span></span> | <span data-ttu-id="9c7fb-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c7fb-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c7fb-114">Version</span><span class="sxs-lookup"><span data-stu-id="9c7fb-114">Version</span></span><br/> | <span data-ttu-id="9c7fb-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9c7fb-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9c7fb-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c7fb-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9c7fb-117">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c7fb-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9c7fb-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9c7fb-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="9c7fb-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c7fb-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9c7fb-120">IID</span><span class="sxs-lookup"><span data-stu-id="9c7fb-120">IID</span></span><br/>     | <span data-ttu-id="9c7fb-121">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9c7fb-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




