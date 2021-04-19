---
description: Ferme un magasin de certificats ouvert.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Store. Close, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537838"
---
# <a name="storeclose-method"></a><span data-ttu-id="17498-103">Store. Close, méthode</span><span class="sxs-lookup"><span data-stu-id="17498-103">Store.Close method</span></span>

<span data-ttu-id="17498-104">\[La méthode **Close** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="17498-104">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="17498-105">Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="17498-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="17498-106">La méthode **Close** ferme un [*magasin de certificats*](../secgloss/c-gly.md)ouvert.</span><span class="sxs-lookup"><span data-stu-id="17498-106">The **Close** method closes an open [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="17498-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17498-107">Syntax</span></span>


```VB
Store.Close()
```



## <a name="parameters"></a><span data-ttu-id="17498-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17498-108">Parameters</span></span>

<span data-ttu-id="17498-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="17498-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17498-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17498-110">Return value</span></span>

<span data-ttu-id="17498-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="17498-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17498-112">Notes</span><span class="sxs-lookup"><span data-stu-id="17498-112">Remarks</span></span>

<span data-ttu-id="17498-113">Une fois la méthode **Close** appelée, l’objet [**Store**](store.md) est détruit.</span><span class="sxs-lookup"><span data-stu-id="17498-113">After the **Close** method is called, the [**Store**](store.md) object is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="17498-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17498-114">Requirements</span></span>



| <span data-ttu-id="17498-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17498-115">Requirement</span></span> | <span data-ttu-id="17498-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="17498-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17498-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="17498-117">Redistributable</span></span><br/> | <span data-ttu-id="17498-118">CAPICOM 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="17498-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="17498-119">DLL</span><span class="sxs-lookup"><span data-stu-id="17498-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="17498-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17498-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17498-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17498-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17498-122">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="17498-122">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="17498-123">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="17498-123">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="17498-124">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="17498-124">**Open**</span></span>](store-open.md)
</dt> </dl>

 

 
