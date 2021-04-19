---
description: La méthode EnableUIPreview de l’objet de base de données facilite la création de boîtes de dialogue et de panneaux en fournissant la prise en charge nécessaire pour afficher les boîtes de dialogue de l’interface utilisateur stockées dans la base de données du programme d’installation.
ms.assetid: c4687de7-8ab4-4377-ac5c-1fed7c915519
title: Database. EnableUIPreview, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.EnableUIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1224bb100e0403e8df9f3bdb0cc0b5dbe017233f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539300"
---
# <a name="databaseenableuipreview-method"></a><span data-ttu-id="aba4b-103">Database. EnableUIPreview, méthode</span><span class="sxs-lookup"><span data-stu-id="aba4b-103">Database.EnableUIPreview method</span></span>

<span data-ttu-id="aba4b-104">La méthode **EnableUIPreview** de l’objet [**de base de données**](database-object.md) facilite la création de boîtes de dialogue et de panneaux en fournissant la prise en charge nécessaire pour afficher les boîtes de dialogue de l’interface utilisateur stockées dans la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="aba4b-104">The **EnableUIPreview** method of the [**Database**](database-object.md) object facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span> <span data-ttu-id="aba4b-105">La méthode démarre le mode aperçu en retournant un objet **de base de données** en aperçu.</span><span class="sxs-lookup"><span data-stu-id="aba4b-105">The method starts the preview mode by returning a preview **Database** object.</span></span> <span data-ttu-id="aba4b-106">Le mode aperçu se termine lorsque l’objet Preview est relâché.</span><span class="sxs-lookup"><span data-stu-id="aba4b-106">The preview mode ends when the preview object is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba4b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aba4b-107">Syntax</span></span>


```JScript
Database.EnableUIPreview()
```



## <a name="parameters"></a><span data-ttu-id="aba4b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aba4b-108">Parameters</span></span>

<span data-ttu-id="aba4b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="aba4b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aba4b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aba4b-110">Return value</span></span>

<span data-ttu-id="aba4b-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="aba4b-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aba4b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aba4b-112">Requirements</span></span>



| <span data-ttu-id="aba4b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aba4b-113">Requirement</span></span> | <span data-ttu-id="aba4b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="aba4b-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba4b-115">Version</span><span class="sxs-lookup"><span data-stu-id="aba4b-115">Version</span></span><br/> | <span data-ttu-id="aba4b-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aba4b-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="aba4b-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aba4b-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="aba4b-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="aba4b-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="aba4b-119">DLL</span><span class="sxs-lookup"><span data-stu-id="aba4b-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="aba4b-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aba4b-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="aba4b-121">IID</span><span class="sxs-lookup"><span data-stu-id="aba4b-121">IID</span></span><br/>     | <span data-ttu-id="aba4b-122">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="aba4b-122">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




