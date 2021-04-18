---
description: Récupère le nombre d’objets de certificat dans la collection.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Propriété Certificates. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540286"
---
# <a name="certificatescount-property"></a><span data-ttu-id="aaf76-103">Propriété Certificates. Count</span><span class="sxs-lookup"><span data-stu-id="aaf76-103">Certificates.Count property</span></span>

<span data-ttu-id="aaf76-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aaf76-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="aaf76-105">Utilisez plutôt la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="aaf76-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="aaf76-106">La propriété **Count** récupère le nombre d’objets de [**certificat**](certificate.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="aaf76-106">The **Count** property retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf76-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaf76-107">Syntax</span></span>


```VB
Certificates.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="aaf76-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="aaf76-108">Property value</span></span>

<span data-ttu-id="aaf76-109">Nombre d’objets de [**certificat**](certificate.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="aaf76-109">The number of [**Certificate**](certificate.md) objects in the collection.</span></span> <span data-ttu-id="aaf76-110">Chaque objet de **certificat** représente un certificat unique dans la collection.</span><span class="sxs-lookup"><span data-stu-id="aaf76-110">Each **Certificate** object represents a single certificate in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaf76-111">Notes</span><span class="sxs-lookup"><span data-stu-id="aaf76-111">Remarks</span></span>

<span data-ttu-id="aaf76-112">CAPICOM ne prend en charge qu’un seul certificat pour le magasin de [*cartes à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="aaf76-112">CAPICOM only supports a single certificate for the [*smart card*](../secgloss/s-gly.md) store.</span></span> <span data-ttu-id="aaf76-113">Même si le magasin de cartes à puce contient plus d’un certificat, cette propriété contient 1.</span><span class="sxs-lookup"><span data-stu-id="aaf76-113">Even if the smart card store contains more than one certificate, this property will contain 1.</span></span> <span data-ttu-id="aaf76-114">Pour plus d’informations sur le magasin de cartes à puce, consultez le membre du **\_ \_ \_ \_ magasin utilisateur de la carte à puce** CAPICOM de l’énumération [**\_ \_ emplacement du magasin CAPICOM**](capicom-store-location.md) .</span><span class="sxs-lookup"><span data-stu-id="aaf76-114">For more information about the smart card store, see the **CAPICOM\_SMART\_CARD\_USER\_STORE** member of the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaf76-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaf76-115">Requirements</span></span>



| <span data-ttu-id="aaf76-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaf76-116">Requirement</span></span> | <span data-ttu-id="aaf76-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaf76-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf76-118">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="aaf76-118">End of client support</span></span><br/> | <span data-ttu-id="aaf76-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aaf76-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aaf76-120">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="aaf76-120">End of server support</span></span><br/> | <span data-ttu-id="aaf76-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aaf76-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aaf76-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="aaf76-122">Redistributable</span></span><br/>       | <span data-ttu-id="aaf76-123">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="aaf76-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aaf76-124">DLL</span><span class="sxs-lookup"><span data-stu-id="aaf76-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="aaf76-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaf76-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaf76-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaf76-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf76-127">**Certificates**</span><span class="sxs-lookup"><span data-stu-id="aaf76-127">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
