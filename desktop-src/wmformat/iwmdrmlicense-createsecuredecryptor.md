---
title: Méthode IWMDRMLicense CreateSecureDecryptor (wmdrmsdk. h)
description: La méthode CreateSecureDecryptor crée un objet déchiffreur sécurisé. Le déchiffreur sécurisé diffère du déchiffreur normal en ce sens qu’il déchiffre le contenu, puis le chiffre à nouveau en fonction des paramètres spécifiés dans les paramètres de cette méthode.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Méthode CreateSecureDecryptor format Windows Media
- Méthode CreateSecureDecryptor format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode CreateSecureDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538752"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a><span data-ttu-id="366eb-107">IWMDRMLicense :: CreateSecureDecryptor, méthode</span><span class="sxs-lookup"><span data-stu-id="366eb-107">IWMDRMLicense::CreateSecureDecryptor method</span></span>

<span data-ttu-id="366eb-108">La méthode **CreateSecureDecryptor** crée un objet déchiffreur sécurisé.</span><span class="sxs-lookup"><span data-stu-id="366eb-108">The **CreateSecureDecryptor** method creates a secure decryptor object.</span></span> <span data-ttu-id="366eb-109">Le déchiffreur sécurisé diffère du déchiffreur normal en ce sens qu’il déchiffre le contenu, puis le chiffre à nouveau en fonction des paramètres spécifiés dans les paramètres de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="366eb-109">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="366eb-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="366eb-110">Syntax</span></span>


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="366eb-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="366eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="366eb-112">*pbCertificate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="366eb-112">*pbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="366eb-113">Certificat de l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="366eb-113">Certificate of the calling application.</span></span>

</dd> <dt>

<span data-ttu-id="366eb-114">*cbCertificate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="366eb-114">*cbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="366eb-115">Taille du certificat en octets.</span><span class="sxs-lookup"><span data-stu-id="366eb-115">Size of the certificate in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="366eb-116">*dwCertificateType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="366eb-116">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="366eb-117">Type du certificat.</span><span class="sxs-lookup"><span data-stu-id="366eb-117">The type of the certificate.</span></span> <span data-ttu-id="366eb-118">Définissez sur le \_ type de certificat WMDRM \_ \_ XML.</span><span class="sxs-lookup"><span data-stu-id="366eb-118">Set to WMDRM\_CERTIFICATE\_TYPE\_XML.</span></span>

</dd> <dt>

<span data-ttu-id="366eb-119">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="366eb-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="366eb-120">Type de protection de session à utiliser pour le ré-encodage.</span><span class="sxs-lookup"><span data-stu-id="366eb-120">The type of session protection to use for re-encoding.</span></span> <span data-ttu-id="366eb-121">Doit être défini sur l’une des constantes dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="366eb-121">Must be set to one of the constants in the following table:</span></span>



| <span data-ttu-id="366eb-122">Constante</span><span class="sxs-lookup"><span data-stu-id="366eb-122">Constant</span></span>                     | <span data-ttu-id="366eb-123">Description</span><span class="sxs-lookup"><span data-stu-id="366eb-123">Description</span></span>                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="366eb-124">\_Type de protection WMDRM \_ \_ RC4</span><span class="sxs-lookup"><span data-stu-id="366eb-124">WMDRM\_PROTECTION\_TYPE\_RC4</span></span> | <span data-ttu-id="366eb-125">Utilise le chiffrement RC4 pour le chiffrement de session.</span><span class="sxs-lookup"><span data-stu-id="366eb-125">Uses RC4 encryption for session encryption.</span></span> <span data-ttu-id="366eb-126">Il s’agit de la seule protection de session prise en charge pour cette version.</span><span class="sxs-lookup"><span data-stu-id="366eb-126">This is the only supported session protection for this version.</span></span> |



 

</dd> <dt>

<span data-ttu-id="366eb-127">*pbInitializationVector* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="366eb-127">*pbInitializationVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="366eb-128">Reçoit le vecteur d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="366eb-128">Receives the initialization vector.</span></span> <span data-ttu-id="366eb-129">Le vecteur d’initialisation est chiffré par RSA à l’aide du schéma de remplissage OAEP avec la clé publique RSA trouvée dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="366eb-129">The initialization vector is RSA encrypted using the OAEP padding scheme with the RSA public key found in the certificate.</span></span> <span data-ttu-id="366eb-130">Affectez la valeur **null** pour recevoir la taille de mémoire tampon requise dans *pcbInitializationVector*.</span><span class="sxs-lookup"><span data-stu-id="366eb-130">Set to **NULL** to receive the required buffer size in *pcbInitializationVector*.</span></span>

</dd> <dt>

<span data-ttu-id="366eb-131">*pcbInitializationVector* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="366eb-131">*pcbInitializationVector* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="366eb-132">En entrée, taille de la mémoire tampon transmise en tant que *pbInitializationVector*.</span><span class="sxs-lookup"><span data-stu-id="366eb-132">On input, the size of the buffer passed as *pbInitializationVector*.</span></span> <span data-ttu-id="366eb-133">À la sortie, taille de la partie utilisée de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="366eb-133">On output, the size of the used portion of the buffer.</span></span> <span data-ttu-id="366eb-134">Si vous transmettez la valeur **null** pour *pbInitializationVector*, cette valeur est définie sur la taille de mémoire tampon requise sur la sortie.</span><span class="sxs-lookup"><span data-stu-id="366eb-134">If you pass **NULL** for *pbInitializationVector*, this value is set to the required buffer size on output.</span></span>

</dd> <dt>

<span data-ttu-id="366eb-135">*ppDecryptor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="366eb-135">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="366eb-136">Reçoit un pointeur vers l’interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) de l’objet nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="366eb-136">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="366eb-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="366eb-137">Return value</span></span>

<span data-ttu-id="366eb-138">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="366eb-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="366eb-139">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="366eb-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="366eb-140">Code de retour</span><span class="sxs-lookup"><span data-stu-id="366eb-140">Return code</span></span>                                                                          | <span data-ttu-id="366eb-141">Description</span><span class="sxs-lookup"><span data-stu-id="366eb-141">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="366eb-142"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="366eb-142"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="366eb-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="366eb-143">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="366eb-144">Notes</span><span class="sxs-lookup"><span data-stu-id="366eb-144">Remarks</span></span>

<span data-ttu-id="366eb-145">Aucun.</span><span class="sxs-lookup"><span data-stu-id="366eb-145">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="366eb-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="366eb-146">Requirements</span></span>



| <span data-ttu-id="366eb-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="366eb-147">Requirement</span></span> | <span data-ttu-id="366eb-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="366eb-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="366eb-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="366eb-149">Header</span></span><br/> | <dl> <span data-ttu-id="366eb-150"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="366eb-150"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="366eb-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="366eb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="366eb-152">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="366eb-152">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





