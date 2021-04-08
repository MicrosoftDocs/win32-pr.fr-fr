---
title: Méthodes de propriété IADsNamespaces (IADs. h)
description: Les méthodes de propriété de l’interface IADsNamespaces obtiennent et définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsNamespaces ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742693"
---
# <a name="iadsnamespaces-property-methods"></a><span data-ttu-id="a9cd8-105">Méthodes de propriété IADsNamespaces</span><span class="sxs-lookup"><span data-stu-id="a9cd8-105">IADsNamespaces Property Methods</span></span>

<span data-ttu-id="a9cd8-106">Les méthodes de propriété de l’interface [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) obtiennent et définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-106">The [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) interface property methods get and set the properties described in the following table.</span></span> <span data-ttu-id="a9cd8-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a9cd8-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a9cd8-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9cd8-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="a9cd8-109">**DefaultContainer**</span><span class="sxs-lookup"><span data-stu-id="a9cd8-109">**DefaultContainer**</span></span>
<span data-ttu-id="a9cd8-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a9cd8-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="a9cd8-111">La propriété **DefaultContainer** identifie un objet conteneur de base auquel vous pouvez lier et utiliser comme point de départ lors de la navigation.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-111">The **DefaultContainer** property identifies a base container object to which you can bind and use as a starting point when browsing.</span></span> <span data-ttu-id="a9cd8-112">Ces données sont stockées et récupérées à partir de la valeur de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-112">This data is stored and retrieved from the following registry value.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

<span data-ttu-id="a9cd8-113">ADSI définit la propriété **DefaultContainer** pour fournir un moyen rapide d’obtenir un pointeur vers un objet conteneur ADSI précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-113">ADSI defines the **DefaultContainer** property to provide a quick way of getting a pointer to a previously defined ADSI container object.</span></span>

<dt>

<span data-ttu-id="a9cd8-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a9cd8-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a9cd8-115">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a9cd8-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="a9cd8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a9cd8-116">Remarks</span></span>

<span data-ttu-id="a9cd8-117">Les fournisseurs doivent fournir cette propriété pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-117">Providers must supply this property on a per-user basis.</span></span> <span data-ttu-id="a9cd8-118">Le conteneur par défaut est défini immédiatement après l’appel de **IADsNamespaces ::p ut \_ DefaultContainer**.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-118">The default container is set immediately after the invocation of **IADsNamespaces::put\_DefaultContainer**.</span></span> <span data-ttu-id="a9cd8-119">L’appel de [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) n’est pas requis.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-119">Calling [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) is not required.</span></span> <span data-ttu-id="a9cd8-120">En fait, l’objet espaces de noms fourni par le système renvoie **E \_ NOTIMPL** pour la méthode **IADs. setinfo** appelée sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-120">In fact, the system-supplied namespaces object returns **E\_NOTIMPL** for the **IADs.SetInfo** method called on this object.</span></span> <span data-ttu-id="a9cd8-121">Lorsqu’un conteneur est l’objet Namespaces, une opération d’énumération produit toujours une liste d’objets d’espace de noms spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-121">When a container is the namespaces object, an enumeration operation always results in a list of provider-specific namespace objects.</span></span> <span data-ttu-id="a9cd8-122">Quand [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) est utilisé pour obtenir un objet Namespace, le paramètre *bstrClass* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-122">When [**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) is used to obtain a namespace object, the *bstrClass* parameter is ignored.</span></span> <span data-ttu-id="a9cd8-123">Cela est dû au fait que le conteneur, autrement dit, l’objet Namespaces, contient un seul type d’objet, à savoir les objets d’espace de noms spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a9cd8-123">This is because the container, that is, the namespaces object, contains only one type of object, namely, provider-specific namespace objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9cd8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9cd8-124">Requirements</span></span>



| <span data-ttu-id="a9cd8-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9cd8-125">Requirement</span></span> | <span data-ttu-id="a9cd8-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9cd8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9cd8-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9cd8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a9cd8-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9cd8-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9cd8-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9cd8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a9cd8-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9cd8-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9cd8-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9cd8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9cd8-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9cd8-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="a9cd8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a9cd8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9cd8-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9cd8-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="a9cd8-135">IID</span><span class="sxs-lookup"><span data-stu-id="a9cd8-135">IID</span></span><br/>                      | <span data-ttu-id="a9cd8-136">IID \_ IADsNamespaces est défini en tant que 28B96BA0-B330-11CF-A9AD-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="a9cd8-136">IID\_IADsNamespaces is defined as 28B96BA0-B330-11CF-A9AD-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a9cd8-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9cd8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9cd8-138">**IADsContainer. GetObject**</span><span class="sxs-lookup"><span data-stu-id="a9cd8-138">**IADsContainer.GetObject**</span></span>](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[<span data-ttu-id="a9cd8-139">**IADsNamespaces**</span><span class="sxs-lookup"><span data-stu-id="a9cd8-139">**IADsNamespaces**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[<span data-ttu-id="a9cd8-140">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="a9cd8-140">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





