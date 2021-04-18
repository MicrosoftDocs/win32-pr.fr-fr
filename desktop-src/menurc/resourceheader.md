---
title: RESOURCEHEADER, structure
description: Contient des informations sur l’en-tête de ressource lui-même et les données spécifiques à cette ressource.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Menus de la structure RESOURCEHEADER et autres ressources
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512147"
---
# <a name="resourceheader-structure"></a><span data-ttu-id="0cccd-104">RESOURCEHEADER, structure</span><span class="sxs-lookup"><span data-stu-id="0cccd-104">RESOURCEHEADER structure</span></span>

<span data-ttu-id="0cccd-105">Contient des informations sur l’en-tête de ressource lui-même et les données spécifiques à cette ressource.</span><span class="sxs-lookup"><span data-stu-id="0cccd-105">Contains information about the resource header itself and the data specific to this resource.</span></span> <span data-ttu-id="0cccd-106">Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="0cccd-106">This structure is not a true C-language structure, because it contains variable-length members.</span></span> <span data-ttu-id="0cccd-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="0cccd-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cccd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cccd-108">Syntax</span></span>


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a><span data-ttu-id="0cccd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0cccd-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0cccd-110">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="0cccd-110">**DataSize**</span></span>
</dt> <dd>

<span data-ttu-id="0cccd-111">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cccd-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0cccd-112">Taille, en octets, des données qui suivent l’en-tête de ressource pour cette ressource particulière.</span><span class="sxs-lookup"><span data-stu-id="0cccd-112">The size, in bytes, of the data that follows the resource header for this particular resource.</span></span> <span data-ttu-id="0cccd-113">Elle n’inclut pas le remplissage des fichiers entre cette ressource et toute ressource qui la suit dans le fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="0cccd-113">It does not include any file padding between this resource and any resource that follows it in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="0cccd-114">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="0cccd-114">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="0cccd-115">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cccd-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0cccd-116">Taille, en octets, des données d’en-tête de ressource qui suivent.</span><span class="sxs-lookup"><span data-stu-id="0cccd-116">The size, in bytes, of the resource header data that follows.</span></span>

</dd> <dt>

<span data-ttu-id="0cccd-117">**TYPE**</span><span class="sxs-lookup"><span data-stu-id="0cccd-117">**TYPE**</span></span>
</dt> <dd>

<span data-ttu-id="0cccd-118">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cccd-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0cccd-119">Type de ressource.</span><span class="sxs-lookup"><span data-stu-id="0cccd-119">The resource type.</span></span> <span data-ttu-id="0cccd-120">Le membre de **type** peut être une valeur numérique ou une chaîne Unicode terminée par le caractère null qui spécifie le nom du type.</span><span class="sxs-lookup"><span data-stu-id="0cccd-120">The **TYPE** member can either be a numeric value or a null-terminated Unicode string that specifies the name of the type.</span></span> <span data-ttu-id="0cccd-121">Consultez la section Notes suivante pour obtenir une description des membres de type **nom** ou **ordinal** .</span><span class="sxs-lookup"><span data-stu-id="0cccd-121">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="0cccd-122">Si le membre de **type** est une valeur numérique, il peut spécifier un type de ressource standard ou défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0cccd-122">If the **TYPE** member is a numeric value, it can specify either a standard or a user-defined resource type.</span></span> <span data-ttu-id="0cccd-123">Si le membre est une chaîne, il s’agit d’un type de ressource défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0cccd-123">If the member is a string, then it is a user-defined resource type.</span></span> <span data-ttu-id="0cccd-124">Pour obtenir la liste des types de ressources prédéfinis, consultez [types de ressources](/windows/desktop/menurc/resource-types).</span><span class="sxs-lookup"><span data-stu-id="0cccd-124">For a list of the predefined resource types, see [Resource Types](/windows/desktop/menurc/resource-types).</span></span>

<span data-ttu-id="0cccd-125">Les valeurs inférieures à 256 sont réservées à l’utilisation du système.</span><span class="sxs-lookup"><span data-stu-id="0cccd-125">Values less than 256 are reserved for system use.</span></span>

</dd> <dt>

<span data-ttu-id="0cccd-126">**NAME**</span><span class="sxs-lookup"><span data-stu-id="0cccd-126">**NAME**</span></span>
</dt> <dd>

