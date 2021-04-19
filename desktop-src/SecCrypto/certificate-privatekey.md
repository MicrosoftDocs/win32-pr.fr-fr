---
description: Définit ou récupère la clé privée associée au certificat.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Propriété Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537928"
---
# <a name="certificateprivatekey-property"></a><span data-ttu-id="9114e-103">Propriété Certificate. PrivateKey</span><span class="sxs-lookup"><span data-stu-id="9114e-103">Certificate.PrivateKey property</span></span>

<span data-ttu-id="9114e-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9114e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9114e-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9114e-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9114e-106">La propriété **PrivateKey** définit ou récupère la clé privée associée au certificat.</span><span class="sxs-lookup"><span data-stu-id="9114e-106">The **PrivateKey** property sets or retrieves the private key associated with the certificate.</span></span> <span data-ttu-id="9114e-107">Cette propriété a été introduite dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9114e-107">This property was introduced in CAPICOM 2.0.</span></span>

<span data-ttu-id="9114e-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9114e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9114e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9114e-109">Syntax</span></span>


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a><span data-ttu-id="9114e-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9114e-110">Property value</span></span>

<span data-ttu-id="9114e-111">Objet [**PrivateKey**](privatekey.md) qui représente la clé privée associée au certificat.</span><span class="sxs-lookup"><span data-stu-id="9114e-111">A [**PrivateKey**](privatekey.md) object that represents the private key that is associated with the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="9114e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9114e-112">Remarks</span></span>

<span data-ttu-id="9114e-113">La définition de la propriété **PrivateKey** sur Nothing supprime l’association entre la clé privée et le certificat, mais elle ne supprime pas la clé privée.</span><span class="sxs-lookup"><span data-stu-id="9114e-113">Setting the **PrivateKey** property to Nothing removes the association between the private key and the certificate, but it does not delete the private key.</span></span> <span data-ttu-id="9114e-114">Pour supprimer la clé privée, appelez la méthode [**PrivateKey. Delete**](privatekey-delete.md) , puis affectez à cette propriété la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="9114e-114">To delete the private key, call the [**PrivateKey.Delete**](privatekey-delete.md) method, and then set this property to Nothing.</span></span>

<span data-ttu-id="9114e-115">Cette propriété déclenche l’E CAPICOM \_ E \_ non \_ autorisée quand elle est définie à partir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="9114e-115">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is set from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="9114e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9114e-116">Requirements</span></span>



| <span data-ttu-id="9114e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9114e-117">Requirement</span></span> | <span data-ttu-id="9114e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9114e-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9114e-119">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9114e-119">End of client support</span></span><br/> | <span data-ttu-id="9114e-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9114e-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9114e-121">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9114e-121">End of server support</span></span><br/> | <span data-ttu-id="9114e-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9114e-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9114e-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9114e-123">Redistributable</span></span><br/>       | <span data-ttu-id="9114e-124">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="9114e-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9114e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9114e-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9114e-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9114e-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9114e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9114e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9114e-128">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="9114e-128">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
