---
description: Récupère le nom de la classe et d’autres informations associées à un GUID donné dans le manifeste d’un composant.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: SxsLookupClrGuid fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525406"
---
# <a name="sxslookupclrguid-function"></a><span data-ttu-id="fb25e-103">SxsLookupClrGuid fonction)</span><span class="sxs-lookup"><span data-stu-id="fb25e-103">SxsLookupClrGuid function</span></span>

<span data-ttu-id="fb25e-104">Récupère le nom de la classe et d’autres informations associées à un GUID donné dans le manifeste d’un composant.</span><span class="sxs-lookup"><span data-stu-id="fb25e-104">Retrieves the class name and other information associated with a given GUID in a component's manifest.</span></span> <span data-ttu-id="fb25e-105">Cette fonction est utilisée uniquement lors de l’implémentation de l’interopérabilité managée et non managée de bas niveau dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fb25e-105">This function is used only when implementing low-level managed-unmanaged interoperability in the .NET Framework.</span></span> <span data-ttu-id="fb25e-106">Pour plus d’informations sur l’interopérabilité managée non managée, consultez « interopérabilité avec du code non managé » dans le kit de développement logiciel (SDK) .NET Framework et également [applications isolées et assemblys côte à côte](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fb25e-106">For more information about managed-unmanaged interoperability, see "Interoperating with Unmanaged Code" in the .NET Framework SDK and also [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb25e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb25e-107">Syntax</span></span>


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="fb25e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb25e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb25e-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb25e-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb25e-110">Combinaison de zéro ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="fb25e-110">A combination of zero or more of the following flags.</span></span>



