---
description: Génère le rendu d’une texture dans un fichier et retourne le résultat à l’hôte asynchrnously.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5 :: RenderTextureAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521524"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span data-ttu-id="c815f-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5 :: RenderTextureAsync, méthode</span><span class="sxs-lookup"><span data-stu-id="c815f-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::RenderTextureAsync method</span></span>

<span data-ttu-id="c815f-104">Génère le rendu d’une texture dans un fichier et retourne le résultat à l’hôte asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="c815f-104">Renders a texture to a file and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="c815f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c815f-105">Syntax</span></span>


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="c815f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c815f-106">Parameters</span></span>

<span data-ttu-id="c815f-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="c815f-107">*textureId* </span></span>  
<span data-ttu-id="c815f-108">ID de la texture à restituer.</span><span class="sxs-lookup"><span data-stu-id="c815f-108">The ID of the texture to render.</span></span>

<span data-ttu-id="c815f-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="c815f-109">*sliceIndex* </span></span>  
<span data-ttu-id="c815f-110">Index de la tranche dans la texture à afficher.</span><span class="sxs-lookup"><span data-stu-id="c815f-110">The index of the slice within the texture to render.</span></span>

<span data-ttu-id="c815f-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="c815f-111">*formatOverride* </span></span>  
<span data-ttu-id="c815f-112">Remplacement du format de couleur.</span><span class="sxs-lookup"><span data-stu-id="c815f-112">The color format override.</span></span>

<span data-ttu-id="c815f-113">*inférieur*</span><span class="sxs-lookup"><span data-stu-id="c815f-113">*lower*</span></span>   

<span data-ttu-id="c815f-114">*coin*</span><span class="sxs-lookup"><span data-stu-id="c815f-114">*upper*</span></span>   

<span data-ttu-id="c815f-115">*shaderFileName* </span><span class="sxs-lookup"><span data-stu-id="c815f-115">*shaderFileName* </span></span>  
<span data-ttu-id="c815f-116">Chaîne COM contenant le nom du chemin d’accès du fichier du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c815f-116">A COM string containing the pathname of the shader file.</span></span>

<span data-ttu-id="c815f-117">*numFloatShaderVars* </span><span class="sxs-lookup"><span data-stu-id="c815f-117">*numFloatShaderVars* </span></span>  
<span data-ttu-id="c815f-118">Nombre de variables de nuanceur à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="c815f-118">The number of floating-point shader variables</span></span>

<span data-ttu-id="c815f-119">*count6 \_ shaderFloatVarName* </span><span class="sxs-lookup"><span data-stu-id="c815f-119">*count6\_shaderFloatVarName* </span></span>  
<span data-ttu-id="c815f-120">Les chaînes COM contianing les noms des variables de nuanceur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="c815f-120">COM strings contianing the names of the floating-point shader variables.</span></span>

<span data-ttu-id="c815f-121">*count6 \_ shaderFloatVarValue* </span><span class="sxs-lookup"><span data-stu-id="c815f-121">*count6\_shaderFloatVarValue* </span></span>  
<span data-ttu-id="c815f-122">Variables de nuanceur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="c815f-122">The floating-point shader variables.</span></span>

<span data-ttu-id="c815f-123">*numBoolShaderVars* </span><span class="sxs-lookup"><span data-stu-id="c815f-123">*numBoolShaderVars* </span></span>  
<span data-ttu-id="c815f-124">Nombre de variables de nuanceur booléennes.</span><span class="sxs-lookup"><span data-stu-id="c815f-124">The number of boolean shader variables.</span></span>

<span data-ttu-id="c815f-125">*count9 \_ shaderBoolVarName* </span><span class="sxs-lookup"><span data-stu-id="c815f-125">*count9\_shaderBoolVarName* </span></span>  
<span data-ttu-id="c815f-126">Les chaînes COM contianing les noms des variables de nuanceur booléen.</span><span class="sxs-lookup"><span data-stu-id="c815f-126">COM strings contianing the names of the boolean shader variables.</span></span>

<span data-ttu-id="c815f-127">*count9 \_ shaderBoolVarValue* </span><span class="sxs-lookup"><span data-stu-id="c815f-127">*count9\_shaderBoolVarValue* </span></span>  
<span data-ttu-id="c815f-128">Variables de nuanceur booléennes.</span><span class="sxs-lookup"><span data-stu-id="c815f-128">The boolean shader variables.</span></span>

<span data-ttu-id="c815f-129">*renderContentFileName* </span><span class="sxs-lookup"><span data-stu-id="c815f-129">*renderContentFileName* </span></span>  
<span data-ttu-id="c815f-130">Chaîne COM contenant le nom du chemin d’accès du fichier dans lequel la texture rendue a été écrite.</span><span class="sxs-lookup"><span data-stu-id="c815f-130">A COM string containing the pathname of the file where the rendered texture was written.</span></span>

<span data-ttu-id="c815f-131">*rappels* </span><span class="sxs-lookup"><span data-stu-id="c815f-131">*callbacks* </span></span>  
<span data-ttu-id="c815f-132">Adresse d’un objet qui fournit l’interface de rappels IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="c815f-132">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="c815f-133">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="c815f-133">*requestCookie* </span></span>  
<span data-ttu-id="c815f-134">Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="c815f-134">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="c815f-135">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="c815f-135">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="c815f-136">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c815f-136">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="c815f-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c815f-137">Return value</span></span>

<span data-ttu-id="c815f-138">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c815f-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c815f-139">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c815f-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c815f-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c815f-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c815f-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="c815f-141">Header</span></span></p></td><td><span data-ttu-id="c815f-142">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c815f-142">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c815f-143"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c815f-143"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c815f-144">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="c815f-144">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
