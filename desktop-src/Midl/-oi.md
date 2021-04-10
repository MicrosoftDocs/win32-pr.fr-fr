---
title: /Oi (commutateur)
description: Les commutateurs/OI et/OIC indiquent au compilateur MIDL d’utiliser une méthode de marshaling entièrement interprétée. Le commutateur/Oicf fournit des améliorations de performances supplémentaires.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- Option de commutateur/OI
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104198883"
---
# <a name="oi-switch"></a><span data-ttu-id="df202-105">/Oi (commutateur)</span><span class="sxs-lookup"><span data-stu-id="df202-105">/Oi switch</span></span>

<span data-ttu-id="df202-106">Les commutateurs **/OI** et **/OIC** indiquent au compilateur MIDL d’utiliser une méthode de marshaling entièrement interprétée.</span><span class="sxs-lookup"><span data-stu-id="df202-106">The **/Oi** and **/Oic** switches direct the MIDL compiler to use a fully-interpreted marshaling method.</span></span> <span data-ttu-id="df202-107">Le commutateur **/Oicf** fournit des améliorations de performances supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="df202-107">The **/Oicf** switch provides additional performance enhancements.</span></span>

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a><span data-ttu-id="df202-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="df202-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="df202-109">*OI*</span><span class="sxs-lookup"><span data-stu-id="df202-109">*Oi*</span></span> 
</dt> <dd>

<span data-ttu-id="df202-110">Spécifie la méthode entièrement interprétée pour le marshaling du code stub passé entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="df202-110">Specifies the fully-interpreted method for marshaling stub code passed between client and server.</span></span>

> [!Note]  
> <span data-ttu-id="df202-111">Ce commutateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="df202-111">This switch is obsolete.</span></span> <span data-ttu-id="df202-112">Il est recommandé d’utiliser le commutateur **/Oicf** à la place.</span><span class="sxs-lookup"><span data-stu-id="df202-112">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="df202-113">*Oic*</span><span class="sxs-lookup"><span data-stu-id="df202-113">*Oic*</span></span> 
</dt> <dd>

<span data-ttu-id="df202-114">Spécifie la méthode de proxy non codée du marshaling qui fournit toutes les fonctionnalités de **/OI** et réduit également la taille du code stub client pour les interfaces d’objet.</span><span class="sxs-lookup"><span data-stu-id="df202-114">Specifies the codeless proxy method of marshaling that provides all the features of **/Oi** and also further reduces the size of the client stub code for object interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="df202-115">Ce commutateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="df202-115">This switch is obsolete.</span></span> <span data-ttu-id="df202-116">Il est recommandé d’utiliser le commutateur **/Oicf** à la place.</span><span class="sxs-lookup"><span data-stu-id="df202-116">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="df202-117">*Interfaces de Oicf*</span><span class="sxs-lookup"><span data-stu-id="df202-117">*Oif or Oicf*</span></span> 
</dt> <dd>

<span data-ttu-id="df202-118">Spécifie la méthode de proxy sans code du marshaling qui inclut toutes les fonctionnalités fournies par **/OI** et **/OIC** , mais utilise un nouvel interpréteur (chaînes de format rapide) qui offre de meilleures performances que **/OI** ou **/OIC**.</span><span class="sxs-lookup"><span data-stu-id="df202-118">Specifies the codeless proxy method of marshaling that includes all the features provided by **/Oi** and **/Oic** but uses a new interpreter (fast format strings) that provides better performance than **/Oi** or **/Oic**.</span></span> <span data-ttu-id="df202-119">Ce commutateur comprend des améliorations récentes de RPC et est recommandé pour les scénarios RPC modernes.</span><span class="sxs-lookup"><span data-stu-id="df202-119">This switch includes recent RPC enhancements and is recommended for modern RPC scenarios.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df202-120">Notes</span><span class="sxs-lookup"><span data-stu-id="df202-120">Remarks</span></span>

