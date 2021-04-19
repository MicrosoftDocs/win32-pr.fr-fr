---
title: Référence de Command-Line MIDL
description: Cette section contient des informations de référence pour chaque commutateur de ligne de commande et option de commutateur reconnue par le compilateur Microsoft RPC MIDL.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Microsoft Interface Definition Language MIDL, référence
- Référence de ligne de commande MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514262"
---
# <a name="midl-command-line-reference"></a><span data-ttu-id="38fb5-105">Référence de Command-Line MIDL</span><span class="sxs-lookup"><span data-stu-id="38fb5-105">MIDL Command-Line Reference</span></span>

<span data-ttu-id="38fb5-106">Cette section contient des informations de référence pour chaque commutateur de ligne de commande et option de commutateur reconnue par le compilateur Microsoft RPC MIDL.</span><span class="sxs-lookup"><span data-stu-id="38fb5-106">This section contains reference information for each command-line switch and switch option recognized by the Microsoft RPC MIDL compiler.</span></span> <span data-ttu-id="38fb5-107">Les entrées de commutateur sont organisées par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="38fb5-107">Switch entries are arranged in alphabetical order.</span></span> <span data-ttu-id="38fb5-108">La [syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md) décrit la syntaxe générale de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="38fb5-108">[General MIDL Command-line Syntax](general-midl-command-line-syntax.md) describes the general command-line syntax.</span></span>

<dl>

