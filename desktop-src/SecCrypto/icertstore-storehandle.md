---
description: Définit ou récupère le handle HCERTSTORE d’un magasin de certificats.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'ICertStore :: StoreHandle, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524037"
---
# <a name="icertstorestorehandle-property"></a><span data-ttu-id="792c2-103">ICertStore :: StoreHandle, propriété</span><span class="sxs-lookup"><span data-stu-id="792c2-103">ICertStore::StoreHandle property</span></span>

<span data-ttu-id="792c2-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="792c2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="792c2-105">La propriété **StoreHandle** définit ou récupère le handle HCERTSTORE d’un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="792c2-105">The **StoreHandle** property sets or retrieves the HCERTSTORE handle of a certificate store.</span></span>

<span data-ttu-id="792c2-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="792c2-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="792c2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="792c2-107">Syntax</span></span>


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a><span data-ttu-id="792c2-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="792c2-108">Property value</span></span>

<span data-ttu-id="792c2-109">Handle HCERTSTORE du magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="792c2-109">The HCERTSTORE handle of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="792c2-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="792c2-110">Error codes</span></span>

<span data-ttu-id="792c2-111">Si les méthodes d’accès aux propriétés **placent \_ StoreHandle** et **obtiennent \_ StoreHandle** , elles retournent la réponse \_ OK.</span><span class="sxs-lookup"><span data-stu-id="792c2-111">If the property access methods **put\_StoreHandle** and **get\_StoreHandle** succeed, they return S\_OK.</span></span>

<span data-ttu-id="792c2-112">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="792c2-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="792c2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="792c2-113">Remarks</span></span>

<span data-ttu-id="792c2-114">Vous devez appeler la méthode [**CloseHandle**](icertstore-closehandle.md) ou la fonction [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) pour libérer le contexte.</span><span class="sxs-lookup"><span data-stu-id="792c2-114">You must call either the [**CloseHandle**](icertstore-closehandle.md) method or the [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) function to free the context.</span></span>

<span data-ttu-id="792c2-115">Si vous définissez la propriété **StoreHandle** , l’état de la totalité de l’objet de [**magasin**](store.md) est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="792c2-115">If you set the **StoreHandle** property, the state of the entire [**Store**](store.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="792c2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="792c2-116">Requirements</span></span>



| <span data-ttu-id="792c2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="792c2-117">Requirement</span></span> | <span data-ttu-id="792c2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="792c2-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="792c2-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="792c2-119">Redistributable</span></span><br/> | <span data-ttu-id="792c2-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="792c2-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="792c2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="792c2-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="792c2-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="792c2-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="792c2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="792c2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792c2-124">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="792c2-124">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