<span data-ttu-id="0cccd-127">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cccd-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0cccd-128">Nom qui identifie la ressource particulière.</span><span class="sxs-lookup"><span data-stu-id="0cccd-128">A name that identifies the particular resource.</span></span> <span data-ttu-id="0cccd-129">Le membre de **nom** , comme le membre de **type** , peut être une valeur numérique ou une chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="0cccd-129">The **NAME** member, like the **TYPE** member, can either be a numeric value or a null-terminated Unicode string.</span></span> <span data-ttu-id="0cccd-130">Consultez la section Notes suivante pour obtenir une description des membres de type **nom** ou **ordinal** .</span><span class="sxs-lookup"><span data-stu-id="0cccd-130">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="0cccd-131">Vous n’avez pas besoin d’ajouter un remplissage pour l’alignement **DWORD** entre le **type** et les membres de **nom** , car ils contiennent des données **Word** .</span><span class="sxs-lookup"><span data-stu-id="0cccd-131">You do not need to add padding for **DWORD** alignment between the **TYPE** and **NAME** members because they contain **WORD** data.</span></span> <span data-ttu-id="0cccd-132">Toutefois, vous devrez peut-être ajouter un **mot** de remplissage après le membre **Name** pour aligner le reste de l’en-tête sur les limites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0cccd-132">However, you may need to add a **WORD** of padding after the **NAME** member to align the rest of the header on **DWORD** boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="0cccd-133">**DataVersion**</span><span class="sxs-lookup"><span data-stu-id="0cccd-133">**DataVersion**</span></span>
</dt> <dd>

<span data-ttu-id="0cccd-134">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cccd-134">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0cccd-135">Version de données de ressource prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="0cccd-135">A predefined resource data version.</span></span> <span data-ttu-id="0cccd-136">Cela permet de déterminer la version des données de ressource que l’application doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="0cccd-136">This will determine which version of the resource data the application should use.</span></span>

</dd> <dt>

<span data-ttu-id="0cccd-137">**MemoryFlags**</span><span class="sxs-lookup"><span data-stu-id="0cccd-137">**MemoryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0cccd-138">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="0cccd-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0cccd-139">Ensemble d’indicateurs d’attribut qui peuvent décrire l’état de la ressource.</span><span class="sxs-lookup"><span data-stu-id="0cccd-139">A set of attribute flags that can describe the state of the resource.</span></span> <span data-ttu-id="0cccd-140">Modificateurs dans le. Fichier de script RC assignez ces attributs à la ressource.</span><span class="sxs-lookup"><span data-stu-id="0cccd-140">Modifiers in the .RC script file assign these attributes to the resource.</span></span> <span data-ttu-id="0cccd-141">Les identificateurs de script peuvent assigner les valeurs d’indicateur suivantes.</span><span class="sxs-lookup"><span data-stu-id="0cccd-141">The script identifiers can assign the following flag values.</span></span>

<span data-ttu-id="0cccd-142">Les applications n’utilisent pas ces attributs.</span><span class="sxs-lookup"><span data-stu-id="0cccd-142">Applications do not use any of these attributes.</span></span> <span data-ttu-id="0cccd-143">Les attributs sont autorisés dans le script à des fins de compatibilité descendante avec les scripts existants, mais ils sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="0cccd-143">The attributes are permitted in the script for backward compatibility with existing scripts, but they are ignored.</span></span> <span data-ttu-id="0cccd-144">Les ressources sont chargées lorsque le module correspondant est chargé, et sont libérées quand le module est déchargé.</span><span class="sxs-lookup"><span data-stu-id="0cccd-144">Resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

<span data-ttu-id="0cccd-145">**Moveable** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="0cccd-145">**MOVEABLE** (0x0010)</span></span>


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

<span data-ttu-id="0cccd-146">**corrigé** (~ déplaçable)</span><span class="sxs-lookup"><span data-stu-id="0cccd-146">**FIXED** (~MOVEABLE)</span></span>


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

<span data-ttu-id="0cccd-147">**Pur** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="0cccd-147">**PURE** (0x0020)</span></span>


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

<span data-ttu-id="0cccd-148">**IMpures** (~ pure)</span><span class="sxs-lookup"><span data-stu-id="0cccd-148">**IMPURE** (~PURE)</span></span>


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

<span data-ttu-id="0cccd-149">**Préchargement** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="0cccd-149">**PRELOAD** (0x0040)</span></span>


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

<span data-ttu-id="0cccd-150">**LOADONCALL** (~ préchargement)</span><span class="sxs-lookup"><span data-stu-id="0cccd-150">**LOADONCALL** (~PRELOAD)</span></span>


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

<span data-ttu-id="0cccd-151">À **Ignorer** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="0cccd-151">**DISCARDABLE** (0x1000)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="0cccd-152">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="0cccd-152">**LanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="0cccd-153">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="0cccd-153">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0cccd-154">Langue de la ressource ou de l’ensemble de ressources.</span><span class="sxs-lookup"><span data-stu-id="0cccd-154">The language for the resource or set of resources.</span></span> <span data-ttu-id="0cccd-155">Définissez la valeur de ce membre avec l’instruction facultative de définition de ressource de [langage](./language-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="0cccd-155">Set the value for this member with the optional [LANGUAGE](./language-statement.md) resource definition statement.</span></span> <span data-ttu-id="0cccd-156">Les paramètres sont des constantes du fichier Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="0cccd-156">The parameters are constants from the Winnt.h file.</span></span>

