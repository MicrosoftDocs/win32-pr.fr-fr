---
description: Retourne une valeur booléenne qui indique si la clé privée peut être exportée.
ms.assetid: 56e72747-126d-4bb4-ac10-ced0acef388b
title: Méthode PrivateKey. IsExportable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsExportable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6aef50091652bcc1294f7feaee44efe75174b6e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532611"
---
# <a name="privatekeyisexportable-method"></a><span data-ttu-id="20a14-103">Méthode PrivateKey. IsExportable</span><span class="sxs-lookup"><span data-stu-id="20a14-103">PrivateKey.IsExportable method</span></span>

<span data-ttu-id="20a14-104">\[La méthode **IsExportable** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="20a14-104">\[The **IsExportable** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="20a14-105">Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="20a14-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="20a14-106">La méthode **IsExportable** retourne une valeur booléenne qui indique si la clé privée peut être exportée.</span><span class="sxs-lookup"><span data-stu-id="20a14-106">The **IsExportable** method returns a Boolean value that indicates whether the private key is exportable.</span></span>

## <a name="syntax"></a><span data-ttu-id="20a14-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20a14-107">Syntax</span></span>


```VB
PrivateKey.IsExportable()
```



## <a name="parameters"></a><span data-ttu-id="20a14-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20a14-108">Parameters</span></span>

<span data-ttu-id="20a14-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="20a14-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20a14-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20a14-110">Return value</span></span>

<span data-ttu-id="20a14-111">Si la valeur est true, la clé privée est marquée comme exportable.</span><span class="sxs-lookup"><span data-stu-id="20a14-111">If true, the private key is marked exportable.</span></span>

## <a name="remarks"></a><span data-ttu-id="20a14-112">Notes</span><span class="sxs-lookup"><span data-stu-id="20a14-112">Remarks</span></span>

<span data-ttu-id="20a14-113">La valeur de retour de cette méthode dépend du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) utilisé.</span><span class="sxs-lookup"><span data-stu-id="20a14-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="20a14-114">Cette méthode renvoie une valeur fiable si un fournisseur de services de chiffrement Microsoft est utilisé.</span><span class="sxs-lookup"><span data-stu-id="20a14-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="20a14-115">Si le fournisseur de services de chiffrement n’est pas un fournisseur de services de chiffrement Microsoft, la valeur de retour ne peut pas être approuvée.</span><span class="sxs-lookup"><span data-stu-id="20a14-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="20a14-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20a14-116">Requirements</span></span>



| <span data-ttu-id="20a14-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20a14-117">Requirement</span></span> | <span data-ttu-id="20a14-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="20a14-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20a14-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="20a14-119">Redistributable</span></span><br/> | <span data-ttu-id="20a14-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="20a14-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="20a14-121">DLL</span><span class="sxs-lookup"><span data-stu-id="20a14-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="20a14-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20a14-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20a14-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20a14-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a14-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="20a14-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
