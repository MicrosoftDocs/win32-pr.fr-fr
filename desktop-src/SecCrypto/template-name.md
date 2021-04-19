---
description: Récupère le nom du modèle.
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Propriété Template.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 005a9cc961b1d7be0ebda0b8e76307b95d92a6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541650"
---
# <a name="templatename-property"></a><span data-ttu-id="dca02-103">Propriété Template.Name</span><span class="sxs-lookup"><span data-stu-id="dca02-103">Template.Name property</span></span>

<span data-ttu-id="dca02-104">\[La propriété **nom** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="dca02-104">\[The **Name** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dca02-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="dca02-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="dca02-106">La propriété **Name** récupère le nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="dca02-106">The **Name** property retrieves the name of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="dca02-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dca02-107">Syntax</span></span>


```VB
Template.Name As String
```



## <a name="property-value"></a><span data-ttu-id="dca02-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="dca02-108">Property value</span></span>

<span data-ttu-id="dca02-109">Nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="dca02-109">The name of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="dca02-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dca02-110">Requirements</span></span>



| <span data-ttu-id="dca02-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dca02-111">Requirement</span></span> | <span data-ttu-id="dca02-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="dca02-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dca02-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="dca02-113">Redistributable</span></span><br/> | <span data-ttu-id="dca02-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="dca02-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dca02-115">DLL</span><span class="sxs-lookup"><span data-stu-id="dca02-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="dca02-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dca02-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dca02-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dca02-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca02-118">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="dca02-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