| <span data-ttu-id="fb25e-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb25e-111">Value</span></span>                                                                                                                                                                                                                                                                                             | <span data-ttu-id="fb25e-112">Signification</span><span class="sxs-lookup"><span data-stu-id="fb25e-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <span data-ttu-id="fb25e-113"><dt>**SxS \_ Rechercher \_ \_ GUID CLR \_ utiliser \_ ACTCTX**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="fb25e-113"><dt>**SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX**</dt> <dt>0x00000001</dt></span></span> </dl>              | <span data-ttu-id="fb25e-114">Si cet indicateur est défini, le paramètre *hActCtx* doit contenir un handle de contexte d’activation retourné par la fonction [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="fb25e-114">If this flag is set, then the *hActCtx* parameter must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="fb25e-115">Si cet indicateur n’est pas défini, le paramètre *hActCtx* est ignoré et **SxsLookupClrGuid** recherche le contexte d’activation qui est actuellement actif (la fonction [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) est utilisée pour rendre un contexte d’activation actif).</span><span class="sxs-lookup"><span data-stu-id="fb25e-115">If this flag is not set, the *hActCtx* parameter is ignored and **SxsLookupClrGuid** searches the activation context that is currently active (the [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) function is used to make an activation context active).</span></span><br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <span data-ttu-id="fb25e-116"><dt>**SxS \_ \_Rechercher un GUID CLR de recherche 0x00010000 de \_ \_ \_ substitution**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fb25e-116"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE**</dt> <dt>0x00010000</dt></span></span> </dl>  | <span data-ttu-id="fb25e-117">Si cet indicateur est défini, **SxsLookupClrGuid** recherche un substitut.</span><span class="sxs-lookup"><span data-stu-id="fb25e-117">If this flag is set, **SxsLookupClrGuid** searches for a surrogate.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <span data-ttu-id="fb25e-118"><dt>**SxS \_ RECHERCHE \_ \_ GUID CLR \_ Rechercher \_ la \_ classe CLR**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="fb25e-118"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="fb25e-119">Si cet indicateur est défini, **SxsLookupClrGuid** recherche une classe.</span><span class="sxs-lookup"><span data-stu-id="fb25e-119">If this flag is set, **SxsLookupClrGuid** searches for a class.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <span data-ttu-id="fb25e-120"><dt>**SxS \_ RECHERCHE \_ du \_ GUID CLR \_ Rechercher \_ les**</dt> <dt>0x00030000</dt></span><span class="sxs-lookup"><span data-stu-id="fb25e-120"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_ANY**</dt> <dt>0x00030000</dt></span></span> </dl>                    | <span data-ttu-id="fb25e-121">Il s’agit d’une combinaison de la recherche  **SxS \_ \_ \_ GUID CLR \_ \_** de recherche de substitut et de **\_ recherche SxS \_ GUID CLR Rechercher les indicateurs de \_ \_ \_ \_ classe CLR** ; si les deux sont définis, SxsLookupClrGuid recherche d’abord un substitut, et seulement s’il n’en trouve pas, puis recherche une classe.</span><span class="sxs-lookup"><span data-stu-id="fb25e-121">This is a combination of the **SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE** and **SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS** flags; if both are set, **SxsLookupClrGuid** searches for a surrogate first, and only if it does not find one, then searches for a class.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="fb25e-122">*pClsid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb25e-122">*pClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb25e-123">Pointeur vers le GUID sur lequel rechercher les informations d’interopérabilité dans le contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="fb25e-123">A pointer to the GUID about which to search the activation context for interoperation information.</span></span> <span data-ttu-id="fb25e-124">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="fb25e-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fb25e-125">*hActCtx* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fb25e-125">*hActCtx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb25e-126">Si le **\_ GUID du CLR de recherche SxS \_ \_ \_ utilise \_** l’indicateur ACTCTX est défini dans le paramètre *dwFlags* , *hActCtx* doit contenir un handle de contexte d’activation retourné par la fonction [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="fb25e-126">If the **SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX** flag is set in the *dwFlags* parameter, then *hActCtx* must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="fb25e-127">Sinon, *hActCtx* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="fb25e-127">Otherwise, *hActCtx* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="fb25e-128">*pvOutputBuffer* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fb25e-128">*pvOutputBuffer* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb25e-129">Pointeur vers la mémoire tampon dans laquelle les informations de retour sont copiées.</span><span class="sxs-lookup"><span data-stu-id="fb25e-129">Pointer to the buffer into which return information is copied.</span></span> <span data-ttu-id="fb25e-130">Ce paramètre peut avoir une valeur NULL uniquement si le paramètre *cbOutputBuffer* a une valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="fb25e-130">This parameter may be NULL-valued only if the *cbOutputBuffer* parameter is zero-valued.</span></span> <span data-ttu-id="fb25e-131">Les données placées dans ce tampon à la sortie (le cas échéant) se composent d’une structure **\_ clr d' \_ informations \_ de GUID côte à côte** , suivie de toutes les données de chaîne supplémentaires requises.</span><span class="sxs-lookup"><span data-stu-id="fb25e-131">The data placed in this buffer on exit (if any) consists of a **SXS\_GUID\_INFORMATION\_CLR** structure followed by any additional string data required.</span></span> <span data-ttu-id="fb25e-132">Pour plus d’informations, consultez la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fb25e-132">See the Remarks section below for more information.</span></span>

</dd> <dt>

<span data-ttu-id="fb25e-133">*cbOutputBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb25e-133">*cbOutputBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb25e-134">Taille en octets de la mémoire tampon vers laquelle pointe le paramètre *pvOutputBuffer* .</span><span class="sxs-lookup"><span data-stu-id="fb25e-134">Size in bytes of the buffer pointed to by the *pvOutputBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fb25e-135">*pcbOutputBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb25e-135">*pcbOutputBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb25e-136">Pointeur vers une variable où la taille, en octets, des informations de retour est placée à la sortie.</span><span class="sxs-lookup"><span data-stu-id="fb25e-136">Pointer to a variable where the size, in bytes, of the return information is placed on exit.</span></span> <span data-ttu-id="fb25e-137">Si le paramètre *cbOutputBuffer* est égal à zéro, ou si la taille de la mémoire tampon de sortie est inférieure à la taille des informations de retour, **SxsLookupClrGuid** échoue et [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur de **\_ \_ mémoire tampon insuffisante**.</span><span class="sxs-lookup"><span data-stu-id="fb25e-137">If the *cbOutputBuffer* parameter is zero, or if the size of the output buffer is smaller than the size of the return information, then **SxsLookupClrGuid** fails and [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns an error of **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="fb25e-138">Dans ce cas, utilisez la valeur de la variable vers laquelle pointe *pcbOutputBuffer* pour allouer une mémoire tampon suffisamment grande, puis appelez à nouveau **SxsLookupClrGuid** pour récupérer les informations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="fb25e-138">In this case, use the value in the variable pointed to by *pcbOutputBuffer* to allocate a large enough buffer, and then call **SxsLookupClrGuid** again to retrieve the desired information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb25e-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb25e-139">Return value</span></span>

<span data-ttu-id="fb25e-140">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fb25e-140">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="fb25e-141">Pour plus d’informations sur l’erreur, appelez [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="fb25e-141">For more error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>

## <a name="remarks"></a><span data-ttu-id="fb25e-142">Notes</span><span class="sxs-lookup"><span data-stu-id="fb25e-142">Remarks</span></span>

<span data-ttu-id="fb25e-143">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fb25e-143">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="fb25e-144">Les composants managés peuvent se déclarer comme prenant en charge les « assemblys PIA » managés, afin de permettre à un consommateur de composant Win32 non managé de référencer l’assembly déclarant.</span><span class="sxs-lookup"><span data-stu-id="fb25e-144">Managed components may declare themselves as supporting managed "interop assemblies" so as to allow an unmanaged Win32 component consumer to reference the declaring assembly.</span></span> <span data-ttu-id="fb25e-145">Le consommateur du composant peut interagir avec le composant géré en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) sur un GUID.</span><span class="sxs-lookup"><span data-stu-id="fb25e-145">The component consumer can interact with the managed component by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on a GUID.</span></span> <span data-ttu-id="fb25e-146">La couche d’interopérabilité achemine la demande de création d’objet à .NET Framework, crée une instance de l’objet managé et retourne un pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="fb25e-146">The interoperation layer routes the object creation request to .NET Framework, creates an instance of the managed object, and returns an interface pointer.</span></span>

<span data-ttu-id="fb25e-147">**SxsLookupClrGuid** permet aux frameworks de récupérer les informations associées à un GUID donné dans le manifeste du composant, telles que son nom de classe .net, la version du .NET Framework requis et l’assembly hôte dans lequel il se trouve.</span><span class="sxs-lookup"><span data-stu-id="fb25e-147">**SxsLookupClrGuid** allows the frameworks to retrieve information associated with a given GUID in the component's manifest, such as what its .NET class name is, what version of the .NET Framework it requires, and what host assembly it is located in.</span></span> <span data-ttu-id="fb25e-148">Les composants managés publient un assembly d’interopérabilité qui contient un certain nombre d’instructions associant des GUID à des noms d’assembly et de type, et le Runtime .NET fournit la construction d’instances d’objets managées quand [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) est appelé.</span><span class="sxs-lookup"><span data-stu-id="fb25e-148">Managed components publish an interop assembly that contains a number of statements associating GUIDs with assembly and type names, and the .NET runtime brokers the construction of managed object instances when [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is called.</span></span>

<span data-ttu-id="fb25e-149">Voici un exemple de manifeste de composant déclarant un GUID CLR et un substitut CLR que **SxsLookupClrGuid** peut rechercher :</span><span class="sxs-lookup"><span data-stu-id="fb25e-149">The following is a sample component manifest declaring a CLR GUID and a CLR surrogate that **SxsLookupClrGuid** can look up:</span></span>

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

<span data-ttu-id="fb25e-150">Un fournisseur d’interopérabilité appelle **SxsLookupClrGuid** avec un pointeur vers le GUID « {fdb46ca5-9477-4528-b4b2-7f00a254cdea} » et reçoit dans le nom de classe « MySampleSurrogate », la version de Runtime requise « 1.0.3055 » et l’identité textuelle « dotnet. Sample. substituts, version = «1.0.0.0 », type = « Interop »» du composant d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="fb25e-150">An interoperation provider would call **SxsLookupClrGuid** with a pointer to the GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", and would receive in return the class name "MySampleSurrogate", the required runtime version "1.0.3055", and the textual identity "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" of the hosting component.</span></span>

<span data-ttu-id="fb25e-151">Ces informations de retour sont contenues et/ou référencées par une structure **\_ clr d' \_ informations \_ de GUID SxS** déclarée comme suit.</span><span class="sxs-lookup"><span data-stu-id="fb25e-151">This return information would be contained and/or referenced by a **SXS\_GUID\_INFORMATION\_CLR** structure declared as follows.</span></span>

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

<span data-ttu-id="fb25e-152">Les membres de cette structure contiennent les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb25e-152">The members of this structure contain the following information.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb25e-153">Membre</span><span class="sxs-lookup"><span data-stu-id="fb25e-153">Member</span></span></th>
<th><span data-ttu-id="fb25e-154">Description</span><span class="sxs-lookup"><span data-stu-id="fb25e-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb25e-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span><span class="sxs-lookup"><span data-stu-id="fb25e-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span></span><br/></td>
<td><span data-ttu-id="fb25e-156">Contient la taille de la structure de SXS_GUID_INFORMATION_CLR (cela permet à la structure de croître dans les versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="fb25e-156">Contains the size of the SXS_GUID_INFORMATION_CLR structure (this allows the structure to grow in later versions).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb25e-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span><span class="sxs-lookup"><span data-stu-id="fb25e-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span></span><br/></td>
<td><span data-ttu-id="fb25e-158">Contient l’une des deux valeurs d’indicateur suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb25e-158">Contains one of the following two flag values:</span></span> <br/>
<ul>
<li><span data-ttu-id="fb25e-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001) : indique que le GUID spécifié a été associé à un &quot; substitut.&quot;</span><span class="sxs-lookup"><span data-stu-id="fb25e-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): Indicates that the specified GUID was associated with a &quot;surrogate.&quot;</span></span></li>
<li><span data-ttu-id="fb25e-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002) : indique que le GUID spécifié a été associé à une &quot; classe.&quot;</span><span class="sxs-lookup"><span data-stu-id="fb25e-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): Indicates that the specified GUID was associated with a &quot;class.&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb25e-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span><span class="sxs-lookup"><span data-stu-id="fb25e-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span></span><br/></td>
<td><span data-ttu-id="fb25e-162">Pointe vers une chaîne de caractères larges se terminant par zéro qui identifie la version du runtime spécifiée dans le manifeste hôte pour cette classe.</span><span class="sxs-lookup"><span data-stu-id="fb25e-162">Points to a zero-terminated wide-character string that identifies the version of the runtime specified in the host manifest for this class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb25e-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="fb25e-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span></span><br/></td>
<td><span data-ttu-id="fb25e-164">Pointe vers une chaîne de caractères larges se terminant par zéro qui contient le nom de la classe .NET associée au GUID spécifié.</span><span class="sxs-lookup"><span data-stu-id="fb25e-164">Points to a zero-terminated wide-character string that contains the name of the .NET class associated with the specified GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb25e-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="fb25e-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span></span><br/></td>
<td><span data-ttu-id="fb25e-166">Pointe vers une chaîne de caractères larges se terminant par zéro qui contient l’identité textuelle de l’assembly qui héberge cette classe.</span><span class="sxs-lookup"><span data-stu-id="fb25e-166">Points to a zero-terminated wide-character string that contains the textual identity of the assembly that hosts this class.</span></span> <span data-ttu-id="fb25e-167">Pour plus d’informations sur l’identité textuelle, consultez &quot; spécification de noms de types qualifiés complets &quot; sous &quot; découverte des informations de type au moment de &quot; l’exécution sous &quot; programmation avec l' .NET Framework &quot; dans le kit de développement logiciel (SDK) .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fb25e-167">For more information about textual identity, see &quot;Specifying Fully Qualified Type Names&quot; under &quot;Discovering Type Information at Run Time&quot; under &quot;Programming with the .NET Framework&quot; in the .NET Framework SDK.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fb25e-168">Une application non managée peut utiliser les informations retournées de cette façon pour charger la version appropriée du .NET Framework, charger l’assembly identifié par l’élément **pcwszAssemblyIdentity** , puis créer une instance de la classe nommée par l’élément **pcwszTypeName** .</span><span class="sxs-lookup"><span data-stu-id="fb25e-168">An unmanaged application can use the information returned in this fashion to load the right version of the .NET Framework, load the assembly identified by the **pcwszAssemblyIdentity** element, and then create an instance of the class named by the **pcwszTypeName** element.</span></span>

