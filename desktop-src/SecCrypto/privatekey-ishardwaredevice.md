---
description: Retourne une valeur booléenne qui indique si la clé privée est stockée dans un périphérique matériel.
ms.assetid: 9a06f598-55cd-441b-a85f-8bec299f8245
title: Méthode PrivateKey. IsHardwareDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsHardwareDevice
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23b6fd379fd3a3b53fe0600dbf28481cd5ef2f86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530366"
---
# <a name="privatekeyishardwaredevice-method"></a><span data-ttu-id="87a16-103">Méthode PrivateKey. IsHardwareDevice</span><span class="sxs-lookup"><span data-stu-id="87a16-103">PrivateKey.IsHardwareDevice method</span></span>

<span data-ttu-id="87a16-104">\[La méthode **IsHardwareDevice** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="87a16-104">\[The **IsHardwareDevice** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="87a16-105">Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="87a16-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="87a16-106">La méthode **IsHardwareDevice** retourne une valeur booléenne qui indique si la clé privée est stockée dans un périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="87a16-106">The **IsHardwareDevice** method returns a Boolean value that indicates whether the private key is stored in a hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a16-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87a16-107">Syntax</span></span>


```VB
PrivateKey.IsHardwareDevice()
```



## <a name="parameters"></a><span data-ttu-id="87a16-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87a16-108">Parameters</span></span>

<span data-ttu-id="87a16-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="87a16-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87a16-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87a16-110">Return value</span></span>

<span data-ttu-id="87a16-111">Si la valeur est true, la clé privée est stockée dans un périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="87a16-111">If true, the private key is stored in a hardware device.</span></span>

## <a name="remarks"></a><span data-ttu-id="87a16-112">Notes</span><span class="sxs-lookup"><span data-stu-id="87a16-112">Remarks</span></span>

<span data-ttu-id="87a16-113">La valeur de retour de cette méthode dépend du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) utilisé.</span><span class="sxs-lookup"><span data-stu-id="87a16-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="87a16-114">Cette méthode renvoie une valeur fiable si un fournisseur de services de chiffrement Microsoft est utilisé.</span><span class="sxs-lookup"><span data-stu-id="87a16-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="87a16-115">Si le fournisseur de services de chiffrement n’est pas un fournisseur de services de chiffrement Microsoft, la valeur de retour ne peut pas être approuvée.</span><span class="sxs-lookup"><span data-stu-id="87a16-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="87a16-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87a16-116">Requirements</span></span>



| <span data-ttu-id="87a16-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87a16-117">Requirement</span></span> | <span data-ttu-id="87a16-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="87a16-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87a16-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="87a16-119">Redistributable</span></span><br/> | <span data-ttu-id="87a16-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="87a16-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="87a16-121">DLL</span><span class="sxs-lookup"><span data-stu-id="87a16-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="87a16-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87a16-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87a16-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87a16-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a16-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="87a16-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
