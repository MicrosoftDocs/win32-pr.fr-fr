---
title: Méthode IWMDRMLicenseManagement RestoreLicenses (wmdrmsdk. h)
description: La méthode RestoreLicenses restaure les licences à partir d’une sauvegarde de licence créée en appelant la méthode BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Méthode RestoreLicenses format Windows Media
- Méthode RestoreLicenses format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode RestoreLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539643"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a><span data-ttu-id="7ac4f-106">IWMDRMLicenseManagement :: RestoreLicenses, méthode</span><span class="sxs-lookup"><span data-stu-id="7ac4f-106">IWMDRMLicenseManagement::RestoreLicenses method</span></span>

<span data-ttu-id="7ac4f-107">La méthode **RestoreLicenses** restaure les licences à partir d’une sauvegarde de licence créée en appelant la méthode [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) .</span><span class="sxs-lookup"><span data-stu-id="7ac4f-107">The **RestoreLicenses** method restores licenses from a license backup that was created by calling the [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac4f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ac4f-108">Syntax</span></span>


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="7ac4f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ac4f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ac4f-110">*bstrBackupDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ac4f-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ac4f-111">Chemin d’accès UNC de l’emplacement à partir duquel les licences seront restaurées.</span><span class="sxs-lookup"><span data-stu-id="7ac4f-111">UNC path of the location from which the licenses will be restored.</span></span>

</dd> <dt>

<span data-ttu-id="7ac4f-112">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ac4f-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ac4f-113">Indicateurs spécifiant les options de restauration à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7ac4f-113">Flags specifying the restore options to use.</span></span> <span data-ttu-id="7ac4f-114">Le seul indicateur actuellement pris en charge est l' \_ \_ élément de restauration WMDRM, qui configure la méthode pour effectuer l’individualisation dans le cadre de la restauration, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7ac4f-114">The only flag currently supported is WMDRM\_RESTORE\_INDIVIDUALIZE, which configures the method to perform individualization as part of the restoration, if required.</span></span>

</dd> <dt>

<span data-ttu-id="7ac4f-115">*ppunkCancelationCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ac4f-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ac4f-116">Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7ac4f-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="7ac4f-117">Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="7ac4f-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ac4f-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ac4f-118">Return value</span></span>

<span data-ttu-id="7ac4f-119">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7ac4f-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7ac4f-120">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7ac4f-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7ac4f-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7ac4f-121">Return code</span></span>                                                                          | <span data-ttu-id="7ac4f-122">Description</span><span class="sxs-lookup"><span data-stu-id="7ac4f-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7ac4f-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ac4f-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7ac4f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ac4f-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ac4f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="7ac4f-125">Remarks</span></span>

<span data-ttu-id="7ac4f-126">Cette méthode s’exécute de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7ac4f-126">This method executes asynchronously.</span></span> <span data-ttu-id="7ac4f-127">Elle retourne immédiatement après l’appel de, puis génère une série d’événements **MEWMDRMLicenseRestoreProgress** suivie d’un événement **MEWMDRMLicenseRestoreCompleted** lorsque le traitement est terminé.</span><span class="sxs-lookup"><span data-stu-id="7ac4f-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseRestoreProgress** events followed by an **MEWMDRMLicenseRestoreCompleted** event when processing is complete.</span></span> <span data-ttu-id="7ac4f-128">La valeur de chacun des événements **MEWMDRMLicenseRestoreProgress** obtenus en appelant **IMFMediaEvent :: GetValue** est un pointeur **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="7ac4f-128">The value of each of the **MEWMDRMLicenseRestoreProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="7ac4f-129">Vous pouvez appeler la méthode **QueryInterface** de l’interface **IUnknown** Récupérée pour récupérer une instance de l’interface [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="7ac4f-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="7ac4f-130">Pour plus d’informations sur l’utilisation des méthodes asynchrones des API étendues du client Windows Media DRM, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="7ac4f-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="7ac4f-131">La sauvegarde peut être à partir de l’ordinateur local ou d’un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7ac4f-131">The backup can be from the local machine or from a different machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac4f-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ac4f-132">Requirements</span></span>



| <span data-ttu-id="7ac4f-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ac4f-133">Requirement</span></span> | <span data-ttu-id="7ac4f-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ac4f-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac4f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ac4f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="7ac4f-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ac4f-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ac4f-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ac4f-137">Library</span></span><br/> | <dl> <span data-ttu-id="7ac4f-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ac4f-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ac4f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ac4f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac4f-140">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="7ac4f-140">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





