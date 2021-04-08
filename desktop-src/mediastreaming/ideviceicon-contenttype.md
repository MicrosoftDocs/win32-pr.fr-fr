---
title: IDeviceIcon, méthode ContentType
description: Récupère le type de contenu de l’icône.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- API de diffusion multimédia en continu de la méthode ContentType
- Méthode ContentType API de diffusion multimédia en continu, interface IDeviceIcon
- API de diffusion multimédia en continu de l’interface IDeviceIcon, méthode ContentType
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842138"
---
# <a name="ideviceiconcontenttype-method"></a><span data-ttu-id="964fa-106">IDeviceIcon :: ContentType, méthode</span><span class="sxs-lookup"><span data-stu-id="964fa-106">IDeviceIcon::ContentType method</span></span>

<span data-ttu-id="964fa-107">Récupère le type de contenu de l’icône.</span><span class="sxs-lookup"><span data-stu-id="964fa-107">Retrieves the content type of the icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="964fa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="964fa-108">Syntax</span></span>


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="964fa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="964fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="964fa-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="964fa-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="964fa-111">Reçoit un pointeur vers le type de contenu de l’icône.</span><span class="sxs-lookup"><span data-stu-id="964fa-111">Receives a pointer to the content type of the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="964fa-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="964fa-112">Return value</span></span>

<span data-ttu-id="964fa-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="964fa-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="964fa-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="964fa-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="964fa-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="964fa-115">Return code</span></span>                                                                          | <span data-ttu-id="964fa-116">Description</span><span class="sxs-lookup"><span data-stu-id="964fa-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="964fa-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="964fa-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="964fa-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="964fa-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="964fa-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="964fa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="964fa-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="964fa-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

