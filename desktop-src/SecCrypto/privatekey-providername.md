---
description: Récupère le nom du fournisseur de services de chiffrement (CSP).
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: PrivateKey. ProviderName, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537674"
---
# <a name="privatekeyprovidername-property"></a><span data-ttu-id="1ba02-103">PrivateKey. ProviderName, propriété</span><span class="sxs-lookup"><span data-stu-id="1ba02-103">PrivateKey.ProviderName property</span></span>

<span data-ttu-id="1ba02-104">\[La propriété **providerName** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1ba02-104">\[The **ProviderName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1ba02-105">Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1ba02-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1ba02-106">La propriété **providerName** récupère le nom du fournisseur de [*services de chiffrement*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="1ba02-106">The **ProviderName** property retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba02-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ba02-107">Syntax</span></span>


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a><span data-ttu-id="1ba02-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1ba02-108">Property value</span></span>

<span data-ttu-id="1ba02-109">Chaîne qui contient le nom du fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="1ba02-109">A string that contains the name of the CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba02-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ba02-110">Requirements</span></span>



| <span data-ttu-id="1ba02-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ba02-111">Requirement</span></span> | <span data-ttu-id="1ba02-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ba02-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba02-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1ba02-113">Redistributable</span></span><br/> | <span data-ttu-id="1ba02-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ba02-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1ba02-115">DLL</span><span class="sxs-lookup"><span data-stu-id="1ba02-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="1ba02-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ba02-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ba02-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ba02-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba02-118">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="1ba02-118">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
