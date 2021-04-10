---
title: Chaînes de format de procédure
description: Voici une description complète de la chaîne de format. Il rassemble toutes les couches liées aux différentes étapes de l’évolution de l’interpréteur.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941226"
---
# <a name="procedure-format-strings"></a><span data-ttu-id="5c216-104">Chaînes de format de procédure</span><span class="sxs-lookup"><span data-stu-id="5c216-104">Procedure Format Strings</span></span>

<span data-ttu-id="5c216-105">Voici une description complète de la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="5c216-105">The following is a complete format string description.</span></span> <span data-ttu-id="5c216-106">Il rassemble toutes les couches liées aux différentes étapes de l’évolution de l’interpréteur.</span><span class="sxs-lookup"><span data-stu-id="5c216-106">It assembles all layers related to different stages of the interpreter evolution.</span></span>

## <a name="procedure-descriptor-overview"></a><span data-ttu-id="5c216-107">Vue d’ensemble du descripteur de procédure</span><span class="sxs-lookup"><span data-stu-id="5c216-107">Procedure Descriptor Overview</span></span>

<span data-ttu-id="5c216-108">Un descripteur de procédure se compose des descripteurs d’en-tête et des descripteurs de paramètre.</span><span class="sxs-lookup"><span data-stu-id="5c216-108">A procedure descriptor consists of the header descriptors and the parameter descriptors.</span></span> <span data-ttu-id="5c216-109">La description du style [**– OI**](/windows/desktop/Midl/-oi) est considérée comme obsolète, en termes d’utilisation courante dans la programmation RPC actuelle.</span><span class="sxs-lookup"><span data-stu-id="5c216-109">The [**–Oi**](/windows/desktop/Midl/-oi) style description is considered outdated, in terms of common usage in current RPC programming.</span></span> <span data-ttu-id="5c216-110">Le **– les interfaces** de prise en compte sont considérées comme plus actuelles.</span><span class="sxs-lookup"><span data-stu-id="5c216-110">The **–Oif** is considered more current.</span></span>

## <a name="the-oi-style-description"></a><span data-ttu-id="5c216-111">Description du style – OI</span><span class="sxs-lookup"><span data-stu-id="5c216-111">The –Oi Style Description</span></span>

<span data-ttu-id="5c216-112">Cette description est constituée des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5c216-112">This description consists of the following:</span></span>

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

<span data-ttu-id="5c216-113">L’en-tête doit être compris entre 6 et 16 octets.</span><span class="sxs-lookup"><span data-stu-id="5c216-113">The header would have from 6 to 16 bytes.</span></span>

<span data-ttu-id="5c216-114">La description complète est générée lors de la compilation en mode [**– OI**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="5c216-114">The complete description is generated when compiling in [**–Oi**](/windows/desktop/Midl/-oi) mode.</span></span> <span data-ttu-id="5c216-115">Dans [**– mode système d’exploitation**](/windows/desktop/Midl/-os) , seuls les descripteurs de paramètre sont générés, qui sont utilisés pour la conversion.</span><span class="sxs-lookup"><span data-stu-id="5c216-115">In [**–Os**](/windows/desktop/Midl/-os) mode, only the parameter descriptors are generated, which are used for conversion.</span></span> <span data-ttu-id="5c216-116">L’interpréteur de sélection utilise les descripteurs de paramètre de style anciens.</span><span class="sxs-lookup"><span data-stu-id="5c216-116">The pickling interpreter uses old style parameter descriptors.</span></span>

## <a name="the-oif-style-description"></a><span data-ttu-id="5c216-117">Description du style de-type d’interfaces</span><span class="sxs-lookup"><span data-stu-id="5c216-117">The –Oif Style Description</span></span>

<span data-ttu-id="5c216-118">La description est constituée des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5c216-118">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

<span data-ttu-id="5c216-119">Le descripteur d' [**en-tête**](/windows/desktop/Midl/-oi) de style</span><span class="sxs-lookup"><span data-stu-id="5c216-119">The [**–Oif**](/windows/desktop/Midl/-oi) style header descriptor consists of</span></span>

<span data-ttu-id="5c216-120">La description du style – de l’interfaces de génération est générée lors de la compilation dans le mode [**–**](/windows/desktop/Midl/-oi) **Oicf ou –** du compilateur.</span><span class="sxs-lookup"><span data-stu-id="5c216-120">The –Oif style description is generated when compiling in [**–Oif**](/windows/desktop/Midl/-oi) or **–Oicf** mode of the compiler.</span></span>

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

<span data-ttu-id="5c216-121">Certaines fonctionnalités plus récentes telles que pipe, Async et [**/Robust**](/windows/desktop/Midl/-robust) forcent le mode [**– Oicf**](/windows/desktop/Midl/-oi) du compilateur, lorsqu’ils sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="5c216-121">Some more recent features like pipe, async, and [**/robust**](/windows/desktop/Midl/-robust) force the [**–Oicf**](/windows/desktop/Midl/-oi) mode of the compiler, when used.</span></span>

## <a name="the-extended-oif-description"></a><span data-ttu-id="5c216-122">Description étendue – interfaces</span><span class="sxs-lookup"><span data-stu-id="5c216-122">The Extended –Oif Description</span></span>

<span data-ttu-id="5c216-123">La description est constituée des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5c216-123">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 