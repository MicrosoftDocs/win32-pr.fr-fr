---
description: Retourne une valeur booléenne qui indique si la clé privée est protégée.
ms.assetid: 6a329581-0ff8-45fa-9997-5fcf043287cb
title: Méthode PrivateKey. IsProtected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsProtected
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33ba72935b2c3f9f9cf537469e043160f9ce2d7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543261"
---
# <a name="privatekeyisprotected-method"></a><span data-ttu-id="9b11f-103">Méthode PrivateKey. IsProtected</span><span class="sxs-lookup"><span data-stu-id="9b11f-103">PrivateKey.IsProtected method</span></span>

<span data-ttu-id="9b11f-104">\[La méthode **IsProtected** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="9b11f-104">\[The **IsProtected** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9b11f-105">Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9b11f-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9b11f-106">La méthode **IsProtected** retourne une valeur booléenne qui indique si la clé privée est protégée.</span><span class="sxs-lookup"><span data-stu-id="9b11f-106">The **IsProtected** method returns a Boolean value that indicates whether the private key is protected.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b11f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b11f-107">Syntax</span></span>


```VB
PrivateKey.IsProtected()
```



## <a name="parameters"></a><span data-ttu-id="9b11f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b11f-108">Parameters</span></span>

<span data-ttu-id="9b11f-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9b11f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b11f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b11f-110">Return value</span></span>

<span data-ttu-id="9b11f-111">Si la valeur est true, la clé privée est protégée.</span><span class="sxs-lookup"><span data-stu-id="9b11f-111">If true, the private key is protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b11f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9b11f-112">Remarks</span></span>

<span data-ttu-id="9b11f-113">La valeur de retour de cette méthode dépend du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) utilisé.</span><span class="sxs-lookup"><span data-stu-id="9b11f-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="9b11f-114">Cette méthode renvoie une valeur fiable si un fournisseur de services de chiffrement Microsoft est utilisé.</span><span class="sxs-lookup"><span data-stu-id="9b11f-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="9b11f-115">Si le fournisseur de services de chiffrement n’est pas un fournisseur de services de chiffrement Microsoft, la valeur de retour ne peut pas être approuvée.</span><span class="sxs-lookup"><span data-stu-id="9b11f-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b11f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b11f-116">Requirements</span></span>



| <span data-ttu-id="9b11f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b11f-117">Requirement</span></span> | <span data-ttu-id="9b11f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b11f-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b11f-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9b11f-119">Redistributable</span></span><br/> | <span data-ttu-id="9b11f-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="9b11f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9b11f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9b11f-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="9b11f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b11f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b11f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b11f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b11f-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="9b11f-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
