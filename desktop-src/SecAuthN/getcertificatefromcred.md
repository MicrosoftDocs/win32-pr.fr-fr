---
description: Obtient le certificat à partir des informations d’identification de l’utilisateur.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: GetCertificateFromCred, fonction (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531878"
---
# <a name="getcertificatefromcred-function"></a><span data-ttu-id="5ea6e-103">GetCertificateFromCred fonction)</span><span class="sxs-lookup"><span data-stu-id="5ea6e-103">GetCertificateFromCred function</span></span>

<span data-ttu-id="5ea6e-104">Obtient le certificat à partir des informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-104">Gets the certificate from the user credential.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea6e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ea6e-105">Syntax</span></span>


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a><span data-ttu-id="5ea6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ea6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea6e-107">*ProviderHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ea6e-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea6e-108">Descripteur de fournisseur d’identité.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="5ea6e-109">*ClientToken* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ea6e-109">*ClientToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea6e-110">Jeton de l’appelant qui récupère le certificat.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-110">Token of the caller who is retrieving the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="5ea6e-111">*SuppliedCred* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ea6e-111">*SuppliedCred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea6e-112">Pointeur vers une structure [**\_ \_ d’informations d’identification fournie par SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) qui contient les informations d’identification d’un ID en ligne dont le certificat est demandé.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-112">A pointer to a [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure that contains the credential of an online ID whose certificate is requested.</span></span> <span data-ttu-id="5ea6e-113">Le fournisseur d’identité doit valider les données d’entrée comme s’il s’agissait d’une source non fiable.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-113">The identity provider must validate the input data as if it is coming from an untrusted source.</span></span>

</dd> <dt>

<span data-ttu-id="5ea6e-114">*SuppliedCredSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ea6e-114">*SuppliedCredSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea6e-115">Taille, en octets, de la mémoire tampon *SuppliedCred* .</span><span class="sxs-lookup"><span data-stu-id="5ea6e-115">The size, in bytes, of the *SuppliedCred* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5ea6e-116">*CertContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5ea6e-116">*CertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea6e-117">Si la fonction est réussie, ce paramètre est un pointeur vers le pointeur de \_ contexte CCERT retourné.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-117">If the function succeeds, this parameter is a pointer to the returned CCERT\_CONTEXT pointer.</span></span> <span data-ttu-id="5ea6e-118">Lorsque vous avez terminé d’utiliser le contexte de certificat, libérez-le en appelant la fonction [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="5ea6e-118">When you have finished using the certificate context, release it by calling the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea6e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ea6e-119">Return value</span></span>

<span data-ttu-id="5ea6e-120">Si la fonction réussit, la fonction retourne l’état \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-120">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="5ea6e-121">Si la fonction échoue, la fonction peut retourner l’un des codes d’erreur NTSTATUS suivants.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-121">If the function fails, the function may return one of the following NTSTATUS error codes.</span></span>



| <span data-ttu-id="5ea6e-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ea6e-122">Return value</span></span>                                                                                            | <span data-ttu-id="5ea6e-123">Description</span><span class="sxs-lookup"><span data-stu-id="5ea6e-123">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ea6e-124"><dt>ÉTAT \_ non \_ pris en charge</dt></span><span class="sxs-lookup"><span data-stu-id="5ea6e-124"><dt>STATUS\_NOT\_SUPPORTED</dt></span></span> </dl>       | <span data-ttu-id="5ea6e-125">Le fournisseur d’identité ne reconnaît pas le type d’informations d’identification des informations d’identification fournies.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-125">The identity provider does not recognize the credential type of the supplied credential.</span></span> <span data-ttu-id="5ea6e-126">LSA essaiera le fournisseur d’identité suivant.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-126">LSA will try the next identity provider.</span></span><br/>                                           |
| <dl> <span data-ttu-id="5ea6e-127"><dt>\_échec d’ouverture de session \_</dt></span><span class="sxs-lookup"><span data-stu-id="5ea6e-127"><dt>STATUS\_LOGON\_FAILURE</dt></span></span> </dl>       | <span data-ttu-id="5ea6e-128">Les informations d’identification sont incorrectes.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-128">The credential is incorrect.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="5ea6e-129"><dt>paramètre d’état \_ non valide \_</dt></span><span class="sxs-lookup"><span data-stu-id="5ea6e-129"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>   | <span data-ttu-id="5ea6e-130">Un paramètre n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-130">A parameter is not valid.</span></span> <span data-ttu-id="5ea6e-131">Les informations d’identification peuvent être dans un format incorrect et non dans la structure [**\_ \_ d’informations d’identification fournie**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) par le SECPKG défini.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-131">The credential may be in an incorrect format and not in the defined [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure.</span></span><br/> |
| <dl> <span data-ttu-id="5ea6e-132"><dt>ÉTAT \_ réseau \_ inaccessible</dt></span><span class="sxs-lookup"><span data-stu-id="5ea6e-132"><dt>STATUS\_NETWORK\_UNREACHABLE</dt></span></span> </dl> | <span data-ttu-id="5ea6e-133">Le fournisseur d’identité ne peut pas contacter le Cloud pour obtenir le certificat.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-133">The identity provider cannot contact the cloud to obtain the certificate.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="5ea6e-134"><dt>\_mot de passe d’état \_ expiré</dt></span><span class="sxs-lookup"><span data-stu-id="5ea6e-134"><dt>STATUS\_PASSWORD\_EXPIRED</dt></span></span> </dl>    | <span data-ttu-id="5ea6e-135">Le mot de passe du compte a expiré.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-135">The account password has expired.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="5ea6e-136"><dt>compte d’état \_ \_ verrouillé \_</dt></span><span class="sxs-lookup"><span data-stu-id="5ea6e-136"><dt>STATUS\_ACCOUNT\_LOCKED\_OUT</dt></span></span> </dl> | <span data-ttu-id="5ea6e-137">Le compte a été verrouillé.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-137">The account has been locked out.</span></span> <br/>                                                                                                                                           |
| <dl> <span data-ttu-id="5ea6e-138"><dt>Autres</dt></span><span class="sxs-lookup"><span data-stu-id="5ea6e-138"><dt>Others</dt></span></span> </dl>                       | <span data-ttu-id="5ea6e-139">Autres codes d’erreur spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-139">Other provider-specific error codes.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="5ea6e-140">Notes</span><span class="sxs-lookup"><span data-stu-id="5ea6e-140">Remarks</span></span>

<span data-ttu-id="5ea6e-141">Avant d’extraire le certificat du Cloud, le fournisseur d’identité doit vérifier qu’il existe un certificat valide pour cet utilisateur dans le magasin de certificats « MY » de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-141">Before fetching the certificate from the cloud, the identity provider should check that there is a valid certificate for this user in the user's "MY" certificate store.</span></span> <span data-ttu-id="5ea6e-142">Si un certificat valide existe, le fournisseur doit retourner ce certificat pour éviter tout trafic réseau inutile.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-142">If a valid certificate exists, the provider should return this certificate to avoid unnecessary network traffic.</span></span>

<span data-ttu-id="5ea6e-143">Le fournisseur d’identité peut également mettre en cache le certificat localement tant qu’il est protégé par l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-143">The identity provider can also cache the certificate locally as long as it is protected from the current user.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea6e-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ea6e-144">Requirements</span></span>



| <span data-ttu-id="5ea6e-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ea6e-145">Requirement</span></span> | <span data-ttu-id="5ea6e-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ea6e-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea6e-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ea6e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea6e-148">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ea6e-148">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5ea6e-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ea6e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea6e-150">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ea6e-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5ea6e-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ea6e-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ea6e-152"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ea6e-152"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

