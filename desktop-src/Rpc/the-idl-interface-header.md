---
title: En-tête d’interface IDL
description: L’en-tête d’interface IDL spécifie des informations sur l’interface dans son ensemble. Contrairement à ACF, l’en-tête d’interface contient des attributs qui sont indépendants de la plateforme.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102281"
---
# <a name="the-idl-interface-header"></a><span data-ttu-id="8ddfa-104">En-tête d’interface IDL</span><span class="sxs-lookup"><span data-stu-id="8ddfa-104">The IDL Interface Header</span></span>

<span data-ttu-id="8ddfa-105">L’en-tête d’interface IDL spécifie des informations sur l’interface dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="8ddfa-105">The IDL interface header specifies information about the interface as a whole.</span></span> <span data-ttu-id="8ddfa-106">Contrairement à ACF, l’en-tête d’interface contient des attributs qui sont indépendants de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="8ddfa-106">Unlike the ACF, the interface header contains attributes that are platform-independent.</span></span>

<span data-ttu-id="8ddfa-107">Les attributs dans l’en-tête d’interface sont globaux pour l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="8ddfa-107">Attributes in the interface header are global to the entire interface.</span></span> <span data-ttu-id="8ddfa-108">Autrement dit, ils s’appliquent à l’interface et à toutes ses parties.</span><span class="sxs-lookup"><span data-stu-id="8ddfa-108">That is, they apply to the interface and all of its parts.</span></span> <span data-ttu-id="8ddfa-109">Ces attributs sont placés entre crochets au début de la définition de l’interface.</span><span class="sxs-lookup"><span data-stu-id="8ddfa-109">These attributes are enclosed in square brackets at the beginning of the interface definition.</span></span> <span data-ttu-id="8ddfa-110">Un exemple est présenté dans la définition d’interface suivante :</span><span class="sxs-lookup"><span data-stu-id="8ddfa-110">An example is shown in the following interface definition:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="8ddfa-111">Notez que l’en-tête d’interface contient les **\[** attributs [**UUID**](/windows/desktop/Midl/uuid) **\]** et **\[** [**version**](/windows/desktop/Midl/version) **\]** .</span><span class="sxs-lookup"><span data-stu-id="8ddfa-111">Notice that the interface header contains the **\[**[**uuid**](/windows/desktop/Midl/uuid)**\]** and **\[**[**version**](/windows/desktop/Midl/version)**\]** attributes.</span></span> <span data-ttu-id="8ddfa-112">Étant donné que ceux-ci représentent respectivement l’UUID et le numéro de version de l’interface, il s’agit d’attributs de l’interface entière.</span><span class="sxs-lookup"><span data-stu-id="8ddfa-112">Since these represent the UUID and version number of the interface respectively, they are attributes of the entire interface.</span></span>

<span data-ttu-id="8ddfa-113">Le corps de l’interface peut également contenir des attributs.</span><span class="sxs-lookup"><span data-stu-id="8ddfa-113">The interface body can also contain attributes.</span></span> <span data-ttu-id="8ddfa-114">Toutefois, ils ne sont pas applicables à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="8ddfa-114">However, they are not applicable to the entire interface.</span></span> <span data-ttu-id="8ddfa-115">Ils font référence à des éléments spécifiques dans l’interface, tels que les paramètres de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="8ddfa-115">They refer to specific items in the interface such as remote procedure parameters.</span></span>

<span data-ttu-id="8ddfa-116">Pour une description complète des attributs d’en-tête IDL, consultez [Référence du langage MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="8ddfa-116">For a complete discussion of the IDL header attributes, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 