<span data-ttu-id="0cccd-157">Chaque ressource contient un identificateur de langue afin que le système ou l’application puisse sélectionner une langue adaptée aux paramètres régionaux actuels du système.</span><span class="sxs-lookup"><span data-stu-id="0cccd-157">Each resource includes a language identifier so the system or application can select a language appropriate for the current locale of the system.</span></span> <span data-ttu-id="0cccd-158">S’il existe plusieurs ressources du même type et du même nom qui diffèrent uniquement par la langue des chaînes dans les ressources, vous devez spécifier un **LanguageID** pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="0cccd-158">If there are multiple resources of the same type and name that differ only in the language of the strings within the resources, you will need to specify a **LanguageId** for each one.</span></span>

</dd> <dt>

<span data-ttu-id="0cccd-159">**Version**</span><span class="sxs-lookup"><span data-stu-id="0cccd-159">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="0cccd-160">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cccd-160">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0cccd-161">Numéro de version défini par l’utilisateur pour les données de ressources que les outils peuvent utiliser pour lire et écrire des fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="0cccd-161">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span> <span data-ttu-id="0cccd-162">Définissez cette valeur avec l’instruction facultative de définition de ressource de [version](./version-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="0cccd-162">Set this value with the optional [VERSION](./version-statement.md) resource definition statement.</span></span>

</dd> <dt>

<span data-ttu-id="0cccd-163">**Caractéristiques**</span><span class="sxs-lookup"><span data-stu-id="0cccd-163">**Characteristics**</span></span>
</dt> <dd>

<span data-ttu-id="0cccd-164">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cccd-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0cccd-165">Spécifie des informations définies par l’utilisateur sur la ressource que les outils peuvent utiliser pour lire et écrire des fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="0cccd-165">Specifies user-defined information about the resource that tools can use to read and write resource files.</span></span> <span data-ttu-id="0cccd-166">Définissez cette valeur avec les [caractéristiques](./characteristics-statement.md) facultatives de l’instruction de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="0cccd-166">Set this value with the optional [CHARACTERISTICS](./characteristics-statement.md) resource definition statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cccd-167">Notes</span><span class="sxs-lookup"><span data-stu-id="0cccd-167">Remarks</span></span>

<span data-ttu-id="0cccd-168">Un membre de type variable est appelé « **nom** » ou « membre **ordinal** », et il est utilisé à la plupart des emplacements dans le fichier de ressources où un identificateur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0cccd-168">A variable type member is called a **Name** or **Ordinal** member, and it is used in most places in the resource file where an identifier appears.</span></span> <span data-ttu-id="0cccd-169">Le premier **mot** d’un membre de type **nom** ou **ordinal** indique si le membre est une valeur numérique ou une chaîne.</span><span class="sxs-lookup"><span data-stu-id="0cccd-169">The first **WORD** of a **Name** or **Ordinal** type member indicates whether the member is a numeric value or a string.</span></span> <span data-ttu-id="0cccd-170">Si le premier **mot** du membre est égal à la valeur 0xFFFF, qui est un caractère Unicode non valide, le **mot** suivant est un numéro de type.</span><span class="sxs-lookup"><span data-stu-id="0cccd-170">If the first **WORD** in the member is equal to the value 0xffff, which is an invalid Unicode character, then the following **WORD** is a type number.</span></span> <span data-ttu-id="0cccd-171">Dans le cas contraire, le membre contient une chaîne Unicode et le premier **mot** du membre est le premier caractère de la chaîne de nom.</span><span class="sxs-lookup"><span data-stu-id="0cccd-171">Otherwise, the member contains a Unicode string and the first **WORD** in the member is the first character in the name string.</span></span> <span data-ttu-id="0cccd-172">Pour plus d’informations sur les instructions de définition de ressource, consultez [instructions de définition de ressource](./resource-definition-statements.md).</span><span class="sxs-lookup"><span data-stu-id="0cccd-172">For additional information about resource definition statements, see [Resource-Definition Statements](./resource-definition-statements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cccd-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cccd-173">Requirements</span></span>



| <span data-ttu-id="0cccd-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cccd-174">Requirement</span></span> | <span data-ttu-id="0cccd-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cccd-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0cccd-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cccd-176">Minimum supported client</span></span><br/> | <span data-ttu-id="0cccd-177">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cccd-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0cccd-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cccd-178">Minimum supported server</span></span><br/> | <span data-ttu-id="0cccd-179">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cccd-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0cccd-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cccd-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="0cccd-181">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="0cccd-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0cccd-182">Ressources</span><span class="sxs-lookup"><span data-stu-id="0cccd-182">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="0cccd-183">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="0cccd-183">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0cccd-184">Instruction de caractéristiques</span><span class="sxs-lookup"><span data-stu-id="0cccd-184">CHARACTERISTICS Statement</span></span>](./characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="0cccd-185">LANGUAGE (instruction)</span><span class="sxs-lookup"><span data-stu-id="0cccd-185">LANGUAGE Statement</span></span>](./language-statement.md)
</dt> <dt>

[<span data-ttu-id="0cccd-186">VERSION (instruction)</span><span class="sxs-lookup"><span data-stu-id="0cccd-186">VERSION Statement</span></span>](./version-statement.md)
</dt> </dl>

 

