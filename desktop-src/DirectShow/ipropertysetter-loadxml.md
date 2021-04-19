---
description: La méthode LoadXML charge des données de propriété exprimées en Extensible Markup Language (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'IPropertySetter :: LoadXML, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539577"
---
# <a name="ipropertysetterloadxml-method"></a><span data-ttu-id="dd054-103">IPropertySetter :: LoadXML, méthode</span><span class="sxs-lookup"><span data-stu-id="dd054-103">IPropertySetter::LoadXML method</span></span>

> [!Note]  
> <span data-ttu-id="dd054-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dd054-104">\[Deprecated.</span></span> <span data-ttu-id="dd054-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dd054-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dd054-106">La `LoadXML` méthode charge des données de propriété exprimées en Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="dd054-106">The `LoadXML` method loads property data expressed in Extensible Markup Language (XML).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd054-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd054-107">Syntax</span></span>


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a><span data-ttu-id="dd054-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd054-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd054-109">*pXML* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd054-109">*pxml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd054-110">Pointeur vers l’interface **IUnknown** d’un élément XML créé par l’analyseur XML Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dd054-110">Pointer to the **IUnknown** interface of an XML element created by the Microsoft XML parser.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd054-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd054-111">Return value</span></span>

<span data-ttu-id="dd054-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd054-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dd054-113">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="dd054-113">Possible values include the following.</span></span>



| <span data-ttu-id="dd054-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dd054-114">Return code</span></span>                                                                                                  | <span data-ttu-id="dd054-115">Description</span><span class="sxs-lookup"><span data-stu-id="dd054-115">Description</span></span>                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="dd054-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="dd054-116"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="dd054-117">Aucune donnée de propriété.</span><span class="sxs-lookup"><span data-stu-id="dd054-117">No property data.</span></span><br/>    |
| <dl> <span data-ttu-id="dd054-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd054-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="dd054-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="dd054-119">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="dd054-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="dd054-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                | <span data-ttu-id="dd054-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="dd054-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="dd054-122"><dt>**VFW \_ E \_ \_ format de fichier non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dd054-122"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="dd054-123">Format non valide.</span><span class="sxs-lookup"><span data-stu-id="dd054-123">Invalid format.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="dd054-124">Notes</span><span class="sxs-lookup"><span data-stu-id="dd054-124">Remarks</span></span>

<span data-ttu-id="dd054-125">En règle générale, les applications n’ont pas besoin d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="dd054-125">Typically, applications will not need to use this method.</span></span> <span data-ttu-id="dd054-126">DES l’utilise en interne pour charger des propriétés à partir de fichiers XTL.</span><span class="sxs-lookup"><span data-stu-id="dd054-126">DES uses it internally to load properties from XTL files.</span></span>

<span data-ttu-id="dd054-127">Pour utiliser cette méthode, créez un objet **IXMLDocument** et utilisez-le pour analyser un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="dd054-127">To use this method, create an **IXMLDocument** object and use it to parse an XML file.</span></span> <span data-ttu-id="dd054-128">Utilisez ensuite l’objet **IXMLDocument** pour récupérer des objets **IXMLElement** .</span><span class="sxs-lookup"><span data-stu-id="dd054-128">Then use the **IXMLDocument** object to retrieve **IXMLElement** objects.</span></span> <span data-ttu-id="dd054-129">Si l’objet possède des propriétés, vous pouvez passer le pointeur **IXMLElement** à la méthode **LoadXml** .</span><span class="sxs-lookup"><span data-stu-id="dd054-129">If the object has properties, you can pass the **IXMLElement** pointer to the **LoadXML** method.</span></span> <span data-ttu-id="dd054-130">La méthode charge les propriétés dans l’accesseur Set de propriété.</span><span class="sxs-lookup"><span data-stu-id="dd054-130">The method loads the properties into the property setter.</span></span>

> [!Note]  
> <span data-ttu-id="dd054-131">Les interfaces **IXMLDocument** et **IXMLElement** sont implémentées dans Microsoft XML Core Services (MSXML) version 1,0, mais elles ne sont pas implémentées dans les versions plus récentes de MSXML.</span><span class="sxs-lookup"><span data-stu-id="dd054-131">The **IXMLDocument** and **IXMLElement** interfaces are implemented in Microsoft XML Core Services (MSXML) version 1.0, but are not implemented in more recent versions of MSXML.</span></span>

 

> [!Note]  
> <span data-ttu-id="dd054-132">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="dd054-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dd054-133">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dd054-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dd054-134">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dd054-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dd054-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd054-135">Requirements</span></span>



| <span data-ttu-id="dd054-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd054-136">Requirement</span></span> | <span data-ttu-id="dd054-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd054-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd054-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd054-138">Header</span></span><br/>  | <dl> <span data-ttu-id="dd054-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd054-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dd054-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd054-140">Library</span></span><br/> | <dl> <span data-ttu-id="dd054-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd054-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd054-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd054-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd054-143">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="dd054-143">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="dd054-144">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="dd054-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




