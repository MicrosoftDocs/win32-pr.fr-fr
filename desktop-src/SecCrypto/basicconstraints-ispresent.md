---
description: Récupère une valeur booléenne qui indique si l’extension de contraintes de base est présente. Il s’agit de la propriété par défaut.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: BasicConstraints. IsPresent, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9632f0d1297f2effd7d1bcc6056b2327d7f38e26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543798"
---
# <a name="basicconstraintsispresent-property"></a><span data-ttu-id="325aa-104">BasicConstraints. IsPresent, propriété</span><span class="sxs-lookup"><span data-stu-id="325aa-104">BasicConstraints.IsPresent property</span></span>

<span data-ttu-id="325aa-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="325aa-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="325aa-106">Utilisez plutôt la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="325aa-106">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="325aa-107">La propriété **IsPresent** récupère une valeur booléenne qui indique si l’extension de contraintes de base est présente.</span><span class="sxs-lookup"><span data-stu-id="325aa-107">The **IsPresent** property retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="325aa-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="325aa-108">This is the default property.</span></span>

<span data-ttu-id="325aa-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="325aa-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="325aa-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="325aa-110">Syntax</span></span>


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="325aa-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="325aa-111">Property value</span></span>

<span data-ttu-id="325aa-112">Si la **valeur est true**, l’extension de contraintes de base est présente.</span><span class="sxs-lookup"><span data-stu-id="325aa-112">If **true**, the basic constraints extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="325aa-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="325aa-113">Requirements</span></span>



| <span data-ttu-id="325aa-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="325aa-114">Requirement</span></span> | <span data-ttu-id="325aa-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="325aa-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="325aa-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="325aa-116">End of client support</span></span><br/> | <span data-ttu-id="325aa-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="325aa-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="325aa-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="325aa-118">End of server support</span></span><br/> | <span data-ttu-id="325aa-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="325aa-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="325aa-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="325aa-120">Redistributable</span></span><br/>       | <span data-ttu-id="325aa-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="325aa-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="325aa-122">DLL</span><span class="sxs-lookup"><span data-stu-id="325aa-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="325aa-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="325aa-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="325aa-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="325aa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325aa-125">**BasicConstraints**</span><span class="sxs-lookup"><span data-stu-id="325aa-125">**BasicConstraints**</span></span>](basicconstraints.md)
</dt> </dl>

 

 
