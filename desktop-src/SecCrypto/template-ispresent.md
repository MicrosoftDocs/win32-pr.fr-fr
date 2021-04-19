---
description: Récupère une valeur booléenne qui indique si l’extension de modèle est présente.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Propriété Template. IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23dcd8cc5ee92a689300078d439998e43933af93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520790"
---
# <a name="templateispresent-property"></a><span data-ttu-id="aeecc-103">Propriété Template. IsPresent</span><span class="sxs-lookup"><span data-stu-id="aeecc-103">Template.IsPresent property</span></span>

<span data-ttu-id="aeecc-104">\[La propriété **IsPresent** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="aeecc-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="aeecc-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="aeecc-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="aeecc-106">La propriété **IsPresent** récupère une valeur booléenne qui indique si l’extension de modèle est présente.</span><span class="sxs-lookup"><span data-stu-id="aeecc-106">The **IsPresent** property retrieves a Boolean value that indicates whether the template extension is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeecc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aeecc-107">Syntax</span></span>


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="aeecc-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="aeecc-108">Property value</span></span>

<span data-ttu-id="aeecc-109">Si la **valeur est true**, l’extension de modèle est présente.</span><span class="sxs-lookup"><span data-stu-id="aeecc-109">If **true**, the template extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeecc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aeecc-110">Requirements</span></span>



| <span data-ttu-id="aeecc-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aeecc-111">Requirement</span></span> | <span data-ttu-id="aeecc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="aeecc-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeecc-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="aeecc-113">Redistributable</span></span><br/> | <span data-ttu-id="aeecc-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="aeecc-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aeecc-115">DLL</span><span class="sxs-lookup"><span data-stu-id="aeecc-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="aeecc-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeecc-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeecc-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aeecc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeecc-118">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="aeecc-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
