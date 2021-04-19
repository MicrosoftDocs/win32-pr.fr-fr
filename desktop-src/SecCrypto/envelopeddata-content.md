---
description: Définit ou récupère le contenu en texte en clair d’un message à envelopper. Il s’agit de la propriété par défaut.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: EnvelopedData. Content, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520920"
---
# <a name="envelopeddatacontent-property"></a><span data-ttu-id="727e2-104">EnvelopedData. Content, propriété</span><span class="sxs-lookup"><span data-stu-id="727e2-104">EnvelopedData.Content property</span></span>

<span data-ttu-id="727e2-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="727e2-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="727e2-106">Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="727e2-106">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="727e2-107">La propriété de **contenu** définit ou récupère le contenu en texte en clair d’un message à envelopper.</span><span class="sxs-lookup"><span data-stu-id="727e2-107">The **Content** property sets or retrieves the plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="727e2-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="727e2-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="727e2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="727e2-109">Syntax</span></span>


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="727e2-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="727e2-110">Property value</span></span>

<span data-ttu-id="727e2-111">Contenu en texte clair d’un message à envelopper.</span><span class="sxs-lookup"><span data-stu-id="727e2-111">The plaintext content of a message to be enveloped.</span></span>

## <a name="remarks"></a><span data-ttu-id="727e2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="727e2-112">Remarks</span></span>

<span data-ttu-id="727e2-113">La définition de cette propriété doit être effectuée avant l’appel de la méthode [**Encrypt**](envelopeddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="727e2-113">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span> <span data-ttu-id="727e2-114">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée et tout contenu chiffré dans l’objet est perdu.</span><span class="sxs-lookup"><span data-stu-id="727e2-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="727e2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="727e2-115">Requirements</span></span>



| <span data-ttu-id="727e2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="727e2-116">Requirement</span></span> | <span data-ttu-id="727e2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="727e2-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="727e2-118">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="727e2-118">End of client support</span></span><br/> | <span data-ttu-id="727e2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="727e2-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="727e2-120">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="727e2-120">End of server support</span></span><br/> | <span data-ttu-id="727e2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="727e2-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="727e2-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="727e2-122">Redistributable</span></span><br/>       | <span data-ttu-id="727e2-123">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="727e2-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="727e2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="727e2-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="727e2-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="727e2-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="727e2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="727e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727e2-127">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="727e2-127">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
