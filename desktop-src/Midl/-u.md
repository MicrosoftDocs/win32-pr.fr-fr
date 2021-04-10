---
title: Commutateur/u
description: Le commutateur/U supprime toute définition précédente d’un nom en transmettant le nom au préprocesseur C comme s’il s’agissait d’une directive \ Undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- MIDL du commutateur/u
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100925"
---
# <a name="u-switch"></a><span data-ttu-id="cfcae-104">Commutateur/u</span><span class="sxs-lookup"><span data-stu-id="cfcae-104">/U switch</span></span>

<span data-ttu-id="cfcae-105">Le commutateur **/u** supprime toute définition précédente d’un nom en passant le nom au préprocesseur C comme s’il s’agissait d’une directive **\# non définie** .</span><span class="sxs-lookup"><span data-stu-id="cfcae-105">The **/U** switch removes any previous definition of a name by passing the name to the C preprocessor as if by a **\#undefine** directive.</span></span>

``` syntax
midl /U name
```

## <a name="switch-options"></a><span data-ttu-id="cfcae-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="cfcae-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="cfcae-107">*name*</span><span class="sxs-lookup"><span data-stu-id="cfcae-107">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="cfcae-108">Spécifie un nom défini à passer au préprocesseur C comme s’il s’agissait d’une directive **\# non définie** .</span><span class="sxs-lookup"><span data-stu-id="cfcae-108">Specifies a defined name to be passed to the C preprocessor as if by a **\#undefine** directive.</span></span> <span data-ttu-id="cfcae-109">Le nom est prédéfini par le préprocesseur C ou précédemment défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cfcae-109">The name is predefined by the C preprocessor or previously defined by the user.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cfcae-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cfcae-110">Remarks</span></span>

<span data-ttu-id="cfcae-111">Plusieurs directives **/u** peuvent être utilisées dans une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="cfcae-111">Multiple **/U** directives can be used in a command line.</span></span> <span data-ttu-id="cfcae-112">L’espace blanc entre le commutateur **/u** et le nom non défini est facultatif.</span><span class="sxs-lookup"><span data-stu-id="cfcae-112">White space between the **/U** switch and the undefined name is optional.</span></span>

<span data-ttu-id="cfcae-113">Lorsque le [**commutateur \_ /CPP cmd**](-cpp-cmd.md) est présent et que le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas, le compilateur MIDL concatène la chaîne spécifiée par le \_ commutateur/CPP cmd avec les options [**/i**](-i.md), [**/d**](-d.md)et **/U** et utilise cette chaîne concaténée pour appeler le préprocesseur C pour chaque fichier source IDL et ACF.</span><span class="sxs-lookup"><span data-stu-id="cfcae-113">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the /cpp\_cmd switch with the [**/I**](-i.md), [**/D**](-d.md), and **/U** options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="cfcae-114">Le commutateur du compilateur MIDL **/u** est ignoré lorsque le commutateur du compilateur MIDL **/non \_ CPP** ou **/CPP \_ OPT** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="cfcae-114">The MIDL compiler switch **/U** is ignored when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="cfcae-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="cfcae-115">Examples</span></span>

<span data-ttu-id="cfcae-116">**MIDL/UUNICODE NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="cfcae-116">**midl /UUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="cfcae-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfcae-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfcae-118">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="cfcae-118">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="cfcae-119">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="cfcae-119">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="cfcae-120">**/CPP \_ opt**</span><span class="sxs-lookup"><span data-stu-id="cfcae-120">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="cfcae-121">**/D**</span><span class="sxs-lookup"><span data-stu-id="cfcae-121">**/D**</span></span>](-d.md)
</dt> <dt>

[<span data-ttu-id="cfcae-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="cfcae-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="cfcae-123">**/non \_ CPP**</span><span class="sxs-lookup"><span data-stu-id="cfcae-123">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




