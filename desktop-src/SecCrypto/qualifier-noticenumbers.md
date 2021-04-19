---
description: Récupère la collection de numéros d’avis de l’utilisateur.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Qualifier. NoticeNumbers, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542403"
---
# <a name="qualifiernoticenumbers-property"></a><span data-ttu-id="9249f-103">Qualifier. NoticeNumbers, propriété</span><span class="sxs-lookup"><span data-stu-id="9249f-103">Qualifier.NoticeNumbers property</span></span>

<span data-ttu-id="9249f-104">\[La propriété **NoticeNumbers** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="9249f-104">\[The **NoticeNumbers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9249f-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="9249f-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="9249f-106">La propriété **NoticeNumbers** récupère la collection de numéros d’avis de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9249f-106">The **NoticeNumbers** property retrieves the collection of user notice numbers.</span></span> <span data-ttu-id="9249f-107">Cette propriété peut être vide.</span><span class="sxs-lookup"><span data-stu-id="9249f-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="9249f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9249f-108">Syntax</span></span>


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a><span data-ttu-id="9249f-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9249f-109">Property value</span></span>

<span data-ttu-id="9249f-110">Collection de numéros d’avis de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9249f-110">The collection of user notice numbers.</span></span>

## <a name="requirements"></a><span data-ttu-id="9249f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9249f-111">Requirements</span></span>



| <span data-ttu-id="9249f-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9249f-112">Requirement</span></span> | <span data-ttu-id="9249f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9249f-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9249f-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9249f-114">Redistributable</span></span><br/> | <span data-ttu-id="9249f-115">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="9249f-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9249f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="9249f-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="9249f-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9249f-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9249f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9249f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9249f-119">**Qualificateur**</span><span class="sxs-lookup"><span data-stu-id="9249f-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
