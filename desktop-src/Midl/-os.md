---
title: /OS (commutateur)
description: Le commutateur/OS spécifie la méthode en mode mixte pour marshaler le code stub passé entre le client et le serveur.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- MIDL du commutateur/OS
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509225"
---
# <a name="os-switch"></a><span data-ttu-id="1f76f-104">/OS (commutateur)</span><span class="sxs-lookup"><span data-stu-id="1f76f-104">/Os switch</span></span>

<span data-ttu-id="1f76f-105">Le commutateur **/OS** spécifie la méthode en mode mixte pour marshaler le code stub passé entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="1f76f-105">The **/Os** switch specifies the mixed-mode method to marshal stub code passed between client and server.</span></span>

``` syntax
midl /Os
```

## <a name="switch-options"></a><span data-ttu-id="1f76f-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="1f76f-106">Switch Options</span></span>

<span data-ttu-id="1f76f-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1f76f-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f76f-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1f76f-108">Remarks</span></span>

<span data-ttu-id="1f76f-109">Il y a des problèmes importants à prendre en compte avant de choisir la méthode de marshaling du code.</span><span class="sxs-lookup"><span data-stu-id="1f76f-109">There are important issues to consider before deciding on the method for marshaling code.</span></span> <span data-ttu-id="1f76f-110">Ces problèmes concernent la taille et les performances.</span><span class="sxs-lookup"><span data-stu-id="1f76f-110">These issues concern size and performance.</span></span> <span data-ttu-id="1f76f-111">Le compilateur MIDL fournit deux méthodes pour marshaler du code : mode mixte (**/OS**) et entièrement interprété ([**/OI**](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="1f76f-111">The MIDL compiler provides two methods for marshaling code: mixed-mode (**/Os**) and fully-interpreted ([**/Oi**](-oi.md)).</span></span> <span data-ttu-id="1f76f-112">La méthode entièrement interprétée marshale les données complètement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1f76f-112">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="1f76f-113">Cela réduit considérablement la taille du code stub, mais entraîne également une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="1f76f-113">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span>

<span data-ttu-id="1f76f-114">Utilisez le mode par défaut MIDL **/Oicf** /Robust pour tous les besoins autres que la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="1f76f-114">Use MIDL default mode **/Oicf** /robust for all purposes other than backward compatibility.</span></span> <span data-ttu-id="1f76f-115">Ce mode est le mode sécurisé standard du compilateur MIDL. n’importe quel autre mode doit être utilisé uniquement après mûre réflexion sur l’implication de sécurité, la réalisation de ces futures extensions sera uniquement implémentée pour le mode par défaut.</span><span class="sxs-lookup"><span data-stu-id="1f76f-115">This mode is the secure standard mode of MIDL compiler; any other mode should be used only after careful consideration to the security implication, realizing that future extensions will only be implemented for default mode.</span></span> <span data-ttu-id="1f76f-116">En mode mixte, le compilateur marshale certains paramètres inline dans les stubs générés.</span><span class="sxs-lookup"><span data-stu-id="1f76f-116">In mixed mode, the compiler marshals some parameters inline in the generated stubs.</span></span> <span data-ttu-id="1f76f-117">Bien que cela entraîne une plus grande taille de stub, elle peut également offrir des performances accrues.</span><span class="sxs-lookup"><span data-stu-id="1f76f-117">While this results in larger stub size, it also may offer increased performance.</span></span>

<span data-ttu-id="1f76f-118">MIDL offre une prise en charge complète des tableaux multidimensionnels et des pointeurs multidimensionnels uniquement en mode [**/Oicf**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="1f76f-118">MIDL provides full support for multidimensional arrays and multidimensional-sized pointers only in [**/Oicf**](-oi.md) mode.</span></span> <span data-ttu-id="1f76f-119">Dans les modes **/OS** et **/OI** , le compilateur prend en charge des cas simples, tels que des tableaux de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="1f76f-119">In **/Os** and **/Oi** modes, the compiler supports simple cases, such as fixed-size arrays.</span></span> <span data-ttu-id="1f76f-120">L’utilisation de tableaux multidimensionnels en mode **/OS** ou **/OI** peut entraîner des paramètres qui ne sont pas correctement marshalés.</span><span class="sxs-lookup"><span data-stu-id="1f76f-120">Using multidimensional arrays in **/Os** or **/Oi** modes can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="1f76f-121">Microsoft vous recommande d’utiliser le commutateur de ligne de commande **/Oicf** lorsque votre interface définit des paramètres qui sont des tableaux multidimensionnels ou des pointeurs de taille multidimensionnelle.</span><span class="sxs-lookup"><span data-stu-id="1f76f-121">Microsoft recommends that you use the **/Oicf** command line switch when your interface defines parameters that are multidimensional arrays or multidimensional-sized pointers.</span></span>

<span data-ttu-id="1f76f-122">Pour définir plus précisément le niveau de gradation dans le mode de marshaling des données, cette version de RPC fournit un \[ [](optimize.md) \] attribut optimize.</span><span class="sxs-lookup"><span data-stu-id="1f76f-122">To further define the level of gradation in how data is marshaled, this version of RPC provides an \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="1f76f-123">Cet attribut est utilisé comme attribut d’interface ou d’opération ACF pour sélectionner le mode de marshaling.</span><span class="sxs-lookup"><span data-stu-id="1f76f-123">This attribute is used as an ACF interface attribute or operation attribute to select the marshaling mode.</span></span>

## <a name="examples"></a><span data-ttu-id="1f76f-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="1f76f-124">Examples</span></span>

<span data-ttu-id="1f76f-125">**MIDL/OS nom du fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="1f76f-125">**midl /Os filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1f76f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f76f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f76f-127">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="1f76f-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1f76f-128">**/OI**</span><span class="sxs-lookup"><span data-stu-id="1f76f-128">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="1f76f-129">**requêtes**</span><span class="sxs-lookup"><span data-stu-id="1f76f-129">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="1f76f-130">**/non \_ format \_ opt**</span><span class="sxs-lookup"><span data-stu-id="1f76f-130">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 




