---
title: commutateur/ACF
description: Le commutateur/ACF permet à l’utilisateur de fournir un nom de fichier ACF explicite. Le commutateur autorise également l’utilisation de différents noms d’interface dans les fichiers IDL et ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- MIDL du commutateur/ACF
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940489"
---
# <a name="acf-switch"></a><span data-ttu-id="74da9-105">commutateur/ACF</span><span class="sxs-lookup"><span data-stu-id="74da9-105">/acf switch</span></span>

<span data-ttu-id="74da9-106">Le commutateur **/ACF** permet à l’utilisateur de fournir un nom de fichier ACF explicite.</span><span class="sxs-lookup"><span data-stu-id="74da9-106">The **/acf** switch allows the user to supply an explicit ACF file name.</span></span> <span data-ttu-id="74da9-107">Le commutateur autorise également l’utilisation de différents noms d’interface dans les fichiers IDL et ACF.</span><span class="sxs-lookup"><span data-stu-id="74da9-107">The switch also allows the use of different interface names in the IDL and ACF files.</span></span>

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a><span data-ttu-id="74da9-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="74da9-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="74da9-109">*\_nom de fichier ACF*</span><span class="sxs-lookup"><span data-stu-id="74da9-109">*acf\_filename*</span></span> 
</dt> <dd>

<span data-ttu-id="74da9-110">Spécifie le nom du CCP.</span><span class="sxs-lookup"><span data-stu-id="74da9-110">Specifies the name of the ACF.</span></span> <span data-ttu-id="74da9-111">Un espace blanc peut ou non être présent entre le commutateur **/ACF** et le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="74da9-111">White space may or may not be present between the **/acf** switch and the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74da9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="74da9-112">Remarks</span></span>

<span data-ttu-id="74da9-113">Par défaut, le compilateur MIDL construit le nom du CCP en remplaçant l’extension de nom de fichier IDL (généralement. idl) par. ACF.</span><span class="sxs-lookup"><span data-stu-id="74da9-113">By default, the MIDL compiler constructs the name of the ACF by replacing the IDL file name extension (usually .idl) with .acf.</span></span> <span data-ttu-id="74da9-114">Quand le commutateur **/ACF** est présent, le CCP prend son nom à partir du nom de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="74da9-114">When the **/acf** switch is present, the ACF takes its name from the specified file name.</span></span> <span data-ttu-id="74da9-115">Le commutateur **/ACF** s’applique uniquement au fichier IDL spécifié sur la ligne de commande du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="74da9-115">The **/acf** switch applies only to the IDL file specified on the MIDL compiler command line.</span></span> <span data-ttu-id="74da9-116">Elle ne s’applique pas aux fichiers importés.</span><span class="sxs-lookup"><span data-stu-id="74da9-116">It does not apply to imported files.</span></span>

<span data-ttu-id="74da9-117">Lorsque le commutateur **/ACF** est utilisé, le nom d’interface dans le ACF n’a pas besoin d’être identique au nom de l’interface MIDL.</span><span class="sxs-lookup"><span data-stu-id="74da9-117">When the **/acf** switch is used, the interface name in the ACF need not match the MIDL interface name.</span></span> <span data-ttu-id="74da9-118">Cette fonctionnalité permet aux interfaces de partager une spécification ACF.</span><span class="sxs-lookup"><span data-stu-id="74da9-118">This feature allows interfaces to share an ACF specification.</span></span>

<span data-ttu-id="74da9-119">Lorsqu’un chemin d’accès absolu à un ACF n’est pas spécifié, le compilateur MIDL recherche dans le répertoire actif, les répertoires fournis par l’option [**/i**](-i.md) et les répertoires dans le chemin d’accès include.</span><span class="sxs-lookup"><span data-stu-id="74da9-119">When an absolute path to an ACF is not specified, the MIDL compiler searches in the current directory, directories supplied by the [**/I**](-i.md) option, and directories in the INCLUDE path.</span></span>

<span data-ttu-id="74da9-120">Si le ACF est introuvable, le compilateur MIDL suppose qu’il n’existe aucun CCP pour cette interface.</span><span class="sxs-lookup"><span data-stu-id="74da9-120">If the ACF is not found, the MIDL compiler assumes there is no ACF for this interface.</span></span> <span data-ttu-id="74da9-121">Pour plus d’informations sur la séquence de répertoires, consultez les entrées de référence pour les commutateurs [**/i**](-i.md) et [**/non \_ Def \_ idir**](-no-def-idir.md) .</span><span class="sxs-lookup"><span data-stu-id="74da9-121">For more information about the sequence of directories, see the reference entries for the [**/I**](-i.md) and [**/no\_def\_idir**](-no-def-idir.md) switches.</span></span> <span data-ttu-id="74da9-122">Pour plus d’informations sur **/ACF**, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="74da9-122">For more information relating to **/acf**, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="74da9-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="74da9-123">Examples</span></span>

<span data-ttu-id="74da9-124">**MIDL/ACF. ACF nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="74da9-124">**midl /acf bar.acf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="74da9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74da9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74da9-126">**/I**</span><span class="sxs-lookup"><span data-stu-id="74da9-126">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="74da9-127">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="74da9-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="74da9-128">**/non \_ Def \_ idir**</span><span class="sxs-lookup"><span data-stu-id="74da9-128">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




