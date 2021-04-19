---
description: La méthode CollectUserInfo de l’objet installer appelle une séquence de l’Assistant interface utilisateur qui collecte et stocke les informations utilisateur et le code du produit.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Installer. CollectUserInfo, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535253"
---
# <a name="installercollectuserinfo-method"></a><span data-ttu-id="bf238-103">Installer. CollectUserInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="bf238-103">Installer.CollectUserInfo method</span></span>

<span data-ttu-id="bf238-104">La méthode **CollectUserInfo** de l’objet [**installer**](installer-object.md) appelle une séquence de l’Assistant interface utilisateur qui collecte et stocke les informations utilisateur et le code du produit.</span><span class="sxs-lookup"><span data-stu-id="bf238-104">The **CollectUserInfo** method of the [**Installer**](installer-object.md) object invokes a user interface wizard sequence which collects and stores both user information and the product code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf238-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf238-105">Syntax</span></span>


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="bf238-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf238-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf238-107">*Produit*</span><span class="sxs-lookup"><span data-stu-id="bf238-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="bf238-108">Spécifie le [**Code de produit**](productcode.md) du produit.</span><span class="sxs-lookup"><span data-stu-id="bf238-108">Specifies the [**product code**](productcode.md) of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf238-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf238-109">Return value</span></span>

<span data-ttu-id="bf238-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bf238-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf238-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bf238-111">Remarks</span></span>

<span data-ttu-id="bf238-112">Une application doit appeler la méthode **CollectUserInfo** la première fois qu’elle est exécutée.</span><span class="sxs-lookup"><span data-stu-id="bf238-112">An application should call the **CollectUserInfo** method the first time it is run.</span></span> <span data-ttu-id="bf238-113">La méthode **CollectUserInfo** ouvre le package d’installation du produit et appelle une séquence créée de l’Assistant de l’interface utilisateur qui collecte les informations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bf238-113">The **CollectUserInfo** method opens the product's installation package and invokes an authored user interface wizard sequence which collects user information.</span></span> <span data-ttu-id="bf238-114">À la fin de la séquence de l’Assistant, les informations utilisateur collectées sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="bf238-114">Upon completion of the wizard sequence, the collected user information is registered.</span></span> <span data-ttu-id="bf238-115">La propriété [**UILevel**](installer-uilevel.md) doit être définie sur msiUILevelFull, car cette API requiert une interface utilisateur créée.</span><span class="sxs-lookup"><span data-stu-id="bf238-115">The [**UILevel**](installer-uilevel.md) property should be set to msiUILevelFull because this API requires an authored user interface.</span></span>

<span data-ttu-id="bf238-116">La méthode **CollectUserInfo** appelle la [boîte de dialogue firstrun](firstrun-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="bf238-116">The **CollectUserInfo** method invokes the [FirstRun Dialog](firstrun-dialog.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf238-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf238-117">Requirements</span></span>



| <span data-ttu-id="bf238-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf238-118">Requirement</span></span> | <span data-ttu-id="bf238-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf238-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf238-120">Version</span><span class="sxs-lookup"><span data-stu-id="bf238-120">Version</span></span><br/> | <span data-ttu-id="bf238-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf238-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bf238-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bf238-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bf238-123">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf238-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bf238-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bf238-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="bf238-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf238-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bf238-126">IID</span><span class="sxs-lookup"><span data-stu-id="bf238-126">IID</span></span><br/>     | <span data-ttu-id="bf238-127">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bf238-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="bf238-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf238-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf238-129">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="bf238-129">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