## <a name="examples"></a><span data-ttu-id="fb25e-169">Exemples</span><span class="sxs-lookup"><span data-stu-id="fb25e-169">Examples</span></span>

<span data-ttu-id="fb25e-170">Utilisez la liaison dynamique comme suit pour appeler la fonction **SxsLookupClrGuid** :</span><span class="sxs-lookup"><span data-stu-id="fb25e-170">Use dynamic linking as follows to call the **SxsLookupClrGuid** function:</span></span>


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a><span data-ttu-id="fb25e-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb25e-171">Requirements</span></span>



| <span data-ttu-id="fb25e-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb25e-172">Requirement</span></span> | <span data-ttu-id="fb25e-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb25e-173">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb25e-174">DLL</span><span class="sxs-lookup"><span data-stu-id="fb25e-174">DLL</span></span><br/> | <dl> <span data-ttu-id="fb25e-175"><dt>Mscoree.dll ; </dt> <dt>Sxs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb25e-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb25e-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb25e-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb25e-177">Applications isolées et assemblys côte à côte</span><span class="sxs-lookup"><span data-stu-id="fb25e-177">Isolated Applications and Side-by-side Assemblies</span></span>](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[<span data-ttu-id="fb25e-178">**CreateActCtx**</span><span class="sxs-lookup"><span data-stu-id="fb25e-178">**CreateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[<span data-ttu-id="fb25e-179">**ActivateActCtx**</span><span class="sxs-lookup"><span data-stu-id="fb25e-179">**ActivateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[<span data-ttu-id="fb25e-180">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="fb25e-180">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
