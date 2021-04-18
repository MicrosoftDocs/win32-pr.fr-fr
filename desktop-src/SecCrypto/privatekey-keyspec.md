---
description: Récupère la spécification de clé.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: PrivateKey. KeySpec, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528922"
---
# <a name="privatekeykeyspec-property"></a><span data-ttu-id="29df4-103">PrivateKey. KeySpec, propriété</span><span class="sxs-lookup"><span data-stu-id="29df4-103">PrivateKey.KeySpec property</span></span>

<span data-ttu-id="29df4-104">\[La propriété **KeySpec** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="29df4-104">\[The **KeySpec** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="29df4-105">Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="29df4-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="29df4-106">La propriété **KeySpec** récupère la spécification de la clé.</span><span class="sxs-lookup"><span data-stu-id="29df4-106">The **KeySpec** property retrieves the key specification.</span></span>

## <a name="syntax"></a><span data-ttu-id="29df4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29df4-107">Syntax</span></span>


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a><span data-ttu-id="29df4-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="29df4-108">Property value</span></span>

<span data-ttu-id="29df4-109">Valeur de l’énumération des [**\_ \_ spécifications de clé CAPICOM**](capicom-key-spec.md) qui indique la spécification de clé.</span><span class="sxs-lookup"><span data-stu-id="29df4-109">A value of the [**CAPICOM\_KEY\_SPEC**](capicom-key-spec.md) enumeration that indicates the key specification.</span></span> <span data-ttu-id="29df4-110">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="29df4-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="29df4-111">Value</span><span class="sxs-lookup"><span data-stu-id="29df4-111">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="29df4-112">Signification</span><span class="sxs-lookup"><span data-stu-id="29df4-112">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <span data-ttu-id="29df4-113"><dt>**clé d’échange de la \_ spécification de clé CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="29df4-113"><dt>**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</dt></span></span> </dl> | <span data-ttu-id="29df4-114">La clé peut être utilisée pour le chiffrement et la signature.</span><span class="sxs-lookup"><span data-stu-id="29df4-114">The key can be used for encryption and signing.</span></span><br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <span data-ttu-id="29df4-115"><dt>**SIGNATURE de la \_ spécification de clé CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="29df4-115"><dt>**CAPICOM\_KEY\_SPEC\_SIGNATURE**</dt></span></span> </dl>       | <span data-ttu-id="29df4-116">La clé peut être utilisée uniquement pour la signature.</span><span class="sxs-lookup"><span data-stu-id="29df4-116">The key can be used only for signing.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="29df4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29df4-117">Requirements</span></span>



| <span data-ttu-id="29df4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29df4-118">Requirement</span></span> | <span data-ttu-id="29df4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="29df4-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29df4-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="29df4-120">Redistributable</span></span><br/> | <span data-ttu-id="29df4-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="29df4-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="29df4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="29df4-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="29df4-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29df4-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29df4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29df4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29df4-125">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="29df4-125">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
