---
title: Méthode IWMDRMSecurity CheckCertForRevocation (wmdrmsdk. h)
description: La méthode CheckCertForRevocation détermine si un certificat a été révoqué.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Méthode CheckCertForRevocation format Windows Media
- Méthode CheckCertForRevocation format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode CheckCertForRevocation
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528427"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a><span data-ttu-id="7bbfc-106">IWMDRMSecurity :: CheckCertForRevocation, méthode</span><span class="sxs-lookup"><span data-stu-id="7bbfc-106">IWMDRMSecurity::CheckCertForRevocation method</span></span>

<span data-ttu-id="7bbfc-107">La méthode **CheckCertForRevocation** détermine si un certificat a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-107">The **CheckCertForRevocation** method determines whether a certificate has been revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbfc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bbfc-108">Syntax</span></span>


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a><span data-ttu-id="7bbfc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7bbfc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bbfc-110">*rguidRevocationList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7bbfc-110">*rguidRevocationList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbfc-111">GUID identifiant la liste de révocation à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-111">GUID identifying the revocation list to use.</span></span> <span data-ttu-id="7bbfc-112">Définissez l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="7bbfc-113">GUID, constante</span><span class="sxs-lookup"><span data-stu-id="7bbfc-113">GUID constant</span></span>                 | <span data-ttu-id="7bbfc-114">Description</span><span class="sxs-lookup"><span data-stu-id="7bbfc-114">Description</span></span>                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbfc-115">\_application REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="7bbfc-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="7bbfc-116">Spécifie la liste de révocation des certificats d’application.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-116">Specifies the application certificate revocation list.</span></span>                                     |
| <span data-ttu-id="7bbfc-117">\_appareil REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="7bbfc-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="7bbfc-118">Spécifie la liste de révocation de certificats de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-118">Specifies the device certificate revocation list.</span></span>                                          |
| <span data-ttu-id="7bbfc-119">\_REVOCATIONTYPE WMDRM \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="7bbfc-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="7bbfc-120">Spécifie la liste de révocation de certificats de Microsoft Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-120">Specifies the Microsoft Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7bbfc-121">*pbCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7bbfc-121">*pbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbfc-122">Mémoire tampon contenant le certificat à rechercher.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-122">Buffer containing the certificate to look up.</span></span>

</dd> <dt>

<span data-ttu-id="7bbfc-123">*cbCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7bbfc-123">*cbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbfc-124">Taille de la mémoire tampon *pbCert*, en octets.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-124">Size of the buffer *pbCert*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7bbfc-125">*fRevoked* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7bbfc-125">*fRevoked* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbfc-126">Lors de la sortie, indique si le certificat est présent dans la liste de révocation.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-126">On output, indicates whether the certificate is present in the revocation list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bbfc-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7bbfc-127">Return value</span></span>

<span data-ttu-id="7bbfc-128">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7bbfc-129">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7bbfc-130">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7bbfc-130">Return code</span></span>                                                                          | <span data-ttu-id="7bbfc-131">Description</span><span class="sxs-lookup"><span data-stu-id="7bbfc-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7bbfc-132"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7bbfc-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="7bbfc-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7bbfc-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bbfc-134">Requirements</span></span>



| <span data-ttu-id="7bbfc-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bbfc-135">Requirement</span></span> | <span data-ttu-id="7bbfc-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bbfc-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbfc-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="7bbfc-137">Header</span></span><br/>  | <dl> <span data-ttu-id="7bbfc-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="7bbfc-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7bbfc-139">Library</span></span><br/> | <dl> <span data-ttu-id="7bbfc-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bbfc-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bbfc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbfc-142">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="7bbfc-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





