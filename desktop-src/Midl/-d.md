---
title: Commutateur/d
description: Le commutateur/D définit un nom et une valeur facultative à passer au préprocesseur C comme s’il s’agissait d’une directive \ define. Plusieurs directives/D peuvent être utilisées dans une ligne de commande.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- MIDL du commutateur/d
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100972"
---
# <a name="d-switch"></a><span data-ttu-id="1497a-105">Commutateur/d</span><span class="sxs-lookup"><span data-stu-id="1497a-105">/D switch</span></span>

<span data-ttu-id="1497a-106">Le commutateur **/d** définit un nom et une valeur facultative à passer au préprocesseur C comme s’il s’agissait d’une directive de **\# définition** .</span><span class="sxs-lookup"><span data-stu-id="1497a-106">The **/D** switch defines a name and an optional value to be passed to the C preprocessor as if by a **\#define** directive.</span></span> <span data-ttu-id="1497a-107">Plusieurs directives **/d** peuvent être utilisées dans une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="1497a-107">Multiple **/D** directives can be used in a command line.</span></span>

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a><span data-ttu-id="1497a-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="1497a-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="1497a-109">*name*</span><span class="sxs-lookup"><span data-stu-id="1497a-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="1497a-110">Spécifie un nom défini qui est passé au préprocesseur C lorsque le commutateur [**/CPP \_ cmd**](-cpp-cmd.md) est présent et que le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="1497a-110">Specifies a defined name that is passed to the C preprocessor when the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not present.</span></span>

</dd> <dt>

<span data-ttu-id="1497a-111">*définition*</span><span class="sxs-lookup"><span data-stu-id="1497a-111">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="1497a-112">Spécifie une valeur associée au nom défini.</span><span class="sxs-lookup"><span data-stu-id="1497a-112">Specifies a value associated with the defined name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1497a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1497a-113">Remarks</span></span>

<span data-ttu-id="1497a-114">L’espace blanc entre le commutateur **/d** et le nom défini est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1497a-114">White space between the **/D** switch and the defined name is optional.</span></span>

<span data-ttu-id="1497a-115">Lorsque le [**commutateur \_ /CPP cmd**](-cpp-cmd.md) est présent et que le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas, le compilateur MIDL concatène la chaîne spécifiée par le commutateur **/CPP \_ cmd** avec les options [**/i**](-i.md), **/d** et [**/u**](-u.md) et utilise cette chaîne concaténée pour appeler le préprocesseur C pour chaque fichier source IDL et ACF.</span><span class="sxs-lookup"><span data-stu-id="1497a-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the [**/I**](-i.md), **/D**, and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span>

<span data-ttu-id="1497a-116">Le commutateur du compilateur MIDL **/d** est ignoré lorsque le commutateur du compilateur MIDL [/non \_ CPP](-no-cpp-nocpp.md) ou [**/CPP \_ OPT**](-cpp-opt.md) est spécifié.</span><span class="sxs-lookup"><span data-stu-id="1497a-116">The MIDL compiler switch **/D** is ignored when the MIDL compiler switch [/no\_cpp](-no-cpp-nocpp.md) or [**/cpp\_opt**](-cpp-opt.md) is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="1497a-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="1497a-117">Examples</span></span>

<span data-ttu-id="1497a-118">**MIDL-DUNICODE nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="1497a-118">**midl -DUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1497a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1497a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1497a-120">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="1497a-120">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="1497a-121">**/CPP \_ opt**</span><span class="sxs-lookup"><span data-stu-id="1497a-121">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="1497a-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="1497a-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="1497a-123">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="1497a-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1497a-124">**/non \_ CPP**</span><span class="sxs-lookup"><span data-stu-id="1497a-124">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="1497a-125">**/U.**</span><span class="sxs-lookup"><span data-stu-id="1497a-125">**/U**</span></span>](-u.md)
</dt> </dl>

 

 




