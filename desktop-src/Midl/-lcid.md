---
title: /LCID (commutateur)
description: L’option de compilateur de/LCID MIDL vous permet d’utiliser des caractères internationaux dans vos fichiers d’entrée, noms de fichiers et chemins d’accès aux répertoires.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /LCID, commutateur MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312949"
---
# <a name="lcid-switch"></a><span data-ttu-id="eac13-104">/LCID (commutateur)</span><span class="sxs-lookup"><span data-stu-id="eac13-104">/lcid switch</span></span>

<span data-ttu-id="eac13-105">L’option de compilateur de **/LCID** MIDL vous permet d’utiliser des caractères internationaux dans vos fichiers d’entrée, noms de fichiers et chemins d’accès aux répertoires.</span><span class="sxs-lookup"><span data-stu-id="eac13-105">The **/lcid** MIDL compiler option lets you use international characters in your input files, file names, and directory paths.</span></span>

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a><span data-ttu-id="eac13-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="eac13-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="eac13-107">*localeID*</span><span class="sxs-lookup"><span data-stu-id="eac13-107">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="eac13-108">Spécifie l’identificateur de paramètres régionaux 32 bits utilisé dans la prise en charge des langues nationales Windows.</span><span class="sxs-lookup"><span data-stu-id="eac13-108">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="eac13-109">L’identificateur de paramètres régionaux doit être spécifié au format décimal.</span><span class="sxs-lookup"><span data-stu-id="eac13-109">The locale identifier should be specified in decimal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eac13-110">Notes</span><span class="sxs-lookup"><span data-stu-id="eac13-110">Remarks</span></span>

<span data-ttu-id="eac13-111">Dans les fichiers d’entrée, vous pouvez utiliser des commentaires, des chaînes, des HelpStrings et des identificateurs localisés.</span><span class="sxs-lookup"><span data-stu-id="eac13-111">Within the input files, you can use localized comments, strings, helpstrings and identifiers.</span></span> <span data-ttu-id="eac13-112">En particulier, le commutateur **/LCID** offre une prise en charge complète des caractères DBCS, pour représenter des langues asiatiques telles que le japonais, le chinois et le coréen.</span><span class="sxs-lookup"><span data-stu-id="eac13-112">In particular, the **/lcid** switch provides full DBCS support, to represent Asian languages such as Japanese, Chinese, and Korean.</span></span>

> [!Note]  
> <span data-ttu-id="eac13-113">Le commutateur **/LCID** est disponible avec la version 3.01.75 et ultérieure de MIDL.</span><span class="sxs-lookup"><span data-stu-id="eac13-113">The **/lcid** switch is available with MIDL version 3.01.75 and later.</span></span>

 

## <a name="examples"></a><span data-ttu-id="eac13-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="eac13-114">Examples</span></span>

<span data-ttu-id="eac13-115">**MIDL/LCID 1041 iface. idl**</span><span class="sxs-lookup"><span data-stu-id="eac13-115">**midl /lcid 1041 iface.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="eac13-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eac13-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac13-117">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="eac13-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="eac13-118">**LCID**</span><span class="sxs-lookup"><span data-stu-id="eac13-118">**lcid**</span></span>](lcid.md)
</dt> </dl>

 

 




