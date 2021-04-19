---
description: Récupère le numéro de version mineure du modèle.
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: Template. MinorVersion, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a1de0beb41cbe87ca86b443c5cc2145c2058073
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537588"
---
# <a name="templateminorversion-property"></a><span data-ttu-id="0f0b3-103">Template. MinorVersion, propriété</span><span class="sxs-lookup"><span data-stu-id="0f0b3-103">Template.MinorVersion property</span></span>

<span data-ttu-id="0f0b3-104">\[La propriété **MinorVersion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="0f0b3-104">\[The **MinorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0f0b3-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="0f0b3-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="0f0b3-106">La propriété **MinorVersion** récupère le numéro de version mineure du modèle.</span><span class="sxs-lookup"><span data-stu-id="0f0b3-106">The **MinorVersion** property retrieves the minor version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f0b3-107">Syntax</span></span>


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="0f0b3-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0f0b3-108">Property value</span></span>

<span data-ttu-id="0f0b3-109">Numéro de version mineure du modèle.</span><span class="sxs-lookup"><span data-stu-id="0f0b3-109">The minor version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f0b3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f0b3-110">Requirements</span></span>



| <span data-ttu-id="0f0b3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f0b3-111">Requirement</span></span> | <span data-ttu-id="0f0b3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f0b3-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0b3-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0f0b3-113">Redistributable</span></span><br/> | <span data-ttu-id="0f0b3-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="0f0b3-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0f0b3-115">DLL</span><span class="sxs-lookup"><span data-stu-id="0f0b3-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="0f0b3-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f0b3-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f0b3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f0b3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f0b3-118">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="0f0b3-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
