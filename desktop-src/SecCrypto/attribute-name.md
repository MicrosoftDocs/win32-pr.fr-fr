---
description: Définit ou récupère le nom CAPICOM de l’attribut. Il s’agit de la propriété par défaut.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Propriété Attribute.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537335"
---
# <a name="attributename-property"></a><span data-ttu-id="e9ba8-104">Propriété Attribute.Name</span><span class="sxs-lookup"><span data-stu-id="e9ba8-104">Attribute.Name property</span></span>

<span data-ttu-id="e9ba8-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="e9ba8-106">Utilisez plutôt la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="e9ba8-106">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="e9ba8-107">La propriété **Name** définit ou récupère le nom CAPICOM de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-107">The **Name** property sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="e9ba8-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-108">This is the default property.</span></span>

<span data-ttu-id="e9ba8-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ba8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9ba8-110">Syntax</span></span>


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a><span data-ttu-id="e9ba8-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e9ba8-111">Property value</span></span>

<span data-ttu-id="e9ba8-112">Valeur de l’énumération d' [**\_ attribut CAPICOM**](capicom-attribute.md) qui spécifie le nom CAPICOM de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-112">A value of the [**CAPICOM\_ATTRIBUTE**](capicom-attribute.md) enumeration that specifies the CAPICOM name of the attribute.</span></span> <span data-ttu-id="e9ba8-113">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="e9ba8-114">Value</span><span class="sxs-lookup"><span data-stu-id="e9ba8-114">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="e9ba8-115">Signification</span><span class="sxs-lookup"><span data-stu-id="e9ba8-115">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <span data-ttu-id="e9ba8-116"><dt>**\_heure de signature de l' \_ attribut \_ authentifié \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ba8-116"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</dt></span></span> </dl>                         | <span data-ttu-id="e9ba8-117">L’attribut contient l’heure à laquelle la signature a été créée.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-117">The attribute contains the time that the signature was created.</span></span><br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <span data-ttu-id="e9ba8-118"><dt>**\_nom du document de l' \_ attribut \_ authentifié \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ba8-118"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</dt></span></span> </dl>                      | <span data-ttu-id="e9ba8-119">L’attribut contient le nom du document signé.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-119">The attribute contains the name of the signed document.</span></span><br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <span data-ttu-id="e9ba8-120"><dt>**\_Description du document de l' \_ attribut \_ authentifié \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ba8-120"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</dt></span></span> </dl> | <span data-ttu-id="e9ba8-121">L’attribut contient une description du document signé.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-121">The attribute contains a description of the signed document.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="e9ba8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e9ba8-122">Remarks</span></span>

<span data-ttu-id="e9ba8-123">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l’état de l’objet est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="e9ba8-123">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ba8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9ba8-124">Requirements</span></span>



| <span data-ttu-id="e9ba8-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9ba8-125">Requirement</span></span> | <span data-ttu-id="e9ba8-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9ba8-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ba8-127">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e9ba8-127">End of client support</span></span><br/> | <span data-ttu-id="e9ba8-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9ba8-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e9ba8-129">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e9ba8-129">End of server support</span></span><br/> | <span data-ttu-id="e9ba8-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9ba8-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e9ba8-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e9ba8-131">Redistributable</span></span><br/>       | <span data-ttu-id="e9ba8-132">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="e9ba8-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e9ba8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e9ba8-133">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e9ba8-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9ba8-134"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ba8-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9ba8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ba8-136">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e9ba8-136">**Attribute**</span></span>](attribute.md)
</dt> </dl>

 

 
