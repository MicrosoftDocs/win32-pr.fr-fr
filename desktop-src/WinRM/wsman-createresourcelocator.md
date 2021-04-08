---
title: Méthode WSMan. CreateResourceLocator (WSManDisp. h)
description: Crée un objet ResourceLocator qui peut être utilisé au lieu de spécifier un URI de ressource dans les opérations d’objet de session, telles que session. obtenir, session. put ou session. Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode CreateResourceLocator
- Méthode CreateResourceLocator Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode CreateResourceLocator
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942041"
---
# <a name="wsmancreateresourcelocator-method"></a><span data-ttu-id="f17a2-106">Méthode WSMan. CreateResourceLocator</span><span class="sxs-lookup"><span data-stu-id="f17a2-106">WSMan.CreateResourceLocator method</span></span>

<span data-ttu-id="f17a2-107">Crée un objet [**ResourceLocator**](resourcelocator.md) qui peut être utilisé au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="f17a2-107">Creates a [**ResourceLocator**](resourcelocator.md) object that can be used instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f17a2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f17a2-108">Syntax</span></span>


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f17a2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f17a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f17a2-110">*URI* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f17a2-110">*uri* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f17a2-111">URI de ressource pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="f17a2-111">The resource URI for the resource.</span></span> <span data-ttu-id="f17a2-112">Pour plus d’informations sur les chaînes d’URI, consultez [URI de ressource](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="f17a2-112">For more information about URI strings, see [Resource URIs](resource-uris.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f17a2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f17a2-113">Return value</span></span>

<span data-ttu-id="f17a2-114">Objet [**ResourceLocator**](resourcelocator.md) qui peut ensuite être utilisé pour effectuer des opérations WinRM locales ou distantes.</span><span class="sxs-lookup"><span data-stu-id="f17a2-114">A [**ResourceLocator**](resourcelocator.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="f17a2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f17a2-115">Remarks</span></span>

<span data-ttu-id="f17a2-116">Si la propriété **FragmentDialect** n’est pas spécifiée dans l’objet [**ResourceLocator**](resourcelocator.md) , la valeur par défaut est la spécification XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="f17a2-116">If the **FragmentDialect** property is not specified in the [**ResourceLocator**](resourcelocator.md) object, the default is the XPath 1.0 specification.</span></span> <span data-ttu-id="f17a2-117">Pour plus d’informations, consultez [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="f17a2-117">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="examples"></a><span data-ttu-id="f17a2-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="f17a2-118">Examples</span></span>

<span data-ttu-id="f17a2-119">L’exemple de code VBScript suivant crée un objet [**ResourceLocator**](resourcelocator.md) et obtient la valeur de la propriété **Description** de la carte réseau à partir de l’instance de [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) avec un index de « 1 ».</span><span class="sxs-lookup"><span data-stu-id="f17a2-119">The following VBScript code example creates a [**ResourceLocator**](resourcelocator.md) object and gets the network adapter **Description** property value from the instance of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) with an Index of "1".</span></span>


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a><span data-ttu-id="f17a2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f17a2-120">Requirements</span></span>



| <span data-ttu-id="f17a2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f17a2-121">Requirement</span></span> | <span data-ttu-id="f17a2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f17a2-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f17a2-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f17a2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f17a2-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f17a2-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f17a2-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f17a2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f17a2-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f17a2-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f17a2-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f17a2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f17a2-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f17a2-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f17a2-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="f17a2-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f17a2-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f17a2-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f17a2-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f17a2-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f17a2-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f17a2-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f17a2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f17a2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f17a2-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f17a2-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f17a2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f17a2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f17a2-136">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="f17a2-136">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="f17a2-137">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="f17a2-137">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="f17a2-138">**session**</span><span class="sxs-lookup"><span data-stu-id="f17a2-138">**Session**</span></span>](session.md)
</dt> </dl>

 

