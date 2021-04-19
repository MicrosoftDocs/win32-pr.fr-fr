---
description: Fournit l’accès au contexte d’un objet de certificat CAPICOM X. 509v3. Ce contexte permet d’utiliser le certificat CAPICOM dans d’autres dérivations de CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Interface ICertContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525634"
---
# <a name="icertcontext-interface"></a><span data-ttu-id="49304-104">Interface ICertContext</span><span class="sxs-lookup"><span data-stu-id="49304-104">ICertContext interface</span></span>

<span data-ttu-id="49304-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="49304-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="49304-106">L’interface **ICertContext** fournit l’accès au contexte d’un objet de [**certificat**](certificate.md) CAPICOM X. 509v3.</span><span class="sxs-lookup"><span data-stu-id="49304-106">The **ICertContext** interface provides access to the context of a CAPICOM X.509v3 [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="49304-107">Ce contexte permet d’utiliser le certificat CAPICOM dans d’autres dérivations de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="49304-107">This context allows the CAPICOM certificate to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="49304-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="49304-108">When to use</span></span>

<span data-ttu-id="49304-109">Utilisez cette interface lorsque vous devez utiliser un objet de [**certificat**](certificate.md) CAPICOM dans une autre dérivation de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="49304-109">Use this interface when you need to use a CAPICOM [**Certificate**](certificate.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="49304-110">Membres</span><span class="sxs-lookup"><span data-stu-id="49304-110">Members</span></span>

<span data-ttu-id="49304-111">L’interface **ICertContext** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="49304-111">The **ICertContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="49304-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="49304-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="49304-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49304-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="49304-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="49304-114">Methods</span></span>

<span data-ttu-id="49304-115">L’interface **ICertContext** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="49304-115">The **ICertContext** interface has these methods.</span></span>



| <span data-ttu-id="49304-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="49304-116">Method</span></span>                                          | <span data-ttu-id="49304-117">Description</span><span class="sxs-lookup"><span data-stu-id="49304-117">Description</span></span>                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49304-118">**FreeContext**</span><span class="sxs-lookup"><span data-stu-id="49304-118">**FreeContext**</span></span>](icertcontext-freecontext.md) | <span data-ttu-id="49304-119">Libère un \_ contexte PCCERT acquis par le biais de la propriété [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="49304-119">Releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="49304-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49304-120">Properties</span></span>

<span data-ttu-id="49304-121">L’interface **ICertContext** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="49304-121">The **ICertContext** interface has these properties.</span></span>



| <span data-ttu-id="49304-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="49304-122">Property</span></span>                                                   | <span data-ttu-id="49304-123">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="49304-123">Access type</span></span>           | <span data-ttu-id="49304-124">Description</span><span class="sxs-lookup"><span data-stu-id="49304-124">Description</span></span>                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="49304-125">**CertContext**</span><span class="sxs-lookup"><span data-stu-id="49304-125">**CertContext**</span></span>](icertcontext-certcontext.md)<br/> | <span data-ttu-id="49304-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="49304-126">Read/write</span></span><br/> | <span data-ttu-id="49304-127">Définit ou récupère le contexte PCCERT \_ d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="49304-127">Sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="49304-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49304-128">Requirements</span></span>



| <span data-ttu-id="49304-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49304-129">Requirement</span></span> | <span data-ttu-id="49304-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="49304-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49304-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="49304-131">Redistributable</span></span><br/> | <span data-ttu-id="49304-132">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="49304-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="49304-133">DLL</span><span class="sxs-lookup"><span data-stu-id="49304-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="49304-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49304-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




