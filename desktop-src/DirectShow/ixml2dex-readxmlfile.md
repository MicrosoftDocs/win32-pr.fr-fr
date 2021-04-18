---
description: La méthode ReadXMLFile charge un fichier de projet XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'IXml2Dex :: ReadXMLFile, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540665"
---
# <a name="ixml2dexreadxmlfile-method"></a><span data-ttu-id="8b7eb-103">IXml2Dex :: ReadXMLFile, méthode</span><span class="sxs-lookup"><span data-stu-id="8b7eb-103">IXml2Dex::ReadXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="8b7eb-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-104">\[Deprecated.</span></span> <span data-ttu-id="8b7eb-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b7eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8b7eb-106">La `ReadXMLFile` méthode charge un fichier projet XML.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-106">The `ReadXMLFile` method loads an XML project file.</span></span> <span data-ttu-id="8b7eb-107">Cette méthode crée des instances de tous les objets exprimés dans le fichier XML et les insère dans la chronologie, ainsi que l’application de tous les attributs fournis pour la chronologie, tels que la fréquence d’images ou l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-107">This method creates instances of all the objects expressed in the XML file and inserts them into the timeline, as well as applying any attributes given for the timeline, such as frame rate or default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b7eb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b7eb-108">Syntax</span></span>


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a><span data-ttu-id="8b7eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b7eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b7eb-110">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="8b7eb-110">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="8b7eb-111">Pointeur vers l’interface **IUnknown** d’un objet Timeline.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-111">Pointer to a timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="8b7eb-112">*XMLName*</span><span class="sxs-lookup"><span data-stu-id="8b7eb-112">*XMLName*</span></span> 
</dt> <dd>

<span data-ttu-id="8b7eb-113">Chaîne qui spécifie le nom du fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-113">String that specifies the name of the file to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b7eb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b7eb-114">Return value</span></span>

<span data-ttu-id="8b7eb-115">Retourne une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-115">Returns an HRESULT value.</span></span> <span data-ttu-id="8b7eb-116">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-116">Possible values include the following.</span></span>



| <span data-ttu-id="8b7eb-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8b7eb-117">Return code</span></span>                                                                                                  | <span data-ttu-id="8b7eb-118">Description</span><span class="sxs-lookup"><span data-stu-id="8b7eb-118">Description</span></span>                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="8b7eb-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b7eb-119"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="8b7eb-120">Succès</span><span class="sxs-lookup"><span data-stu-id="8b7eb-120">Success</span></span><br/>             |
| <dl> <span data-ttu-id="8b7eb-121"><dt>**VFW \_ E \_ \_ format de fichier non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b7eb-121"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="8b7eb-122">Format de fichier non valide</span><span class="sxs-lookup"><span data-stu-id="8b7eb-122">Invalid file format</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8b7eb-123">Notes</span><span class="sxs-lookup"><span data-stu-id="8b7eb-123">Remarks</span></span>

<span data-ttu-id="8b7eb-124">Cette méthode n’efface pas les objets existants de la chronologie avant d’insérer les nouveaux objets définis dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-124">This method does not clear existing objects from the timeline before it inserts the new objects defined in the XML file.</span></span> <span data-ttu-id="8b7eb-125">Si vous devez actualiser une chronologie existante, appelez d’abord [**IAMTimeline :: ClearAllGroups**](iamtimeline-clearallgroups.md) .</span><span class="sxs-lookup"><span data-stu-id="8b7eb-125">If you need to refresh an existing timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) first.</span></span>

> [!Note]  
> <span data-ttu-id="8b7eb-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8b7eb-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8b7eb-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8b7eb-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8b7eb-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b7eb-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b7eb-129">Requirements</span></span>



| <span data-ttu-id="8b7eb-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b7eb-130">Requirement</span></span> | <span data-ttu-id="8b7eb-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b7eb-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7eb-132">Version</span><span class="sxs-lookup"><span data-stu-id="8b7eb-132">Version</span></span><br/> | <span data-ttu-id="8b7eb-133">Internet Explorer 4,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8b7eb-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="8b7eb-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b7eb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8b7eb-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b7eb-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8b7eb-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8b7eb-136">Library</span></span><br/> | <dl> <span data-ttu-id="8b7eb-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b7eb-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b7eb-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b7eb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b7eb-139">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="8b7eb-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="8b7eb-140">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="8b7eb-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




