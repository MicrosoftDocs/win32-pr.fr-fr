---
description: Récupère un objet OID qui identifie l’objet de modèle.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Template. OID, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543260"
---
# <a name="templateoid-property"></a><span data-ttu-id="45246-103">Template. OID, propriété</span><span class="sxs-lookup"><span data-stu-id="45246-103">Template.OID property</span></span>

<span data-ttu-id="45246-104">\[La propriété **OID** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="45246-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="45246-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="45246-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="45246-106">La propriété **OID** récupère un objet [**OID**](oid.md) qui identifie l’objet de [**modèle**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="45246-106">The **OID** property retrieves an [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

<span data-ttu-id="45246-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="45246-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="45246-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45246-108">Syntax</span></span>


```VB
Template.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="45246-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="45246-109">Property value</span></span>

<span data-ttu-id="45246-110">Objet [**OID**](oid.md) qui identifie l’objet de [**modèle**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="45246-110">An [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="45246-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45246-111">Requirements</span></span>



| <span data-ttu-id="45246-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45246-112">Requirement</span></span> | <span data-ttu-id="45246-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="45246-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45246-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="45246-114">Redistributable</span></span><br/> | <span data-ttu-id="45246-115">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="45246-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="45246-116">DLL</span><span class="sxs-lookup"><span data-stu-id="45246-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="45246-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45246-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45246-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45246-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45246-119">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="45246-119">**Template**</span></span>](template.md)
</dt> </dl>

 

 
