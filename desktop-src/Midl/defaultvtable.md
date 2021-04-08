---
title: defaultvtable (attribut)
description: L’attribut \ defaultvtable \ définit une interface en tant qu’interface vtable par défaut.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- MIDL de l’attribut defaultvtable
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842233"
---
# <a name="defaultvtable-attribute"></a><span data-ttu-id="1b073-104">defaultvtable (attribut)</span><span class="sxs-lookup"><span data-stu-id="1b073-104">defaultvtable attribute</span></span>

<span data-ttu-id="1b073-105">L’attribut **\[ defaultvtable \]** définit une interface en tant qu’interface vtable par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b073-105">The **\[defaultvtable\]** attribute defines an interface as the default Vtable interface.</span></span>

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="1b073-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b073-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b073-107">*coclass-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="1b073-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1b073-108">Autres attributs qui s’appliquent à la classe.</span><span class="sxs-lookup"><span data-stu-id="1b073-108">Other attributes that apply to the class.</span></span> <span data-ttu-id="1b073-109">Les **\[** [](source.md) **\]** attributs source et **\[** [**UUID**](uuid.md) **\]** sont requis.</span><span class="sxs-lookup"><span data-stu-id="1b073-109">The **\[**[**source**](source.md)**\]** and **\[**[**uuid**](uuid.md)**\]** attributes are required.</span></span>

</dd> <dt>

<span data-ttu-id="1b073-110">*nom de la coclasse*</span><span class="sxs-lookup"><span data-stu-id="1b073-110">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1b073-111">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="1b073-111">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="1b073-112">*coclass-interface-List*</span><span class="sxs-lookup"><span data-stu-id="1b073-112">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1b073-113">Liste des interfaces pour la classe.</span><span class="sxs-lookup"><span data-stu-id="1b073-113">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b073-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1b073-114">Remarks</span></span>

<span data-ttu-id="1b073-115">Une interface vtable par défaut ne peut pas être une dispinterface ; il doit s’agir d’une interface double ou vtable ou d’une interface.</span><span class="sxs-lookup"><span data-stu-id="1b073-115">A default Vtable interface cannot be a dispinterface—it must be a dual or Vtable or interface.</span></span> <span data-ttu-id="1b073-116">Si l’interface est une interface double, les récepteurs peuvent supposer qu’ils recevront des événements via vtable.</span><span class="sxs-lookup"><span data-stu-id="1b073-116">If the interface is a dual interface, then sinks can assume that they will receive events through Vtable.</span></span>

<span data-ttu-id="1b073-117">Une classe peut être à la fois une interface source par défaut et une interface source vtable par défaut, comme indiqué dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="1b073-117">A class can be both a default source interface and a default Vtable source interface as shown in the example.</span></span> <span data-ttu-id="1b073-118">Dans ce cas, un récepteur de notification doit utiliser \_ l’IID IDISPATCH pour recevoir les événements de dispatch et utiliser l’identificateur d’interface pour recevoir des événements vtable.</span><span class="sxs-lookup"><span data-stu-id="1b073-118">In this case an advise sink should use IID\_IDISPATCH to receive dispatch events and use the interface identifier to receive Vtable events.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="1b073-119">Représentation TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="1b073-119">Typeflag Representation</span></span>

<span data-ttu-id="1b073-120">Présence de IMPLTYPEFLAG \_ FDEFAULTVTABLE.</span><span class="sxs-lookup"><span data-stu-id="1b073-120">The presence of IMPLTYPEFLAG\_FDEFAULTVTABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="1b073-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="1b073-121">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="1b073-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b073-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b073-123">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="1b073-123">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="1b073-124">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="1b073-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="1b073-125">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="1b073-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="1b073-126">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="1b073-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="1b073-127">**code**</span><span class="sxs-lookup"><span data-stu-id="1b073-127">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="1b073-128">**universel**</span><span class="sxs-lookup"><span data-stu-id="1b073-128">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 