<span data-ttu-id="df202-121">Veuillez noter les restrictions liées aux plateformes de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df202-121">Please note the restrictions related to supporting platforms.</span></span>

<span data-ttu-id="df202-122">Le compilateur MIDL 3,0 fournit deux méthodes pour marshaler du code : entièrement interprété ( **/OI**, **/OIC** et **/Oicf**) et en mode mixte ( [**/OS**](-os.md)).</span><span class="sxs-lookup"><span data-stu-id="df202-122">The MIDL 3.0 compiler provides two methods for marshaling code: fully-interpreted ( **/Oi**, **/Oic** and **/Oicf**) and mixed-mode ( [**/Os**](-os.md)).</span></span> <span data-ttu-id="df202-123">À compter de la version 6.0.359 de MIDL, le compilateur MIDL génère des stubs **/Oicf** Â  [**/Robust**](-robust.md) par défaut.</span><span class="sxs-lookup"><span data-stu-id="df202-123">Starting with MIDL version 6.0.359, the MIDL compiler generates **/Oicf** Â  [**/robust**](-robust.md) stubs by default.</span></span> <span data-ttu-id="df202-124">Certaines fonctionnalités du langage ne sont pas prises en charge dans certains modes.</span><span class="sxs-lookup"><span data-stu-id="df202-124">Some language features are not supported in some modes.</span></span> <span data-ttu-id="df202-125">Dans ce cas, le compilateur bascule automatiquement vers le mode approprié et émet un avertissement.</span><span class="sxs-lookup"><span data-stu-id="df202-125">In this case, the compiler automatically switches to the appropriate mode and issues a warning.</span></span>

<span data-ttu-id="df202-126">Si les performances constituent un problème, la méthode en mode mixte ( [**/OS**](-os.md)) peut être la meilleure approche.</span><span class="sxs-lookup"><span data-stu-id="df202-126">If performance is a concern, the mixed-mode ( [**/Os**](-os.md)) method can be the best approach.</span></span> <span data-ttu-id="df202-127">Dans ce mode, le compilateur choisit de marshaler certains paramètres inline dans les stubs générés.</span><span class="sxs-lookup"><span data-stu-id="df202-127">In this mode, the compiler chooses to marshal some parameters inline in the generated stubs.</span></span> <span data-ttu-id="df202-128">Bien que cela entraîne une plus grande taille de stub, elle offre des performances accrues.</span><span class="sxs-lookup"><span data-stu-id="df202-128">While this results in larger stub size, it offers increased performance.</span></span>

<span data-ttu-id="df202-129">La méthode entièrement interprétée marshale les données complètement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="df202-129">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="df202-130">Cela réduit considérablement la taille du code stub, mais entraîne une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="df202-130">This considerably reduces the size of the stub code, but results in decreased performance.</span></span> <span data-ttu-id="df202-131">En outre, avec la méthode entièrement interprétée, il existe une limite de 16 paramètres pour chaque procédure.</span><span class="sxs-lookup"><span data-stu-id="df202-131">Also, with the fully-interpreted method, there is a limit of 16 parameters for each procedure.</span></span> <span data-ttu-id="df202-132">Toute procédure contenant plus de 16 paramètres sera automatiquement traitée en mode [**/OS**](-os.md) .</span><span class="sxs-lookup"><span data-stu-id="df202-132">Any procedure containing more than 16 parameters will automatically be processed in [**/Os**](-os.md) mode.</span></span> <span data-ttu-id="df202-133">Parmi les modes interprétés, **/Oicf** offre les meilleures performances et **/OI** offre la meilleure compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="df202-133">Among the interpreted modes, **/Oicf** offers the best performance and **/Oi** offers the best backward compatibility.</span></span>

