---
title: Point d’entrée VirtualChannelGetInstance
description: Appelé pour que le plug-in crée une instance de l’interface IWTSPlugin pour tous les plug-ins implémentés par la DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Point d’entrée VirtualChannelGetInstance Services Bureau à distance
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384271"
---
# <a name="virtualchannelgetinstance-entry-point"></a><span data-ttu-id="b0e22-104">Point d’entrée VirtualChannelGetInstance</span><span class="sxs-lookup"><span data-stu-id="b0e22-104">VirtualChannelGetInstance entry point</span></span>

<span data-ttu-id="b0e22-105">Appelé pour que le plug-in crée une instance de l’interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) pour tous les plug-ins implémentés par la dll.</span><span class="sxs-lookup"><span data-stu-id="b0e22-105">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

> [!Note]
>
> <span data-ttu-id="b0e22-106">Cette fonction est implémentée par le plug-in et doit être exportée par nom afin qu’une application puisse utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à la fonction.</span><span class="sxs-lookup"><span data-stu-id="b0e22-106">This function is implemented by the plug-in and must be exported by name such that an application can use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to the function.</span></span>
>
> <span data-ttu-id="b0e22-107">Le prototype de cette fonction n’est contenu dans aucun fichier d’en-tête public. vous devez donc le déclarer exactement comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="b0e22-107">The prototype for this function is not contained in any public header file, so you must declare it exactly as shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b0e22-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0e22-108">Syntax</span></span>


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a><span data-ttu-id="b0e22-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0e22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e22-110">*REFIID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0e22-110">*refiid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e22-111">Spécifie le type d’interface à retourner.</span><span class="sxs-lookup"><span data-stu-id="b0e22-111">Specifies the type of interface to return.</span></span> <span data-ttu-id="b0e22-112">Il doit s’agir de l' **IID \_ IWTSPlugin**.</span><span class="sxs-lookup"><span data-stu-id="b0e22-112">This must be **IID\_IWTSPlugin**.</span></span>

</dd> <dt>

<span data-ttu-id="b0e22-113">*pNumObjs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b0e22-113">*pNumObjs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e22-114">Adresse d’une variable **ULong** qui reçoit le nombre d’interfaces récupérées.</span><span class="sxs-lookup"><span data-stu-id="b0e22-114">The address of a **ULONG** variable that receives the number of interfaces retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="b0e22-115">*ppObjArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0e22-115">*ppObjArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e22-116">Adresse d’un tableau de pointeurs qui reçoit les pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="b0e22-116">The address of an array of pointers that receives the interface pointers.</span></span> <span data-ttu-id="b0e22-117">Si ce paramètre a la **valeur null**, l’implémentation doit placer le nombre de plug-ins implémentés par la dll dans le paramètre *pNumObjs* .</span><span class="sxs-lookup"><span data-stu-id="b0e22-117">If this parameter is **NULL**, the implementation must put the number of plug-ins implemented by the DLL in the *pNumObjs* parameter.</span></span> <span data-ttu-id="b0e22-118">Cela permet à l’appelant d’allouer le tableau de taille approprié pour *ppObjArray*.</span><span class="sxs-lookup"><span data-stu-id="b0e22-118">This allows the caller to allocate the proper size array for *ppObjArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e22-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0e22-119">Return value</span></span>

<span data-ttu-id="b0e22-120">Si ce point d’entrée est correctement exécuté, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b0e22-120">If this entry point succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0e22-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0e22-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e22-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0e22-122">Requirements</span></span>



| <span data-ttu-id="b0e22-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0e22-123">Requirement</span></span> | <span data-ttu-id="b0e22-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0e22-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b0e22-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e22-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e22-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0e22-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b0e22-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e22-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e22-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0e22-128">Windows Server 2008</span></span><br/> |



 

