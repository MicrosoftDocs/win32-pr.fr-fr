---
title: Méthode IWMDRMLicenseManagement BackupLicenses (wmdrmsdk. h)
description: La méthode BackupLicenses crée une sauvegarde des licences dans le magasin de licences local.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Méthode BackupLicenses format Windows Media
- Méthode BackupLicenses format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode BackupLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543795"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a><span data-ttu-id="5702f-106">IWMDRMLicenseManagement :: BackupLicenses, méthode</span><span class="sxs-lookup"><span data-stu-id="5702f-106">IWMDRMLicenseManagement::BackupLicenses method</span></span>

<span data-ttu-id="5702f-107">La méthode **BackupLicenses** crée une sauvegarde des licences dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="5702f-107">The **BackupLicenses** method creates a backup of the licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="5702f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5702f-108">Syntax</span></span>


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="5702f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5702f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5702f-110">*bstrBackupDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5702f-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5702f-111">Chemin d’accès UNC de l’emplacement vers lequel les licences seront sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="5702f-111">UNC path of the location to which the licenses will be backed up.</span></span>

</dd> <dt>

<span data-ttu-id="5702f-112">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5702f-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5702f-113">Indicateurs spécifiant les options de sauvegarde à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5702f-113">Flags specifying the backup options to use.</span></span> <span data-ttu-id="5702f-114">Le seul indicateur actuellement pris en charge est le \_ remplacement de la sauvegarde WMDRM \_ , qui configure la méthode pour remplacer les fichiers de sauvegarde existants dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="5702f-114">The only flag currently supported is WMDRM\_BACKUP\_OVERWRITE, which configures the method to overwrite any existing backup files in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="5702f-115">*ppunkCancelationCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5702f-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5702f-116">Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5702f-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="5702f-117">Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="5702f-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5702f-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5702f-118">Return value</span></span>

<span data-ttu-id="5702f-119">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5702f-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5702f-120">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5702f-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5702f-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5702f-121">Return code</span></span>                                                                          | <span data-ttu-id="5702f-122">Description</span><span class="sxs-lookup"><span data-stu-id="5702f-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5702f-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5702f-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5702f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5702f-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5702f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5702f-125">Remarks</span></span>

<span data-ttu-id="5702f-126">Cette méthode s’exécute de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5702f-126">This method executes asynchronously.</span></span> <span data-ttu-id="5702f-127">Elle retourne immédiatement après l’appel de, puis génère une série d’événements **MEWMDRMLicenseBackupProgress** suivie d’un événement **MEWMDRMLicenseBackupCompleted** lorsque le traitement est terminé.</span><span class="sxs-lookup"><span data-stu-id="5702f-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseBackupProgress** events followed by an **MEWMDRMLicenseBackupCompleted** event when processing is complete.</span></span> <span data-ttu-id="5702f-128">La valeur de chacun des événements **MEWMDRMLicenseBackupProgress** obtenus en appelant **IMFMediaEvent :: GetValue** est un pointeur **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="5702f-128">The value of each of the **MEWMDRMLicenseBackupProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="5702f-129">Vous pouvez appeler la méthode **QueryInterface** de l’interface **IUnknown** Récupérée pour récupérer une instance de l’interface [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="5702f-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="5702f-130">Pour plus d’informations sur l’utilisation des méthodes asynchrones des API étendues du client Windows Media DRM, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="5702f-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="5702f-131">Toutes les licences ne sont pas autorisées à être sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="5702f-131">Not all licenses are permitted to be backed up.</span></span> <span data-ttu-id="5702f-132">Cette méthode sauvegarde uniquement les licences qui l’autorisent.</span><span class="sxs-lookup"><span data-stu-id="5702f-132">This method only backs up licenses that allow it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5702f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5702f-133">Requirements</span></span>



| <span data-ttu-id="5702f-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5702f-134">Requirement</span></span> | <span data-ttu-id="5702f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5702f-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5702f-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5702f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="5702f-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5702f-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5702f-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5702f-138">Library</span></span><br/> | <dl> <span data-ttu-id="5702f-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5702f-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5702f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5702f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5702f-141">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="5702f-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





