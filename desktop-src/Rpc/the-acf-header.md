---
title: En-tête ACF
description: L’en-tête ACF contient des attributs spécifiques à la plateforme qui s’appliquent à l’ensemble de l’interface. Les attributs appliqués aux types et aux fonctions individuels dans le corps ACF remplacent les attributs dans l’en-tête ACF. Aucun attribut n’est requis dans l’en-tête ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031519"
---
# <a name="the-acf-header"></a><span data-ttu-id="1199a-105">En-tête ACF</span><span class="sxs-lookup"><span data-stu-id="1199a-105">The ACF Header</span></span>

<span data-ttu-id="1199a-106">L’en-tête ACF contient des attributs spécifiques à la plateforme qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="1199a-106">The ACF header contains platform-specific attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="1199a-107">Les attributs appliqués aux types et aux fonctions individuels dans le corps ACF remplacent les attributs dans l’en-tête ACF.</span><span class="sxs-lookup"><span data-stu-id="1199a-107">Attributes applied to individual types and functions in the ACF body override the attributes in the ACF header.</span></span> <span data-ttu-id="1199a-108">Aucun attribut n’est requis dans l’en-tête ACF.</span><span class="sxs-lookup"><span data-stu-id="1199a-108">No attributes are required in the ACF header.</span></span>

<span data-ttu-id="1199a-109">L’en-tête ACF peut inclure l’un des attributs suivants : **\[** [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**\_ handle implicite**](/windows/desktop/Midl/implicit-handle) **\]** ou [**\_ handle explicite**](/windows/desktop/Midl/explicit-handle) **\]** .</span><span class="sxs-lookup"><span data-stu-id="1199a-109">The ACF header can include one of the following attributes: **\[**[**auto\_handle**](/windows/desktop/Midl/auto-handle)**\]**, **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]**, or [**explicit\_handle**](/windows/desktop/Midl/explicit-handle)**\]**.</span></span> <span data-ttu-id="1199a-110">Si le **\[ \_ handle \] automatique** ou le **\[ \_ \] handle implicite** est utilisé, il spécifie le type de handle de liaison qui sera utilisé pour la liaison lorsqu’une fonction distante n’a pas de paramètre de handle de liaison explicite.</span><span class="sxs-lookup"><span data-stu-id="1199a-110">If **\[auto\_handle\]** or **\[implicit\_handle\]** is used, it specifies the type of binding handle that will be used for binding when a remote function does not have an explicit binding-handle parameter.</span></span> <span data-ttu-id="1199a-111">Lorsque le ACF n’est pas présent ou qu’il ne spécifie pas un handle de liaison automatique, implicite ou explicite, MIDL utilise le **\[ \_ handle \] automatique** pour la liaison implicite.</span><span class="sxs-lookup"><span data-stu-id="1199a-111">When the ACF is not present or does not specify an automatic, implicit, or explicit binding handle, MIDL uses **\[auto\_handle\]** for implicit binding.</span></span>

<span data-ttu-id="1199a-112">Le **\[** [**code**](/windows/desktop/Midl/code) **\]** ou le **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** peut apparaître dans l’en-tête de l’interface, mais celui que vous choisissez ne peut apparaître qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="1199a-112">Either **\[**[**code**](/windows/desktop/Midl/code)**\]** or **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]** can appear in the interface header, but the one you choose can appear only once.</span></span> <span data-ttu-id="1199a-113">Quand aucun attribut n’est présent, le compilateur utilise le **\[ code \]** comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="1199a-113">When neither attribute is present, the compiler uses **\[code\]** as a default.</span></span>

<span data-ttu-id="1199a-114">Pour plus d’informations, consultez la rubrique [attributs ACF](/windows/desktop/Midl/acf-attributes).</span><span class="sxs-lookup"><span data-stu-id="1199a-114">For more information, see [ACF Attributes](/windows/desktop/Midl/acf-attributes).</span></span>

 

 