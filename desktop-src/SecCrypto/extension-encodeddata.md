---
description: Récupère les données encodées pour l’extension.
ms.assetid: 79811557-6d7e-4d19-bcbb-1f79455dd286
title: Propriété extension. EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2153c97d523693a0a1ea13f92135a17591ce68d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528060"
---
# <a name="extensionencodeddata-property"></a><span data-ttu-id="5b70f-103">Propriété extension. EncodedData</span><span class="sxs-lookup"><span data-stu-id="5b70f-103">Extension.EncodedData property</span></span>

<span data-ttu-id="5b70f-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5b70f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5b70f-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="5b70f-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5b70f-106">La propriété **EncodedData** récupère les données encodées pour l’extension.</span><span class="sxs-lookup"><span data-stu-id="5b70f-106">The **EncodedData** property retrieves the encoded data for the extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b70f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b70f-107">Syntax</span></span>


```VB
Extension.EncodedData As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="5b70f-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5b70f-108">Property value</span></span>

<span data-ttu-id="5b70f-109">Objet [**EncodedData**](encodeddata.md) qui représente les données de l’extension de certificat.</span><span class="sxs-lookup"><span data-stu-id="5b70f-109">An [**EncodedData**](encodeddata.md) object that represents the data of the certificate extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b70f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b70f-110">Requirements</span></span>



| <span data-ttu-id="5b70f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b70f-111">Requirement</span></span> | <span data-ttu-id="5b70f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b70f-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b70f-113">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5b70f-113">End of client support</span></span><br/> | <span data-ttu-id="5b70f-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b70f-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5b70f-115">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="5b70f-115">End of server support</span></span><br/> | <span data-ttu-id="5b70f-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b70f-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5b70f-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5b70f-117">Redistributable</span></span><br/>       | <span data-ttu-id="5b70f-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="5b70f-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5b70f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5b70f-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5b70f-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b70f-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
