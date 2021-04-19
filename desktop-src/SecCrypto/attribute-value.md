---
description: Définit ou récupère la valeur de l’attribut.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Propriété Attribute. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539985"
---
# <a name="attributevalue-property"></a><span data-ttu-id="ce8fb-103">Propriété Attribute. Value</span><span class="sxs-lookup"><span data-stu-id="ce8fb-103">Attribute.Value property</span></span>

<span data-ttu-id="ce8fb-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ce8fb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="ce8fb-105">Utilisez plutôt la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="ce8fb-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="ce8fb-106">La propriété **value** définit ou récupère la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="ce8fb-106">The **Value** property sets or retrieves the value of the attribute.</span></span>

<span data-ttu-id="ce8fb-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ce8fb-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce8fb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce8fb-108">Syntax</span></span>


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="ce8fb-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ce8fb-109">Property value</span></span>

<span data-ttu-id="ce8fb-110">Variable de **type Variant** qui contient la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="ce8fb-110">A **Variant** variable that contains the value of the attribute.</span></span> <span data-ttu-id="ce8fb-111">Pour les attributs de temps de signature des attributs **\_ authentifiés \_ \_ \_ CAPICOM** , le type de données est date.</span><span class="sxs-lookup"><span data-stu-id="ce8fb-111">For **CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME** attributes, the data type is **DATE**.</span></span> <span data-ttu-id="ce8fb-112">Pour tous les autres attributs, la valeur de la propriété est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="ce8fb-112">For all other attributes, the property value is a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce8fb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce8fb-113">Requirements</span></span>



| <span data-ttu-id="ce8fb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce8fb-114">Requirement</span></span> | <span data-ttu-id="ce8fb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce8fb-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce8fb-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ce8fb-116">End of client support</span></span><br/> | <span data-ttu-id="ce8fb-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce8fb-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ce8fb-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ce8fb-118">End of server support</span></span><br/> | <span data-ttu-id="ce8fb-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce8fb-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ce8fb-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ce8fb-120">Redistributable</span></span><br/>       | <span data-ttu-id="ce8fb-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="ce8fb-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ce8fb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ce8fb-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ce8fb-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce8fb-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
