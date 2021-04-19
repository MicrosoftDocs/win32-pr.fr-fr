---
description: Ferme un handle HCERTSTORE acquis par le biais de la propriété StoreHandle.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'ICertStore :: CloseHandle, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540722"
---
# <a name="icertstoreclosehandle-method"></a><span data-ttu-id="95bda-103">ICertStore :: CloseHandle, méthode</span><span class="sxs-lookup"><span data-stu-id="95bda-103">ICertStore::CloseHandle method</span></span>

<span data-ttu-id="95bda-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="95bda-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="95bda-105">La méthode **CloseHandle** ferme un handle HCERTSTORE acquis par le biais de la propriété [**StoreHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="95bda-105">The **CloseHandle** method closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="95bda-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95bda-106">Syntax</span></span>


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a><span data-ttu-id="95bda-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95bda-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95bda-108">*hCertStore* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95bda-108">*hCertStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95bda-109">Handle HCERTSTORE à fermer.</span><span class="sxs-lookup"><span data-stu-id="95bda-109">The HCERTSTORE handle to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95bda-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95bda-110">Return value</span></span>

<span data-ttu-id="95bda-111">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="95bda-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="95bda-112">La valeur **S \_ OK** indique la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="95bda-112">A value of **S\_OK** indicates success.</span></span> <span data-ttu-id="95bda-113">Toute autre valeur indique que l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="95bda-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="95bda-114">Notes</span><span class="sxs-lookup"><span data-stu-id="95bda-114">Remarks</span></span>

<span data-ttu-id="95bda-115">Cette méthode ne libère pas le handle HCERTSTORE contenu dans un objet de [**magasin**](store.md) .</span><span class="sxs-lookup"><span data-stu-id="95bda-115">This method does not release the HCERTSTORE handle contained within a [**Store**](store.md) object.</span></span> <span data-ttu-id="95bda-116">Elle doit être utilisée uniquement pour libérer un handle HCERTSTORE acquis par le biais de la propriété [**StoreHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="95bda-116">It should be used only to release a HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="95bda-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95bda-117">Requirements</span></span>



| <span data-ttu-id="95bda-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95bda-118">Requirement</span></span> | <span data-ttu-id="95bda-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="95bda-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95bda-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="95bda-120">Redistributable</span></span><br/> | <span data-ttu-id="95bda-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="95bda-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="95bda-122">DLL</span><span class="sxs-lookup"><span data-stu-id="95bda-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="95bda-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95bda-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95bda-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95bda-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95bda-125">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="95bda-125">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




