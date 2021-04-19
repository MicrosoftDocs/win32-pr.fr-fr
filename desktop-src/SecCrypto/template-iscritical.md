---
description: Récupère une valeur booléenne qui indique si l’extension de modèle est marquée comme critique.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Propriété Template. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539681"
---
# <a name="templateiscritical-property"></a><span data-ttu-id="98b11-103">Propriété Template. IsCritical</span><span class="sxs-lookup"><span data-stu-id="98b11-103">Template.IsCritical property</span></span>

<span data-ttu-id="98b11-104">\[La propriété **IsCritical** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="98b11-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="98b11-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="98b11-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="98b11-106">La propriété **IsCritical** récupère une valeur booléenne qui indique si l’extension de modèle est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="98b11-106">The **IsCritical** property retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b11-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98b11-107">Syntax</span></span>


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="98b11-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="98b11-108">Property value</span></span>

<span data-ttu-id="98b11-109">Si la **valeur est true**, l’extension de modèle est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="98b11-109">If **true**, the template extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="98b11-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98b11-110">Requirements</span></span>



| <span data-ttu-id="98b11-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98b11-111">Requirement</span></span> | <span data-ttu-id="98b11-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="98b11-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98b11-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="98b11-113">Redistributable</span></span><br/> | <span data-ttu-id="98b11-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="98b11-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="98b11-115">DLL</span><span class="sxs-lookup"><span data-stu-id="98b11-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="98b11-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98b11-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b11-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98b11-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b11-118">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="98b11-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