[<span data-ttu-id="38fb5-109">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="38fb5-109">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)  
[<span data-ttu-id="38fb5-110">Commande fichier réponse</span><span class="sxs-lookup"><span data-stu-id="38fb5-110">The Response File Command</span></span>](the-response-file-command.md)  
[<span data-ttu-id="38fb5-111">**/acf**</span><span class="sxs-lookup"><span data-stu-id="38fb5-111">**/acf**</span></span>](-acf.md)  
[<span data-ttu-id="38fb5-112">**/align**</span><span class="sxs-lookup"><span data-stu-id="38fb5-112">**/align**</span></span>](-align.md)  
[<span data-ttu-id="38fb5-113">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="38fb5-113">**/amd64**</span></span>](-amd64.md)  
[<span data-ttu-id="38fb5-114">**configuration de/App \_**</span><span class="sxs-lookup"><span data-stu-id="38fb5-114">**/app\_config**</span></span>](-app-config.md)  
[<span data-ttu-id="38fb5-115">\_compatibilité/Backward</span><span class="sxs-lookup"><span data-stu-id="38fb5-115">/backward\_compat</span></span>](-backward-compat.md)  
[<span data-ttu-id="38fb5-116">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="38fb5-116">**/c\_ext**</span></span>](-c-ext.md)  
[<span data-ttu-id="38fb5-117">**/caux**</span><span class="sxs-lookup"><span data-stu-id="38fb5-117">**/caux**</span></span>](-caux.md)  
[<span data-ttu-id="38fb5-118">**/Char**</span><span class="sxs-lookup"><span data-stu-id="38fb5-118">**/char**</span></span>](-char.md)  
[<span data-ttu-id="38fb5-119">**/client**</span><span class="sxs-lookup"><span data-stu-id="38fb5-119">**/client**</span></span>](-client.md)  
[<span data-ttu-id="38fb5-120">**/confirm**</span><span class="sxs-lookup"><span data-stu-id="38fb5-120">**/confirm**</span></span>](-confirm.md)  
[<span data-ttu-id="38fb5-121">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="38fb5-121">**/cpp\_cmd**</span></span>](-cpp-cmd.md)  
[<span data-ttu-id="38fb5-122">**/CPP \_ opt**</span><span class="sxs-lookup"><span data-stu-id="38fb5-122">**/cpp\_opt**</span></span>](-cpp-opt.md)  
<span data-ttu-id="38fb5-123">[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)</span><span class="sxs-lookup"><span data-stu-id="38fb5-123">[**/cstruct_out**](-cstruct-out.md)
[**/cstub**](-cstub.md)</span></span>  
[<span data-ttu-id="38fb5-124">**/D**</span><span class="sxs-lookup"><span data-stu-id="38fb5-124">**/D**</span></span>](-d.md)  
[<span data-ttu-id="38fb5-125">**/dlldata**</span><span class="sxs-lookup"><span data-stu-id="38fb5-125">**/dlldata**</span></span>](-dlldata.md)  
[<span data-ttu-id="38fb5-126">**/env**</span><span class="sxs-lookup"><span data-stu-id="38fb5-126">**/env**</span></span>](-env.md)  
[<span data-ttu-id="38fb5-127">**/Error**</span><span class="sxs-lookup"><span data-stu-id="38fb5-127">**/error**</span></span>](-error.md)  
[<span data-ttu-id="38fb5-128">**/Error**</span><span class="sxs-lookup"><span data-stu-id="38fb5-128">**/error**</span></span>](-error.md)  
[<span data-ttu-id="38fb5-129">**/h**</span><span class="sxs-lookup"><span data-stu-id="38fb5-129">**/h**</span></span>](-h.md)  
[<span data-ttu-id="38fb5-130">**/Header**</span><span class="sxs-lookup"><span data-stu-id="38fb5-130">**/header**</span></span>](-header.md)  
[<span data-ttu-id="38fb5-131">**/Help (/ ?)**</span><span class="sxs-lookup"><span data-stu-id="38fb5-131">**/help (/?)**</span></span>](-help-.md)  
[<span data-ttu-id="38fb5-132">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="38fb5-132">**/ia64**</span></span>](-ia64.md)  
[<span data-ttu-id="38fb5-133">**/I**</span><span class="sxs-lookup"><span data-stu-id="38fb5-133">**/I**</span></span>](-i.md)  
[<span data-ttu-id="38fb5-134">**/IID**</span><span class="sxs-lookup"><span data-stu-id="38fb5-134">**/iid**</span></span>](-iid.md)  
[<span data-ttu-id="38fb5-135">**/Import**</span><span class="sxs-lookup"><span data-stu-id="38fb5-135">**/import**</span></span>](-import.md)  
[<span data-ttu-id="38fb5-136">**/LCID**</span><span class="sxs-lookup"><span data-stu-id="38fb5-136">**/lcid**</span></span>](-lcid.md)  
[<span data-ttu-id="38fb5-137">**/mktyplib203**</span><span class="sxs-lookup"><span data-stu-id="38fb5-137">**/mktyplib203**</span></span>](-mktyplib203.md)  
[<span data-ttu-id="38fb5-138">**/ms. \_ ext**</span><span class="sxs-lookup"><span data-stu-id="38fb5-138">**/ms\_ext**</span></span>](-ms-ext.md)  
[<span data-ttu-id="38fb5-139">**/ms. \_ Union**</span><span class="sxs-lookup"><span data-stu-id="38fb5-139">**/ms\_union**</span></span>](-ms-union.md)  
[<span data-ttu-id="38fb5-140">**/MSC \_ ver**</span><span class="sxs-lookup"><span data-stu-id="38fb5-140">**/msc\_ver**</span></span>](-msc-ver.md)  
[<span data-ttu-id="38fb5-141">**/New**</span><span class="sxs-lookup"><span data-stu-id="38fb5-141">**/new**</span></span>](-new.md)  
[<span data-ttu-id="38fb5-142">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="38fb5-142">**/newtlb**</span></span>](-newtlb.md)  
[<span data-ttu-id="38fb5-143">**/non \_ CPP,/nocpp**</span><span class="sxs-lookup"><span data-stu-id="38fb5-143">**/no\_cpp, /nocpp**</span></span>](-no-cpp-nocpp.md)  
[<span data-ttu-id="38fb5-144">**/non \_ par défaut \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="38fb5-144">**/no\_default\_epv**</span></span>](-no-default-epv.md)  
[<span data-ttu-id="38fb5-145">**/non \_ Def \_ idir**</span><span class="sxs-lookup"><span data-stu-id="38fb5-145">**/no\_def\_idir**</span></span>](-no-def-idir.md)  
[<span data-ttu-id="38fb5-146">**/non \_ format \_ opt**</span><span class="sxs-lookup"><span data-stu-id="38fb5-146">**/no\_format\_opt**</span></span>](-no-format-opt.md)  
[<span data-ttu-id="38fb5-147">**/non \_ robuste**</span><span class="sxs-lookup"><span data-stu-id="38fb5-147">**/no\_robust**</span></span>](-no-robust.md)  
[<span data-ttu-id="38fb5-148">**/non \_ Avertissement**</span><span class="sxs-lookup"><span data-stu-id="38fb5-148">**/no\_warn**</span></span>](-no-warn.md)  
[<span data-ttu-id="38fb5-149">**/nologo**</span><span class="sxs-lookup"><span data-stu-id="38fb5-149">**/nologo**</span></span>](-nologo.md)  
[<span data-ttu-id="38fb5-150">**/notlb**</span><span class="sxs-lookup"><span data-stu-id="38fb5-150">**/notlb**</span></span>](-notlb.md)  
[<span data-ttu-id="38fb5-151">**/o**</span><span class="sxs-lookup"><span data-stu-id="38fb5-151">**/o**</span></span>](-o.md)  
[<span data-ttu-id="38fb5-152">**/OI**</span><span class="sxs-lookup"><span data-stu-id="38fb5-152">**/Oi**</span></span>](-oi.md)  
[<span data-ttu-id="38fb5-153">**/Old**</span><span class="sxs-lookup"><span data-stu-id="38fb5-153">**/old**</span></span>](-old.md)  
[<span data-ttu-id="38fb5-154">**/oldtlb**</span><span class="sxs-lookup"><span data-stu-id="38fb5-154">**/oldtlb**</span></span>](-oldtlb.md)  
[<span data-ttu-id="38fb5-155">**/oldnames**</span><span class="sxs-lookup"><span data-stu-id="38fb5-155">**/oldnames**</span></span>](-oldnames.md)  
[<span data-ttu-id="38fb5-156">**/OS**</span><span class="sxs-lookup"><span data-stu-id="38fb5-156">**/Os**</span></span>](-os.md)  
[<span data-ttu-id="38fb5-157">**/osf**</span><span class="sxs-lookup"><span data-stu-id="38fb5-157">**/osf**</span></span>](-osf.md)  
[<span data-ttu-id="38fb5-158">**/out**</span><span class="sxs-lookup"><span data-stu-id="38fb5-158">**/out**</span></span>](-out.md)  
[<span data-ttu-id="38fb5-159">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="38fb5-159">**/pack**</span></span>](-pack.md)  
[<span data-ttu-id="38fb5-160">**/prefix**</span><span class="sxs-lookup"><span data-stu-id="38fb5-160">**/prefix**</span></span>](-prefix.md)  
[<span data-ttu-id="38fb5-161">**/Protocol**</span><span class="sxs-lookup"><span data-stu-id="38fb5-161">**/protocol**</span></span>](-protocol.md)  
[<span data-ttu-id="38fb5-162">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="38fb5-162">**/proxy**</span></span>](-proxy.md)  
[<span data-ttu-id="38fb5-163">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="38fb5-163">**/robust**</span></span>](-robust.md)  
[<span data-ttu-id="38fb5-164">**/rpcss**</span><span class="sxs-lookup"><span data-stu-id="38fb5-164">**/rpcss**</span></span>](-rpcss.md)  
[<span data-ttu-id="38fb5-165">**/sal**</span><span class="sxs-lookup"><span data-stu-id="38fb5-165">**/sal**</span></span>](-sal.md)  
[<span data-ttu-id="38fb5-166">**/SAL \_ local**</span><span class="sxs-lookup"><span data-stu-id="38fb5-166">**/sal\_local**</span></span>](-sal-local.md)  
[<span data-ttu-id="38fb5-167">**/saux**</span><span class="sxs-lookup"><span data-stu-id="38fb5-167">**/saux**</span></span>](-saux.md)  
[<span data-ttu-id="38fb5-168">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="38fb5-168">**/savePP**</span></span>](-savepp.md)  
[<span data-ttu-id="38fb5-169">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="38fb5-169">**/sstub**</span></span>](-sstub.md)  
[<span data-ttu-id="38fb5-170">**vérification de/Syntax \_**</span><span class="sxs-lookup"><span data-stu-id="38fb5-170">**/syntax\_check**</span></span>](-syntax-check.md)  
[**/<system>**](-system-.md)  
[<span data-ttu-id="38fb5-171">**/Target**</span><span class="sxs-lookup"><span data-stu-id="38fb5-171">**/target**</span></span>](-target.md)  
[<span data-ttu-id="38fb5-172">**/TLB**</span><span class="sxs-lookup"><span data-stu-id="38fb5-172">**/tlb**</span></span>](-tlb.md)  
[<span data-ttu-id="38fb5-173">**/U.**</span><span class="sxs-lookup"><span data-stu-id="38fb5-173">**/U**</span></span>](-u.md)  
[<span data-ttu-id="38fb5-174">**/Utilisez \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="38fb5-174">**/use\_epv**</span></span>](-use-epv.md)  
[<span data-ttu-id="38fb5-175">**\_horodatage/version**</span><span class="sxs-lookup"><span data-stu-id="38fb5-175">**/version\_stamp**</span></span>](-version-stamp.md)  
[<span data-ttu-id="38fb5-176">**/W**</span><span class="sxs-lookup"><span data-stu-id="38fb5-176">**/W**</span></span>](-w.md)  
[<span data-ttu-id="38fb5-177">**/WARN**</span><span class="sxs-lookup"><span data-stu-id="38fb5-177">**/warn**</span></span>](-warn.md)  
[<span data-ttu-id="38fb5-178">**/win32**</span><span class="sxs-lookup"><span data-stu-id="38fb5-178">**/win32**</span></span>](-win32.md)  
[<span data-ttu-id="38fb5-179">**/win64**</span><span class="sxs-lookup"><span data-stu-id="38fb5-179">**/win64**</span></span>](-win64.md)  
[<span data-ttu-id="38fb5-180">**/WX**</span><span class="sxs-lookup"><span data-stu-id="38fb5-180">**/WX**</span></span>](-wx.md)  
[<span data-ttu-id="38fb5-181">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="38fb5-181">**/Zp**</span></span>](-zp.md)  
[<span data-ttu-id="38fb5-182">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="38fb5-182">**/Zs**</span></span>](-zs.md)  
</dl>

