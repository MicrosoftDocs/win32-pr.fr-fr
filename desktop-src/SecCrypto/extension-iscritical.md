---
description: Récupère une valeur booléenne qui indique si l’extension est marquée comme critique.
ms.assetid: 71f55d63-a51c-472c-81fc-59212c97bb34
title: Propriété extension. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 61e53f869a7063e029cb629b8b2fff4cff025b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526033"
---
# <a name="extensioniscritical-property"></a><span data-ttu-id="339af-103">Propriété extension. IsCritical</span><span class="sxs-lookup"><span data-stu-id="339af-103">Extension.IsCritical property</span></span>

<span data-ttu-id="339af-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="339af-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="339af-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="339af-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="339af-106">La propriété **IsCritical** récupère une valeur booléenne qui indique si l’extension est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="339af-106">The **IsCritical** property retrieves a Boolean value that indicates whether the extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="339af-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="339af-107">Syntax</span></span>


```VB
Extension.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="339af-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="339af-108">Property value</span></span>

<span data-ttu-id="339af-109">Si la **valeur est true**, l’extension est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="339af-109">If **true**, the extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="339af-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="339af-110">Requirements</span></span>



| <span data-ttu-id="339af-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="339af-111">Requirement</span></span> | <span data-ttu-id="339af-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="339af-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="339af-113">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="339af-113">End of client support</span></span><br/> | <span data-ttu-id="339af-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="339af-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="339af-115">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="339af-115">End of server support</span></span><br/> | <span data-ttu-id="339af-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="339af-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="339af-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="339af-117">Redistributable</span></span><br/>       | <span data-ttu-id="339af-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="339af-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="339af-119">DLL</span><span class="sxs-lookup"><span data-stu-id="339af-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="339af-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="339af-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
