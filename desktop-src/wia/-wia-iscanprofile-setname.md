---
description: Définit le nom convivial du profil.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'IScanProfile :: SetName, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517094"
---
# <a name="iscanprofilesetname-method"></a><span data-ttu-id="b95fd-103">IScanProfile :: SetName, méthode</span><span class="sxs-lookup"><span data-stu-id="b95fd-103">IScanProfile::SetName method</span></span>

<span data-ttu-id="b95fd-104">Définit le nom convivial du profil.</span><span class="sxs-lookup"><span data-stu-id="b95fd-104">Sets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="b95fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b95fd-105">Syntax</span></span>


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a><span data-ttu-id="b95fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b95fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b95fd-107">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b95fd-107">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b95fd-108">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b95fd-108">Type: **BSTR**</span></span>

<span data-ttu-id="b95fd-109">Nom convivial du profil.</span><span class="sxs-lookup"><span data-stu-id="b95fd-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b95fd-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b95fd-110">Return value</span></span>

<span data-ttu-id="b95fd-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b95fd-111">Type: **HRESULT**</span></span>

<span data-ttu-id="b95fd-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b95fd-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b95fd-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b95fd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b95fd-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b95fd-114">Remarks</span></span>

<span data-ttu-id="b95fd-115">Cette méthode est requise car le GUID d’un profil ne peut pas être utilisé pour afficher le profil de numérisation à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b95fd-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

<span data-ttu-id="b95fd-116">Un utilisateur peut modifier le nom convivial d’un profil à l’aide de la méthode [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="b95fd-116">A user can change the friendly name of a profile with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="b95fd-117">Les modifications apportées à un profil ne sont pas enregistrées sur le disque tant que l’application n’a pas appelé la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="b95fd-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="b95fd-118">Si deux applications créent des objets de profil d’analyse à partir du même fichier XML, et que chaque application écrit des modifications dans son objet, seules les modifications apportées par l’application qui appelle [**IScanProfile :: Save**](-wia-iscanprofile-save.md) Last sont enregistrées sur le disque.</span><span class="sxs-lookup"><span data-stu-id="b95fd-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="b95fd-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b95fd-119">Requirements</span></span>



| <span data-ttu-id="b95fd-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b95fd-120">Requirement</span></span> | <span data-ttu-id="b95fd-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b95fd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b95fd-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b95fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b95fd-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b95fd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b95fd-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b95fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b95fd-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b95fd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b95fd-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b95fd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b95fd-127"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="b95fd-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="b95fd-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="b95fd-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b95fd-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b95fd-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



 

 




