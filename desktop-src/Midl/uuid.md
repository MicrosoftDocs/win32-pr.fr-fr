---
title: uuid (attribut)
description: L’attribut \ UUID \ interface désigne un identificateur universel unique (UUID) qui est affecté à l’interface et qui la distingue des autres interfaces.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- UUID, attribut MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678557"
---
# <a name="uuid-attribute"></a><span data-ttu-id="26c37-104">uuid (attribut)</span><span class="sxs-lookup"><span data-stu-id="26c37-104">uuid attribute</span></span>

<span data-ttu-id="26c37-105">L’attribut d’interface **\[ UUID \]** désigne un identificateur universel unique (UUID) qui est affecté à l’interface et qui la distingue des autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="26c37-105">The **\[uuid\]** interface attribute designates a universally unique identifier (UUID) that is assigned to the interface and that distinguishes it from other interfaces.</span></span>

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a><span data-ttu-id="26c37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26c37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26c37-107">*chaîne-UUID*</span><span class="sxs-lookup"><span data-stu-id="26c37-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="26c37-108">Spécifie une chaîne composée de 8 chiffres hexadécimaux suivis d’un trait d’Union, puis trois groupes de 4 chiffres hexadécimaux chacun suivi d’un trait d’Union, puis 12 chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="26c37-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="26c37-109">Vous pouvez placer la chaîne UUID entre guillemets, sauf si vous utilisez le commutateur de compilateur MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="26c37-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26c37-110">Notes</span><span class="sxs-lookup"><span data-stu-id="26c37-110">Remarks</span></span>

<span data-ttu-id="26c37-111">La bibliothèque Runtime utilise l’UUID de l’interface que l’attribut **\[ UUID \]** désigne pour aider à établir la communication entre les applications client et serveur.</span><span class="sxs-lookup"><span data-stu-id="26c37-111">The run-time library uses the interface UUID that the **\[uuid\]** attribute designates to help establish communication between the client and server applications.</span></span> <span data-ttu-id="26c37-112">L’attribut **\[ UUID \]** peut apparaître dans la liste des attributs de l’interface pour une interface RPC ou une interface com.</span><span class="sxs-lookup"><span data-stu-id="26c37-112">The **\[uuid\]** attribute can appear in the interface attribute list for either an RPC interface or a COM interface.</span></span>

<span data-ttu-id="26c37-113">Pour une interface RPC, la liste des attributs d’interface doit inclure l’attribut **\[ UUID \]** ou l' **\[** [](local.md) **\]** attribut local, et celle que vous choisissez doit se produire exactement une fois.</span><span class="sxs-lookup"><span data-stu-id="26c37-113">For an RPC interface, the interface attribute list must include either the **\[uuid\]** attribute or the **\[**[**local**](local.md)**\]** attribute, and the one you choose must occur exactly once.</span></span> <span data-ttu-id="26c37-114">Si la liste inclut l’attribut **\[ UUID \]** , elle peut également inclure l' **\[** attribut [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="26c37-114">If the list includes the **\[uuid\]** attribute, it can also include the **\[**[**version**](version.md)**\]** attribute.</span></span>

<span data-ttu-id="26c37-115">Pour une interface COM (identifiée par l’attribut interface de l' **\[** [**objet**](object.md) **\]** ), la liste des attributs de l’interface doit inclure l’attribut **\[ UUID \]** , mais elle ne peut pas inclure l’attribut **\[ version \]** .</span><span class="sxs-lookup"><span data-stu-id="26c37-115">For a COM interface (identified by the **\[**[**object**](object.md)**\]** interface attribute), the interface attribute list must include the **\[uuid\]** attribute, but it cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="26c37-116">La liste d’une interface COM peut inclure l’attribut **\[ local \]** même si l’attribut **\[ UUID \]** est présent.</span><span class="sxs-lookup"><span data-stu-id="26c37-116">The list for a COM interface can include the **\[local\]** attribute even though the **\[uuid\]** attribute is present.</span></span>

<span data-ttu-id="26c37-117">Microsoft RPC prend en charge une extension de l’IDL DCE qui autorise l’UUID à être placé entre guillemets doubles ("" ").</span><span class="sxs-lookup"><span data-stu-id="26c37-117">Microsoft RPC supports an extension to DCE IDL that allows the UUID to be enclosed in double quotation marks ("" "").</span></span> <span data-ttu-id="26c37-118">La forme entre guillemets est nécessaire pour les préprocesseurs de compilateur C qui interprètent les valeurs UUID comme des nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="26c37-118">The quoted form is needed for C-compiler preprocessors that interpret UUID numbers as floating-point numbers.</span></span>

<span data-ttu-id="26c37-119">Toutes les valeurs UUID doivent être générées par ordinateur pour garantir l’unicité.</span><span class="sxs-lookup"><span data-stu-id="26c37-119">All UUID values should be computer-generated to guarantee uniqueness.</span></span> <span data-ttu-id="26c37-120">Utilisez l’utilitaire uuidgen pour générer des valeurs UUID uniques.</span><span class="sxs-lookup"><span data-stu-id="26c37-120">Use the Uuidgen utility to generate unique UUID values.</span></span>

<span data-ttu-id="26c37-121">L’UUID et les numéros de version de l’interface sont utilisés pour déterminer si le client peut effectuer une liaison avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="26c37-121">The UUID and version numbers of the interface are used to determine whether the client can bind to the server.</span></span> <span data-ttu-id="26c37-122">Pour que le client se lie au serveur, l’UUID spécifié dans les interfaces client et serveur doit être identique.</span><span class="sxs-lookup"><span data-stu-id="26c37-122">For the client to bind to the server, the UUID specified in the client and server interfaces must be the same.</span></span>

<span data-ttu-id="26c37-123">Notez qu’une interface sans attributs peut être importée dans un fichier IDL de base.</span><span class="sxs-lookup"><span data-stu-id="26c37-123">Note that an interface without attributes can be imported into a base IDL file.</span></span> <span data-ttu-id="26c37-124">Toutefois, l’interface ne doit contenir que des types de données sans procédures.</span><span class="sxs-lookup"><span data-stu-id="26c37-124">However, the interface must contain only datatypes with no procedures.</span></span> <span data-ttu-id="26c37-125">Si même une procédure est contenue dans l’interface, un attribut local ou UUID doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="26c37-125">If even one procedure is contained in the interface, a local or UUID attribute must be specified.</span></span>

## <a name="examples"></a><span data-ttu-id="26c37-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="26c37-126">Examples</span></span>

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a><span data-ttu-id="26c37-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26c37-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c37-128">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="26c37-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="26c37-129">**interface**</span><span class="sxs-lookup"><span data-stu-id="26c37-129">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="26c37-130">**localisé**</span><span class="sxs-lookup"><span data-stu-id="26c37-130">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="26c37-131">**object**</span><span class="sxs-lookup"><span data-stu-id="26c37-131">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="26c37-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="26c37-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="26c37-133">**Version**</span><span class="sxs-lookup"><span data-stu-id="26c37-133">**version**</span></span>](version.md)
</dt> </dl>

 

 




