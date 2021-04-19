---
description: Détermine si le certificat a une clé privée qui lui est associée. La méthode détermine cela en vérifiant si la propriété de l’ID de la clé de certificat \_ \_ Prov \_ info \_ prop \_ est présente.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: 'ICertificate2 :: HasPrivateKey, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523488"
---
# <a name="icertificate2hasprivatekey-method"></a><span data-ttu-id="3d944-104">ICertificate2 :: HasPrivateKey, méthode</span><span class="sxs-lookup"><span data-stu-id="3d944-104">ICertificate2::HasPrivateKey method</span></span>

<span data-ttu-id="3d944-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3d944-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3d944-106">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3d944-106">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3d944-107">La méthode **HasPrivateKey** détermine si le [*certificat*](../secgloss/c-gly.md) a une [*clé privée*](../secgloss/p-gly.md) qui lui est associée.</span><span class="sxs-lookup"><span data-stu-id="3d944-107">The **HasPrivateKey** method determines whether the [*certificate*](../secgloss/c-gly.md) has a [*private key*](../secgloss/p-gly.md) associated with it.</span></span> <span data-ttu-id="3d944-108">La méthode détermine cela en vérifiant si la propriété de l’ID de la clé de certificat \_ \_ Prov \_ info \_ prop \_ est présente.</span><span class="sxs-lookup"><span data-stu-id="3d944-108">The method determines this by checking whether the CERT\_KEY\_PROV\_INFO\_PROP\_ID property is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d944-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d944-109">Syntax</span></span>


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a><span data-ttu-id="3d944-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d944-110">Parameters</span></span>

<span data-ttu-id="3d944-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3d944-111">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d944-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d944-112">Requirements</span></span>



| <span data-ttu-id="3d944-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d944-113">Requirement</span></span> | <span data-ttu-id="3d944-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d944-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d944-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3d944-115">End of client support</span></span><br/> | <span data-ttu-id="3d944-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d944-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3d944-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3d944-117">End of server support</span></span><br/> | <span data-ttu-id="3d944-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d944-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3d944-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3d944-119">Redistributable</span></span><br/>       | <span data-ttu-id="3d944-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="3d944-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3d944-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3d944-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3d944-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d944-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d944-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d944-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d944-124">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="3d944-124">**PrivateKey.Open**</span></span>](privatekey-open.md)
</dt> <dt>

[<span data-ttu-id="3d944-125">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="3d944-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="3d944-126">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="3d944-126">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
