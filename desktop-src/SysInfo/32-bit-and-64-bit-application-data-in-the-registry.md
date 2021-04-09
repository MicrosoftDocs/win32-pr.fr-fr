---
description: Sur Windows 64 bits, certaines parties des entrées du Registre sont stockées séparément pour l’application 32 bits et les applications 64 bits et sont mappées dans des vues de Registre logique distinctes à l’aide du redirecteur du Registre et de la réflexion du Registre, car la version 64 bits d’une application peut utiliser des clés de Registre et des valeurs différentes de celles de la version de 32 bits. Il existe également des clés de Registre partagées qui ne sont pas redirigées ou reflétées.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Données d’application 32 bits et 64 bits dans le registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865397"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a><span data-ttu-id="99a80-104">Données d’application 32 bits et 64 bits dans le registre</span><span class="sxs-lookup"><span data-stu-id="99a80-104">32-bit and 64-bit Application Data in the Registry</span></span>

<span data-ttu-id="99a80-105">Sur Windows 64 bits, certaines parties des entrées du Registre sont stockées séparément pour l’application 32 bits et les applications 64 bits et sont mappées dans des vues de Registre logique distinctes à l’aide du [redirecteur du Registre](/windows/desktop/WinProg64/registry-redirector) et de la [réflexion du registre](/windows/desktop/WinProg64/registry-reflection), car la version 64 bits d’une application peut utiliser des clés de Registre et des valeurs différentes de celles de la version de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="99a80-105">On 64-bit Windows, portions of the registry entries are stored separately for 32-bit application and 64-bit applications and mapped into separate logical registry views using the [registry redirector](/windows/desktop/WinProg64/registry-redirector) and [registry reflection](/windows/desktop/WinProg64/registry-reflection), because the 64-bit version of an application may use different registry keys and values than the 32-bit version.</span></span> <span data-ttu-id="99a80-106">Il existe également des [clés de Registre partagées](/windows/desktop/WinProg64/shared-registry-keys) qui ne sont pas redirigées ou reflétées.</span><span class="sxs-lookup"><span data-stu-id="99a80-106">There are also [shared registry keys](/windows/desktop/WinProg64/shared-registry-keys) that are not redirected or reflected.</span></span>

<span data-ttu-id="99a80-107">Le parent de chaque nœud de Registre 64 bits est le nœud Image-Specific ou ISN.</span><span class="sxs-lookup"><span data-stu-id="99a80-107">The parent of each 64-bit registry node is the Image-Specific Node or ISN.</span></span> <span data-ttu-id="99a80-108">Le redirecteur du Registre dirige en toute transparence l’accès au registre d’une application vers le sous-nœud ISN approprié.</span><span class="sxs-lookup"><span data-stu-id="99a80-108">The registry redirector transparently directs an application's registry access to the appropriate ISN subnode.</span></span> <span data-ttu-id="99a80-109">Les sous-nœuds de redirection de l’arborescence du Registre sont créés automatiquement par le composant WOW64 en utilisant le nom **Wow6432Node**.</span><span class="sxs-lookup"><span data-stu-id="99a80-109">Redirection subnodes in the registry tree are created automatically by the WOW64 component using the name **Wow6432Node**.</span></span> <span data-ttu-id="99a80-110">Par conséquent, il est essentiel de ne pas nommer une clé de registre que vous créez **Wow6432Node**.</span><span class="sxs-lookup"><span data-stu-id="99a80-110">As a result, it is essential not to name any registry key you create **Wow6432Node**.</span></span>

<span data-ttu-id="99a80-111">Les \_ indicateurs Key WOW64 \_ 64KEY et Key \_ WOW64 \_ 32KEY permettent un accès explicite à la vue de Registre 64 bits et à la vue 32 bits, respectivement.</span><span class="sxs-lookup"><span data-stu-id="99a80-111">The KEY\_WOW64\_64KEY and KEY\_WOW64\_32KEY flags enable explicit access to the 64-bit registry view and the 32-bit view, respectively.</span></span> <span data-ttu-id="99a80-112">Pour plus d’informations, consultez [accès à une autre vue de Registre](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span><span class="sxs-lookup"><span data-stu-id="99a80-112">For more information, see [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span></span>

<span data-ttu-id="99a80-113">Pour désactiver et activer la réflexion du Registre pour une clé particulière, utilisez les fonctions [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) et [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="99a80-113">To disable and enable registry reflection for a particular key, use the [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) and [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) functions.</span></span> <span data-ttu-id="99a80-114">Les applications doivent désactiver la réflexion uniquement pour les clés de registre qu’elles créent et ne pas tenter de désactiver la réflexion pour les clés prédéfinies, telles que **HKEY \_ local \_ machine** ou **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="99a80-114">Applications should disable reflection only for the registry keys that they create and not attempt to disable reflection for the predefined keys such as **HKEY\_LOCAL\_MACHINE** or **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="99a80-115">Pour déterminer quelles clés figurent dans la liste de réflexion, utilisez la fonction [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="99a80-115">To determine which keys are on the reflection list, use the [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99a80-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99a80-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99a80-117">redirecteur du Registre</span><span class="sxs-lookup"><span data-stu-id="99a80-117">registry redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[<span data-ttu-id="99a80-118">réflexion du Registre</span><span class="sxs-lookup"><span data-stu-id="99a80-118">registry reflection</span></span>](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
