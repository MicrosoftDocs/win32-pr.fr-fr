---
description: Récupère le numéro de version principale du modèle.
ms.assetid: efde3a7c-48e0-4bfe-9118-3098c7ef8771
title: Template. MajorVersion, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MajorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a193a36ed7e914d1ed45d26c21008a7e59a5b8a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541651"
---
# <a name="templatemajorversion-property"></a><span data-ttu-id="4f937-103">Template. MajorVersion, propriété</span><span class="sxs-lookup"><span data-stu-id="4f937-103">Template.MajorVersion property</span></span>

<span data-ttu-id="4f937-104">\[La propriété **MajorVersion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="4f937-104">\[The **MajorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4f937-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="4f937-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="4f937-106">La propriété **MajorVersion** récupère le numéro de version principale du modèle.</span><span class="sxs-lookup"><span data-stu-id="4f937-106">The **MajorVersion** property retrieves the major version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f937-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f937-107">Syntax</span></span>


```VB
Template.MajorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="4f937-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4f937-108">Property value</span></span>

<span data-ttu-id="4f937-109">Numéro de version principale du modèle.</span><span class="sxs-lookup"><span data-stu-id="4f937-109">The major version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f937-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f937-110">Requirements</span></span>



| <span data-ttu-id="4f937-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f937-111">Requirement</span></span> | <span data-ttu-id="4f937-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f937-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f937-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4f937-113">Redistributable</span></span><br/> | <span data-ttu-id="4f937-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f937-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4f937-115">DLL</span><span class="sxs-lookup"><span data-stu-id="4f937-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="4f937-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f937-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f937-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f937-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f937-118">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="4f937-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
