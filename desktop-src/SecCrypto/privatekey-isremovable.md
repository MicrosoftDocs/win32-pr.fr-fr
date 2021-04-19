---
description: Retourne une valeur booléenne qui indique si la clé privée est dans un stockage amovible.
ms.assetid: 9371d7cf-65b2-4c0f-a387-195a058d6a8b
title: Méthode PrivateKey. IsRemovable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsRemovable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6684d40302746a736701b824685a54faeff5354a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542664"
---
# <a name="privatekeyisremovable-method"></a><span data-ttu-id="ac743-103">Méthode PrivateKey. IsRemovable</span><span class="sxs-lookup"><span data-stu-id="ac743-103">PrivateKey.IsRemovable method</span></span>

<span data-ttu-id="ac743-104">\[La méthode **IsRemovable** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ac743-104">\[The **IsRemovable** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ac743-105">Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ac743-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ac743-106">La méthode **IsRemovable** retourne une valeur booléenne qui indique si la clé privée est dans un stockage amovible.</span><span class="sxs-lookup"><span data-stu-id="ac743-106">The **IsRemovable** method returns a Boolean value that indicates whether the private key is in removable storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac743-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac743-107">Syntax</span></span>


```VB
PrivateKey.IsRemovable()
```



## <a name="parameters"></a><span data-ttu-id="ac743-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac743-108">Parameters</span></span>

<span data-ttu-id="ac743-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ac743-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac743-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac743-110">Return value</span></span>

<span data-ttu-id="ac743-111">Si la valeur est true, la clé privée est dans un stockage amovible.</span><span class="sxs-lookup"><span data-stu-id="ac743-111">If true, the private key is in removable storage.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac743-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ac743-112">Remarks</span></span>

<span data-ttu-id="ac743-113">La valeur de retour de cette méthode dépend du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) utilisé.</span><span class="sxs-lookup"><span data-stu-id="ac743-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="ac743-114">Cette méthode renvoie une valeur fiable si un fournisseur de services de chiffrement Microsoft est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ac743-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="ac743-115">Si le fournisseur de services de chiffrement n’est pas un fournisseur de services de chiffrement Microsoft, la valeur de retour ne peut pas être approuvée.</span><span class="sxs-lookup"><span data-stu-id="ac743-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac743-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac743-116">Requirements</span></span>



| <span data-ttu-id="ac743-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac743-117">Requirement</span></span> | <span data-ttu-id="ac743-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac743-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac743-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ac743-119">Redistributable</span></span><br/> | <span data-ttu-id="ac743-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac743-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ac743-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ac743-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="ac743-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac743-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac743-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac743-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac743-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="ac743-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