<span data-ttu-id="df202-134">Vous pouvez utiliser l’option **/OIF** si votre application utilise des fonctionnalités MIDL qui ont été introduites avec MIDL 3,0, telles que les attributs du \[ [**\_ marshaleur de câble**](wire-marshal.md) et du \] \[ [**\_ Marshal d’utilisateur**](user-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="df202-134">You may want to use the **/Oif** option if your application uses MIDL features that were introduced with MIDL 3.0, such as the \[[**wire\_marshal**](wire-marshal.md)\] and \[[**user\_marshal**](user-marshal.md)\] attributes.</span></span> <span data-ttu-id="df202-135">Si votre application utilise des [canaux](/windows/desktop/Rpc/pipes) , vous devez utiliser l’option **/OIF** ; Si vous spécifiez un autre mode, le compilateur MIDL passe à **/OIF**.</span><span class="sxs-lookup"><span data-stu-id="df202-135">If your application uses [pipes](/windows/desktop/Rpc/pipes) you must use the **/Oif** option; if you specify another mode, the MIDL compiler will switch to **/Oif**.</span></span>

<span data-ttu-id="df202-136">Pour affiner la façon dont votre code stub est marshalé, Microsoft RPC fournit un attribut d' \[ [**optimisation**](optimize.md) ACF \] .</span><span class="sxs-lookup"><span data-stu-id="df202-136">To fine-tune the way your stub code is marshaled, Microsoft RPC provides an ACF \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="df202-137">Cet attribut est utilisé en tant qu’attribut d’interface ou d’opération pour sélectionner le mode de marshaling pour des interfaces individuelles ou pour des opérations individuelles.</span><span class="sxs-lookup"><span data-stu-id="df202-137">This attribute is used as an interface attribute or operation attribute to select the marshaling mode for individual interfaces or for individual operations.</span></span>

### <a name="calling-conventions"></a><span data-ttu-id="df202-138">Conventions d’appel</span><span class="sxs-lookup"><span data-stu-id="df202-138">Calling Conventions</span></span>

<span data-ttu-id="df202-139">Les stubs générés par le compilateur MIDL dans la méthode interprétée à l’aide des commutateurs **/OI**, **/OIC** ou **/OIF** doivent être compilés comme une procédure stdcall ou cdecl pendant la compilation C.</span><span class="sxs-lookup"><span data-stu-id="df202-139">Stubs generated by the MIDL compiler in the interpreted method using the **/Oi**, **/Oic**, or **/Oif** switches must be compiled as either a stdcall or a cdecl procedure during the C compilation.</span></span> <span data-ttu-id="df202-140">Une convention d’appel PASCAL ou fastcall ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="df202-140">A PASCAL or Fastcall calling convention will not work.</span></span> <span data-ttu-id="df202-141">En outre, le stub du serveur doit être compilé comme StdCall.</span><span class="sxs-lookup"><span data-stu-id="df202-141">Additionally, the server stub must be compiled as stdcall.</span></span>

## <a name="examples"></a><span data-ttu-id="df202-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="df202-142">Examples</span></span>

<span data-ttu-id="df202-143">**MIDL/OI nom de fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="df202-143">**midl /Oi filename.idl**</span></span>

<span data-ttu-id="df202-144">**MIDL/OIC NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="df202-144">**midl /Oic filename.idl**</span></span>

<span data-ttu-id="df202-145">**MIDL/OIF NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="df202-145">**midl /Oif filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="df202-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df202-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df202-147">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="df202-147">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="df202-148">**/non \_ robuste**</span><span class="sxs-lookup"><span data-stu-id="df202-148">**/no\_robust**</span></span>](-no-robust.md)
</dt> <dt>

[<span data-ttu-id="df202-149">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="df202-149">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="df202-150">**/OS**</span><span class="sxs-lookup"><span data-stu-id="df202-150">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="df202-151">**requêtes**</span><span class="sxs-lookup"><span data-stu-id="df202-151">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="df202-152">**/non \_ format \_ opt**</span><span class="sxs-lookup"><span data-stu-id="df202-152">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 