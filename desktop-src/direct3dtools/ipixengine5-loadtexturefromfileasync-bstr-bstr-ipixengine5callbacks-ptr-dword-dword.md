---
description: Charge une texture à partir d’un fichier et avertit l’hôte de façon asynchrone lorsqu’il se termine.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureFromFileAsync\_BSTR\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5 :: LoadTextureFromFileAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DF10C209-B6B5-4692-81D7-7FD59CE49F56
api_name:
- IPixEngine5.LoadTextureFromFileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bef4e4e5117680f7c18f13cc99f801c8e8b8bdfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109754"
---
# <a name="span-idvspixengineipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturefromfileasync-method"></a><span data-ttu-id="caa5c-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5 :: LoadTextureFromFileAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="caa5c-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureFromFileAsync method</span></span>

<span data-ttu-id="caa5c-104">Charge une texture à partir d’un fichier et avertit l’hôte de façon asynchrone lorsqu’il se termine.</span><span class="sxs-lookup"><span data-stu-id="caa5c-104">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="caa5c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caa5c-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileAsync(
   BSTR                  fileName,
   BSTR                  histogramDataFileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="caa5c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caa5c-106">Parameters</span></span>

<span data-ttu-id="caa5c-107">*Extension* </span><span class="sxs-lookup"><span data-stu-id="caa5c-107">*fileName* </span></span>  
<span data-ttu-id="caa5c-108">Chaîne COM contenant le nom du fichier de texture.</span><span class="sxs-lookup"><span data-stu-id="caa5c-108">A COM string containing the name of the texture file.</span></span>

<span data-ttu-id="caa5c-109">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="caa5c-109">*histogramDataFileName* </span></span>  
<span data-ttu-id="caa5c-110">Chaîne COM contenant le nom du fichier de données de l’histogramme associé à la texture.</span><span class="sxs-lookup"><span data-stu-id="caa5c-110">A COM string containing the name of the histogram data file associated with the texture.</span></span>

<span data-ttu-id="caa5c-111">*rappels* </span><span class="sxs-lookup"><span data-stu-id="caa5c-111">*callbacks* </span></span>  
<span data-ttu-id="caa5c-112">Adresse d’un objet qui fournit l’interface de rappels IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="caa5c-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="caa5c-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="caa5c-113">*requestCookie* </span></span>  
<span data-ttu-id="caa5c-114">Cookie qui idenfies la demande de manière unique et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="caa5c-114">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="caa5c-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="caa5c-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="caa5c-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="caa5c-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="caa5c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="caa5c-117">Return value</span></span>

<span data-ttu-id="caa5c-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="caa5c-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="caa5c-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="caa5c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="caa5c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caa5c-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="caa5c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="caa5c-121">Header</span></span></p></td><td><span data-ttu-id="caa5c-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="caa5c-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="caa5c-123"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caa5c-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="caa5c-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="caa5c-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
