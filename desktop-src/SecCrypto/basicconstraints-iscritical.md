---
description: Récupère une valeur booléenne qui indique si l’extension de contrainte de base est marquée comme critique.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: BasicConstraints. IsCritical, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8f3f61a0c458229977abae60258ba4cb71420e72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544038"
---
# <a name="basicconstraintsiscritical-property"></a><span data-ttu-id="43869-103">BasicConstraints. IsCritical, propriété</span><span class="sxs-lookup"><span data-stu-id="43869-103">BasicConstraints.IsCritical property</span></span>

<span data-ttu-id="43869-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="43869-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="43869-105">Utilisez plutôt la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="43869-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="43869-106">La propriété **IsCritical** récupère une valeur booléenne qui indique si l’extension de contrainte de base est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="43869-106">The **IsCritical** property retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span>

<span data-ttu-id="43869-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="43869-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="43869-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43869-108">Syntax</span></span>


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="43869-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="43869-109">Property value</span></span>

<span data-ttu-id="43869-110">Si la **valeur est true**, l’extension de contrainte de base est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="43869-110">If **true**, the basic constraint extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="43869-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43869-111">Requirements</span></span>



| <span data-ttu-id="43869-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43869-112">Requirement</span></span> | <span data-ttu-id="43869-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="43869-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43869-114">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="43869-114">End of client support</span></span><br/> | <span data-ttu-id="43869-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43869-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="43869-116">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="43869-116">End of server support</span></span><br/> | <span data-ttu-id="43869-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43869-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="43869-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="43869-118">Redistributable</span></span><br/>       | <span data-ttu-id="43869-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="43869-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="43869-120">DLL</span><span class="sxs-lookup"><span data-stu-id="43869-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="43869-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43869-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
