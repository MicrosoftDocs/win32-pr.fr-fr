---
title: commutateur/app_config
description: Le commutateur de configuration/App \_ sélectionne le mode de configuration de l’application, ce qui vous permet d’utiliser des mots clés ACF dans le fichier IDL. Avec ce commutateur MIDL du compilateur, vous pouvez omettre le ACF et spécifier une interface dans un fichier IDL unique.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /commutateur app_config MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380895"
---
# <a name="app_config-switch"></a><span data-ttu-id="2711e-105">\_commutateur de configuration/App</span><span class="sxs-lookup"><span data-stu-id="2711e-105">/app\_config switch</span></span>

<span data-ttu-id="2711e-106">Le **commutateur \_ de configuration/App** sélectionne le mode de configuration de l’application, ce qui vous permet d’utiliser des mots clés ACF dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="2711e-106">The **/app\_config** switch selects application-configuration mode, which allows you to use some ACF keywords in the IDL file.</span></span> <span data-ttu-id="2711e-107">Avec ce commutateur MIDL du compilateur, vous pouvez omettre le ACF et spécifier une interface dans un fichier IDL unique.</span><span class="sxs-lookup"><span data-stu-id="2711e-107">With this MIDL compiler switch, you can omit the ACF and specify an interface in a single IDL file.</span></span>

``` syntax
midl /app_config
```

## <a name="switch-options"></a><span data-ttu-id="2711e-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="2711e-108">Switch Options</span></span>

<span data-ttu-id="2711e-109">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2711e-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2711e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2711e-110">Remarks</span></span>

<span data-ttu-id="2711e-111">Microsoft RPC prend en charge l’utilisation des attributs ACF suivants dans le fichier IDL :</span><span class="sxs-lookup"><span data-stu-id="2711e-111">Microsoft RPC supports the use of the following ACF attributes in the IDL file:</span></span>

-   <span data-ttu-id="2711e-112">Handle implicite \_</span><span class="sxs-lookup"><span data-stu-id="2711e-112">Implicit\_handle</span></span>
-   <span data-ttu-id="2711e-113">\_Handle automatique</span><span class="sxs-lookup"><span data-stu-id="2711e-113">Auto\_handle</span></span>
-   <span data-ttu-id="2711e-114">\_Handle explicite</span><span class="sxs-lookup"><span data-stu-id="2711e-114">Explicit\_handle</span></span>

<span data-ttu-id="2711e-115">Les versions ultérieures de Microsoft RPC peuvent prendre en charge l’utilisation d’autres attributs ACF dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="2711e-115">Future releases of Microsoft RPC may support the use of other ACF attributes in the IDL file.</span></span> <span data-ttu-id="2711e-116">L’option de **\_ configuration/App** représente une extension Microsoft de la spécification OSF-DCE et, par conséquent, s’exclut mutuellement avec l’option [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="2711e-116">The **/app\_config** option represents a Microsoft extension to the OSF-DCE specification and, as such, is mutually exclusive with the [**/osf**](-osf.md) option.</span></span>

<span data-ttu-id="2711e-117">Pour plus d’informations sur le commutateur de configuration **/app \_** , consultez fichier de [configuration d’application (ACF)](application-configuration-file-acf-.md) et [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="2711e-117">For more information related to the **/app\_config** switch, see [Application Configuration File (ACF)](application-configuration-file-acf-.md) and [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2711e-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="2711e-118">Examples</span></span>

<span data-ttu-id="2711e-119">**\_nom du fichier. idl de la configuration MIDL/App**</span><span class="sxs-lookup"><span data-stu-id="2711e-119">**midl /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="2711e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2711e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2711e-121">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="2711e-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




