---
description: Enregistre les modèles dans un fichier DirectX. Action déconseillée.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'IDirectXFileSaveObject :: SaveTemplates, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322845"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a><span data-ttu-id="7b2ca-104">IDirectXFileSaveObject :: SaveTemplates, méthode</span><span class="sxs-lookup"><span data-stu-id="7b2ca-104">IDirectXFileSaveObject::SaveTemplates method</span></span>

<span data-ttu-id="7b2ca-105">Enregistre les modèles dans un fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="7b2ca-105">Saves templates to a DirectX file.</span></span> <span data-ttu-id="7b2ca-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7b2ca-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b2ca-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b2ca-107">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a><span data-ttu-id="7b2ca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b2ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b2ca-109">*cTemplates* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b2ca-109">*cTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2ca-110">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b2ca-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b2ca-111">Nombre total de modèles à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="7b2ca-111">Total number of templates to save.</span></span>

</dd> <dt>

<span data-ttu-id="7b2ca-112">*ppguidTemplates* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b2ca-112">*ppguidTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2ca-113">Type : **const [**GUID**](guid.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="7b2ca-113">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="7b2ca-114">Adresse d’un pointeur vers un tableau de GUID pour tous les modèles à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="7b2ca-114">Address of a pointer to an array of the GUIDs for all templates to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b2ca-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b2ca-115">Return value</span></span>

<span data-ttu-id="7b2ca-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b2ca-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b2ca-117">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b2ca-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="7b2ca-118">Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="7b2ca-118">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b2ca-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7b2ca-119">Remarks</span></span>

<span data-ttu-id="7b2ca-120">Le fragment de code suivant fournit un exemple d’appel à **IDirectXFileSaveObject :: SaveTemplates** et un exemple de contenu pour le tableau auquel ppguidTemplates pointe.</span><span class="sxs-lookup"><span data-stu-id="7b2ca-120">The following code fragment provides an example call to **IDirectXFileSaveObject::SaveTemplates** and example contents for the array to which ppguidTemplates points.</span></span>


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



<span data-ttu-id="7b2ca-121">Après avoir utilisé cette méthode pour enregistrer les modèles, utilisez la méthode [**IDirectXFileSaveObject :: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) pour créer un objet de données.</span><span class="sxs-lookup"><span data-stu-id="7b2ca-121">After using this method to save the templates, use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b2ca-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b2ca-122">Requirements</span></span>



| <span data-ttu-id="7b2ca-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b2ca-123">Requirement</span></span> | <span data-ttu-id="7b2ca-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b2ca-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2ca-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b2ca-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7b2ca-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b2ca-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b2ca-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7b2ca-127">Library</span></span><br/> | <dl> <span data-ttu-id="7b2ca-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b2ca-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b2ca-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b2ca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b2ca-130">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="7b2ca-130">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="7b2ca-131">**IDirectXFileSaveObject::CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="7b2ca-131">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
