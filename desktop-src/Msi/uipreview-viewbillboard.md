---
description: La méthode ViewBillboard de l’objet UIPreview affiche un panneau d’affichage créé à l’aide du contrôle hôte dans la boîte de dialogue actuellement affichée.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Méthode UIPreview. ViewBillboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526082"
---
# <a name="uipreviewviewbillboard-method"></a><span data-ttu-id="2291c-103">Méthode UIPreview. ViewBillboard</span><span class="sxs-lookup"><span data-stu-id="2291c-103">UIPreview.ViewBillboard method</span></span>

<span data-ttu-id="2291c-104">La méthode **ViewBillboard** de l’objet [**UIPreview**](uipreview-object.md) affiche un panneau d’affichage créé à l’aide du contrôle hôte dans la boîte de dialogue actuellement affichée.</span><span class="sxs-lookup"><span data-stu-id="2291c-104">The **ViewBillboard** method of the [**UIPreview**](uipreview-object.md) object displays an authored billboard using the host control in the currently displayed dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="2291c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2291c-105">Syntax</span></span>


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a><span data-ttu-id="2291c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2291c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2291c-107">*control*</span><span class="sxs-lookup"><span data-stu-id="2291c-107">*control*</span></span> 
</dt> <dd>

<span data-ttu-id="2291c-108">Nom requis du contrôle qui héberge le panneau, qui respecte la casse, ainsi que la boîte de dialogue, et les clés primaires de la table de base de données de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2291c-108">Required name of the control hosting the billboard, case-sensitive, along with the dialog box, and the primary keys of the Control database table.</span></span>

</dd> <dt>

<span data-ttu-id="2291c-109">*blanc*</span><span class="sxs-lookup"><span data-stu-id="2291c-109">*billboard*</span></span> 
</dt> <dd>

<span data-ttu-id="2291c-110">Nom requis du panneau d’affichage à afficher à l’aide du contrôle spécifié et de la boîte de dialogue active, ainsi que de la clé primaire de la table de base de données de tableau blanc.</span><span class="sxs-lookup"><span data-stu-id="2291c-110">Required name of the billboard to display using the specified control and current dialog box, and the primary key of the Billboard database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2291c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2291c-111">Return value</span></span>

<span data-ttu-id="2291c-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2291c-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2291c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2291c-113">Requirements</span></span>



| <span data-ttu-id="2291c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2291c-114">Requirement</span></span> | <span data-ttu-id="2291c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2291c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2291c-116">Version</span><span class="sxs-lookup"><span data-stu-id="2291c-116">Version</span></span><br/> | <span data-ttu-id="2291c-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2291c-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2291c-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2291c-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2291c-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="2291c-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2291c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2291c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="2291c-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2291c-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2291c-122">IID</span><span class="sxs-lookup"><span data-stu-id="2291c-122">IID</span></span><br/>     | <span data-ttu-id="2291c-123">IID \_ IUIPreview est défini en tant que 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2291c-123">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




