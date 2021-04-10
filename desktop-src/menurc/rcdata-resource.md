---
title: Ressource RCDATA
description: Définit une ressource de données brutes pour une application. Les ressources de données brutes permettent d’inclure des données binaires directement dans le fichier exécutable.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menus des ressources RCDATA et autres ressources
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940498"
---
# <a name="rcdata-resource"></a><span data-ttu-id="d7752-105">Ressource RCDATA</span><span class="sxs-lookup"><span data-stu-id="d7752-105">RCDATA resource</span></span>

<span data-ttu-id="d7752-106">Définit une ressource de données brutes pour une application.</span><span class="sxs-lookup"><span data-stu-id="d7752-106">Defines a raw data resource for an application.</span></span> <span data-ttu-id="d7752-107">Les ressources de données brutes permettent d’inclure des données binaires directement dans le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="d7752-107">Raw data resources permit the inclusion of binary data directly in the executable file.</span></span>

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a><span data-ttu-id="d7752-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7752-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7752-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="d7752-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="d7752-110">Nom unique ou valeur d’entier non signé 16 bits qui identifie la ressource.</span><span class="sxs-lookup"><span data-stu-id="d7752-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="d7752-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*</span><span class="sxs-lookup"><span data-stu-id="d7752-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="d7752-112">Ce paramètre peut être égal à zéro ou plusieurs des instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7752-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="d7752-113">.</span><span class="sxs-lookup"><span data-stu-id="d7752-113">Statement</span></span>                                                        | <span data-ttu-id="d7752-114">Description</span><span class="sxs-lookup"><span data-stu-id="d7752-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7752-115">[**Caractéristiques**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="d7752-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="d7752-116">Informations définies par l’utilisateur sur une ressource qui peuvent être utilisées par des outils qui lisent et écrivent des fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="d7752-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="d7752-117">Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d7752-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="d7752-118">[](language-statement.md) *Langue* langue, sous- *langue*</span><span class="sxs-lookup"><span data-stu-id="d7752-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="d7752-119">Langue de la ressource.</span><span class="sxs-lookup"><span data-stu-id="d7752-119">Language for the resource.</span></span> <span data-ttu-id="d7752-120">Pour plus d’informations, consultez [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d7752-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="d7752-121">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="d7752-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="d7752-122">Numéro de version défini par l’utilisateur pour la ressource qui peut être utilisé par les outils qui lisent et écrivent les fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="d7752-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="d7752-123">Pour plus d’informations, consultez [**version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d7752-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="d7752-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*données brutes*</span><span class="sxs-lookup"><span data-stu-id="d7752-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="d7752-125">Données brutes constituées d’un ou plusieurs entiers ou chaînes de caractères.</span><span class="sxs-lookup"><span data-stu-id="d7752-125">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="d7752-126">Les entiers peuvent être spécifiés au format décimal, octal ou hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="d7752-126">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="d7752-127">Pour être compatible avec Windows 16 bits, les entiers sont stockés sous la forme de valeurs **Word** .</span><span class="sxs-lookup"><span data-stu-id="d7752-127">To be compatible with 16-bit Windows, integers are stored as **WORD** values.</span></span> <span data-ttu-id="d7752-128">Vous pouvez stocker un entier comme valeur **DWORD** en qualifiant l’entier avec le suffixe « L ».</span><span class="sxs-lookup"><span data-stu-id="d7752-128">You can store an integer as a **DWORD** value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="d7752-129">Les chaînes sont placées entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="d7752-129">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="d7752-130">RC n’ajoute pas automatiquement un caractère null de fin à une chaîne.</span><span class="sxs-lookup"><span data-stu-id="d7752-130">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="d7752-131">Chaque chaîne est une séquence de caractères ANSI spécifiée, sauf si vous la qualifiez comme une chaîne de caractères larges avec le préfixe L.</span><span class="sxs-lookup"><span data-stu-id="d7752-131">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the L prefix.</span></span>

<span data-ttu-id="d7752-132">Le bloc de données commence sur une limite **DWORD** et RC n’effectue aucun remplissage ou alignement des données dans le bloc de *données brutes* .</span><span class="sxs-lookup"><span data-stu-id="d7752-132">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="d7752-133">Il vous incombe de garantir l’alignement correct des données dans le bloc.</span><span class="sxs-lookup"><span data-stu-id="d7752-133">It is your responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

<span data-ttu-id="d7752-134">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="d7752-134">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="d7752-135">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d7752-135">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d7752-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="d7752-136">Examples</span></span>

<span data-ttu-id="d7752-137">L’exemple suivant illustre l’utilisation de l’instruction **RCDATA** :</span><span class="sxs-lookup"><span data-stu-id="d7752-137">The following example demonstrates the use of the **RCDATA** statement:</span></span>

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a><span data-ttu-id="d7752-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7752-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7752-139">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="d7752-139">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="d7752-140">**ATTRIBUTS**</span><span class="sxs-lookup"><span data-stu-id="d7752-140">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="d7752-141">**SOUS**</span><span class="sxs-lookup"><span data-stu-id="d7752-141">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="d7752-142">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="d7752-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="d7752-143">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="d7752-143">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="d7752-144">**Version**</span><span class="sxs-lookup"><span data-stu-id="d7752-144">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 




