---
description: La méthode ViewDialog de l’objet UIPreview affiche une boîte de dialogue d’interface utilisateur créée, stockée dans la base de données active.
ms.assetid: 5bc935ac-38ca-4a51-a1dc-6879dee97b05
title: Méthode UIPreview. ViewDialog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewDialog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d9ad3772ced2dba952a3d3b068aaa307d1c06398
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540385"
---
# <a name="uipreviewviewdialog-method"></a><span data-ttu-id="9e72d-103">Méthode UIPreview. ViewDialog</span><span class="sxs-lookup"><span data-stu-id="9e72d-103">UIPreview.ViewDialog method</span></span>

<span data-ttu-id="9e72d-104">La méthode **ViewDialog** de l’objet [**UIPreview**](uipreview-object.md) affiche une boîte de dialogue d’interface utilisateur créée, stockée dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="9e72d-104">The **ViewDialog** method of the [**UIPreview**](uipreview-object.md) object displays an authored user interface dialog box stored in the current database.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e72d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e72d-105">Syntax</span></span>


```JScript
UIPreview.ViewDialog(
  dialog
)
```



## <a name="parameters"></a><span data-ttu-id="9e72d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e72d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e72d-107">*dialogue*</span><span class="sxs-lookup"><span data-stu-id="9e72d-107">*dialog*</span></span> 
</dt> <dd>

<span data-ttu-id="9e72d-108">Nom requis de la boîte de dialogue, respect de la casse et de la clé primaire de la table de base de données de boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9e72d-108">Required name of the dialog box, case-sensitive, and the primary key of the Dialog database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e72d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e72d-109">Return value</span></span>

<span data-ttu-id="9e72d-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9e72d-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e72d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e72d-111">Requirements</span></span>



| <span data-ttu-id="9e72d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e72d-112">Requirement</span></span> | <span data-ttu-id="9e72d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e72d-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e72d-114">Version</span><span class="sxs-lookup"><span data-stu-id="9e72d-114">Version</span></span><br/> | <span data-ttu-id="9e72d-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9e72d-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9e72d-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e72d-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9e72d-117">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="9e72d-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9e72d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9e72d-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="9e72d-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e72d-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9e72d-120">IID</span><span class="sxs-lookup"><span data-stu-id="9e72d-120">IID</span></span><br/>     | <span data-ttu-id="9e72d-121">IID \_ IUIPreview est défini en tant que 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9e72d-121">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