<span data-ttu-id="38fb5-183">Le compilateur MIDL peut générer du code pour différentes plateformes et versions système.</span><span class="sxs-lookup"><span data-stu-id="38fb5-183">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="38fb5-184">Consultez le commutateur [**/target**](-target.md) pour en savoir plus sur les commutateurs suggérés et sur la façon de générer du code optimisé pour une version donnée.</span><span class="sxs-lookup"><span data-stu-id="38fb5-184">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a given release.</span></span>

<span data-ttu-id="38fb5-185">Notez que le signe moins (–) peut remplacer la barre oblique (/) dans tous les commutateurs de ligne de commande MIDL qui commencent par une barre oblique (/).</span><span class="sxs-lookup"><span data-stu-id="38fb5-185">Note that the minus sign (–) may be substituted for the slash (/) in all MIDL command-line switches that begin with a slash (/).</span></span> <span data-ttu-id="38fb5-186">L’exemple suivant illustre leur équivalence lors de l’appel du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="38fb5-186">The following example demonstrates their equivalence when invoking the MIDL compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="38fb5-187">Exemples</span><span class="sxs-lookup"><span data-stu-id="38fb5-187">Examples</span></span>

<span data-ttu-id="38fb5-188">**MIDL/ACF mon nom de fichier \_ ACF. ACF** \*\* \* *. idl*\*</span><span class="sxs-lookup"><span data-stu-id="38fb5-188">**midl /acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

<span data-ttu-id="38fb5-189">**MIDL-ACF My \_ ACF. ACF** *filename \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="38fb5-189">**midl -acf my\_acf.acf** *filename\*\*\*.idl*\*</span></span>

 

 




