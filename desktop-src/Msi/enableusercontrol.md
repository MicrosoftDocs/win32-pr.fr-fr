---
description: Cette stratégie système par ordinateur peut être utilisée pour spécifier que la Windows Installer transmettre toutes les propriétés publiques côté serveur au cours d’une installation gérée à l’aide de privilèges élevés.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114570"
---
# <a name="enableusercontrol"></a><span data-ttu-id="ea83f-103">EnableUserControl</span><span class="sxs-lookup"><span data-stu-id="ea83f-103">EnableUserControl</span></span>

<span data-ttu-id="ea83f-104">Dans le cas d’une installation gérée, l’auteur du package peut avoir besoin de limiter les propriétés publiques qui sont transmises côté serveur et peut être modifiée par un utilisateur qui n’est pas un administrateur système.</span><span class="sxs-lookup"><span data-stu-id="ea83f-104">In the case of a managed installation, the package author may need to limit which public properties are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="ea83f-105">Certaines restrictions sont généralement nécessaires pour maintenir un environnement sécurisé lorsque l’installation requiert que le programme d’installation utilise des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="ea83f-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span>

<span data-ttu-id="ea83f-106">Si cette [stratégie système](system-policy.md) par ordinateur est définie sur « 1 », le programme d’installation peut passer toutes les [propriétés publiques](public-properties.md) côté serveur au cours d’une installation gérée à l’aide de privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="ea83f-106">If this per-machine [system policy](system-policy.md) is set to "1", then the installer can pass all [public properties](public-properties.md) to the server side during a managed installation using elevated privileges.</span></span> <span data-ttu-id="ea83f-107">La définition de cette stratégie a le même effet que la définition de la propriété **EnableUserControl** .</span><span class="sxs-lookup"><span data-stu-id="ea83f-107">Setting this policy has the same effect as setting the **EnableUserControl** property.</span></span> <span data-ttu-id="ea83f-108">La définition de cette stratégie permet de transmettre toutes les propriétés publiques au service et de les modifier par des utilisateurs non administratifs.</span><span class="sxs-lookup"><span data-stu-id="ea83f-108">Setting this policy allows all public properties to be passed to the service and to be changeable by nonadministrative users.</span></span> <span data-ttu-id="ea83f-109">Par défaut, cette stratégie n’est pas activée. seules les propriétés publiques restreintes sont transmises côté serveur et peuvent être modifiées par un utilisateur non administratif.</span><span class="sxs-lookup"><span data-stu-id="ea83f-109">By default, this policy is not enabled; only restricted public properties are passed to the server side and changeable by a nonadministrative user.</span></span> <span data-ttu-id="ea83f-110">Toutes les autres propriétés publiques sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="ea83f-110">All other public properties are ignored.</span></span>

<span data-ttu-id="ea83f-111">Si le système d’exploitation est Windows 2000, que l’utilisateur n’est pas un administrateur système et que l’application ou le produit est installé avec des privilèges élevés, un utilisateur qui n’est pas un administrateur système peut uniquement remplacer une liste approuvée de propriétés publiques restreintes.</span><span class="sxs-lookup"><span data-stu-id="ea83f-111">If the operating system is Windows 2000, the user is not a system administrator, and the application or product is being installed with elevated privileges, then a user that is not a system administrator can only override an approved list of restricted public properties.</span></span> <span data-ttu-id="ea83f-112">Pour plus d’informations, consultez [propriétés publiques restreintes](restricted-public-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ea83f-112">For more information see [Restricted Public Properties](restricted-public-properties.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="ea83f-113">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="ea83f-113">Registry Key</span></span>

<span data-ttu-id="ea83f-114">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="ea83f-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="ea83f-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="ea83f-115">Data Type</span></span>

<span data-ttu-id="ea83f-116">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="ea83f-116">**REG\_DWORD**</span></span>

 

 



