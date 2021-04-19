---
description: Récupère une valeur booléenne qui indique si le certificat est destiné à une autorité de certification (CA).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: BasicConstraints. IsCertificateAuthority, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d4878a8cb21f89f3abeeb9e4b530948ef12e9aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531046"
---
# <a name="basicconstraintsiscertificateauthority-property"></a><span data-ttu-id="ab0c9-103">BasicConstraints. IsCertificateAuthority, propriété</span><span class="sxs-lookup"><span data-stu-id="ab0c9-103">BasicConstraints.IsCertificateAuthority property</span></span>

<span data-ttu-id="ab0c9-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab0c9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="ab0c9-105">Utilisez plutôt la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="ab0c9-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="ab0c9-106">La propriété **IsCertificateAuthority** récupère une valeur booléenne qui indique si le certificat est destiné à une [*autorité de certification*](../secgloss/c-gly.md) (ca).</span><span class="sxs-lookup"><span data-stu-id="ab0c9-106">The **IsCertificateAuthority** property retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="ab0c9-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ab0c9-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0c9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab0c9-108">Syntax</span></span>


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ab0c9-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ab0c9-109">Property value</span></span>

<span data-ttu-id="ab0c9-110">Si la **valeur est true**, le certificat doit être utilisé uniquement par une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="ab0c9-110">If **True**, the certificate is to be used only by a CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab0c9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab0c9-111">Requirements</span></span>



| <span data-ttu-id="ab0c9-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab0c9-112">Requirement</span></span> | <span data-ttu-id="ab0c9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab0c9-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0c9-114">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ab0c9-114">End of client support</span></span><br/> | <span data-ttu-id="ab0c9-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab0c9-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ab0c9-116">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ab0c9-116">End of server support</span></span><br/> | <span data-ttu-id="ab0c9-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab0c9-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ab0c9-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ab0c9-118">Redistributable</span></span><br/>       | <span data-ttu-id="ab0c9-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="ab0c9-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ab0c9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ab0c9-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ab0c9-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab0c9-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
