---
description: Récupère la collection d’attributs authentifiés.
ms.assetid: d4b3efab-d71e-4fef-9691-0c0bbcb27281
title: Propriété signer. AuthenticatedAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.AuthenticatedAttributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3963ec60d699300c4cde368d4d78c39c0873edd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537378"
---
# <a name="signerauthenticatedattributes-property"></a><span data-ttu-id="8c0be-103">Propriété signer. AuthenticatedAttributes</span><span class="sxs-lookup"><span data-stu-id="8c0be-103">Signer.AuthenticatedAttributes property</span></span>

<span data-ttu-id="8c0be-104">\[La propriété **AuthenticatedAttributes** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="8c0be-104">\[The **AuthenticatedAttributes** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8c0be-105">Utilisez plutôt la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="8c0be-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="8c0be-106">La propriété **AuthenticatedAttributes** récupère la collection d’attributs authentifiés.</span><span class="sxs-lookup"><span data-stu-id="8c0be-106">The **AuthenticatedAttributes** property retrieves the collection of authenticated attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c0be-107">Syntax</span></span>


```VB
Signer.AuthenticatedAttributes As Attributes
```



## <a name="property-value"></a><span data-ttu-id="8c0be-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8c0be-108">Property value</span></span>

<span data-ttu-id="8c0be-109">Collection d' [**attributs**](attributes.md) qui représente les attributs authentifiés du signataire.</span><span class="sxs-lookup"><span data-stu-id="8c0be-109">An [**Attributes**](attributes.md) collection that represents the signer's authenticated attributes.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0be-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c0be-110">Requirements</span></span>



| <span data-ttu-id="8c0be-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c0be-111">Requirement</span></span> | <span data-ttu-id="8c0be-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c0be-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0be-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8c0be-113">Redistributable</span></span><br/> | <span data-ttu-id="8c0be-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c0be-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8c0be-115">DLL</span><span class="sxs-lookup"><span data-stu-id="8c0be-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="8c0be-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c0be-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c0be-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c0be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0be-118">**Signataire**</span><span class="sxs-lookup"><span data-stu-id="8c0be-118">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
