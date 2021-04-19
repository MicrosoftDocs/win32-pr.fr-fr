---
title: Méthode IWMDRMSecurity GetMachineCertificate (wmdrmsdk. h)
description: La méthode GetMachineCertificate récupère le certificat de l’ordinateur du sous-système DRM sur l’ordinateur client.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Méthode GetMachineCertificate format Windows Media
- Méthode GetMachineCertificate format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetMachineCertificate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540434"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a><span data-ttu-id="32022-106">IWMDRMSecurity :: GetMachineCertificate, méthode</span><span class="sxs-lookup"><span data-stu-id="32022-106">IWMDRMSecurity::GetMachineCertificate method</span></span>

<span data-ttu-id="32022-107">La méthode **GetMachineCertificate** récupère le certificat de l’ordinateur du sous-système DRM sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="32022-107">The **GetMachineCertificate** method retrieves the machine certificate of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="32022-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32022-108">Syntax</span></span>


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="32022-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32022-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32022-110">*dwCertificateType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32022-110">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32022-111">Type de certificat à récupérer.</span><span class="sxs-lookup"><span data-stu-id="32022-111">Type of certificate to retrieve.</span></span> <span data-ttu-id="32022-112">Définissez l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="32022-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="32022-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="32022-113">Value</span></span>                        | <span data-ttu-id="32022-114">Description</span><span class="sxs-lookup"><span data-stu-id="32022-114">Description</span></span>                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32022-115">\_Type de certificat WMDRM \_ \_ v1</span><span class="sxs-lookup"><span data-stu-id="32022-115">WMDRM\_CERTIFICATE\_TYPE\_V1</span></span> | <span data-ttu-id="32022-116">Le certificat sera récupéré dans le format utilisé par les composants hérités.</span><span class="sxs-lookup"><span data-stu-id="32022-116">The certificate will be retrieved in the format used by legacy components.</span></span>            |
| <span data-ttu-id="32022-117">\_Type de certificat WMDRM \_ \_ v2</span><span class="sxs-lookup"><span data-stu-id="32022-117">WMDRM\_CERTIFICATE\_TYPE\_V2</span></span> | <span data-ttu-id="32022-118">Le certificat sera récupéré dans le format utilisé par les composants de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32022-118">The certificate will be retrieved in the format used by the Windows Vista components.</span></span> |



 

</dd> <dt>

<span data-ttu-id="32022-119">*rgbVersion \[ 4 \]* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="32022-119">*rgbVersion\[4\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32022-120">Tableau de quatre octets spécifiant la version du sous-système DRM sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="32022-120">Array of four bytes specifying the version of the DRM subsystem on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="32022-121">*ppbCertificate* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="32022-121">*ppbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32022-122">Adresse d’une variable qui reçoit un pointeur vers les données du certificat.</span><span class="sxs-lookup"><span data-stu-id="32022-122">Address of a variable that receives a pointer to the certificate data.</span></span> <span data-ttu-id="32022-123">Affectez la valeur **null** pour que la méthode fournisse la taille de mémoire tampon nécessaire pour contenir le certificat dans *pcbCertificate*.</span><span class="sxs-lookup"><span data-stu-id="32022-123">Set to **NULL** to have the method provide the buffer size required to hold the certificate in *pcbCertificate*.</span></span>

</dd> <dt>

<span data-ttu-id="32022-124">*pcbCertificate* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="32022-124">*pcbCertificate* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32022-125">Taille du certificat en octets.</span><span class="sxs-lookup"><span data-stu-id="32022-125">Size of the certificate in bytes.</span></span> <span data-ttu-id="32022-126">Si *ppbCertificate* a la valeur **null**, cette valeur sera définie sur la taille du certificat.</span><span class="sxs-lookup"><span data-stu-id="32022-126">If *ppbCertificate* is **NULL**, this value will be set to the size of the certificate.</span></span> <span data-ttu-id="32022-127">Si *ppbCertificate* n’a pas la valeur **null**, cette valeur doit être définie sur la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="32022-127">If *ppbCertificate* is not **NULL**, this value must be set to the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32022-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32022-128">Return value</span></span>

<span data-ttu-id="32022-129">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="32022-129">The method returns an **HRESULT**.</span></span> <span data-ttu-id="32022-130">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="32022-130">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="32022-131">Code de retour</span><span class="sxs-lookup"><span data-stu-id="32022-131">Return code</span></span>                                                                          | <span data-ttu-id="32022-132">Description</span><span class="sxs-lookup"><span data-stu-id="32022-132">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="32022-133"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="32022-133"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="32022-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="32022-134">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="32022-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32022-135">Requirements</span></span>



| <span data-ttu-id="32022-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32022-136">Requirement</span></span> | <span data-ttu-id="32022-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="32022-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32022-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="32022-138">Header</span></span><br/>  | <dl> <span data-ttu-id="32022-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="32022-139"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="32022-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="32022-140">Library</span></span><br/> | <dl> <span data-ttu-id="32022-141"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32022-141"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32022-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32022-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32022-143">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="32022-143">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





