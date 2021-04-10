---
title: Exemple de valeurs de Registre
description: L’exemple suivant montre des données possibles pour certaines des valeurs de Registre du protocole d’authentification.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104030648"
---
# <a name="registry-values-example"></a><span data-ttu-id="d037e-103">Exemple de valeurs de Registre</span><span class="sxs-lookup"><span data-stu-id="d037e-103">Registry Values Example</span></span>

<span data-ttu-id="d037e-104">L’exemple suivant montre des données possibles pour certaines des valeurs de Registre du protocole d’authentification.</span><span class="sxs-lookup"><span data-stu-id="d037e-104">The following example shows possible data for some of the authentication protocol registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| <span data-ttu-id="d037e-105">Nom de la clé</span><span class="sxs-lookup"><span data-stu-id="d037e-105">Key Name</span></span>            | <span data-ttu-id="d037e-106">Datatype</span><span class="sxs-lookup"><span data-stu-id="d037e-106">Datatype</span></span>        | <span data-ttu-id="d037e-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="d037e-107">Value</span></span>                                  |
|---------------------|-----------------|----------------------------------------|
| <span data-ttu-id="d037e-108">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="d037e-108">Path</span></span>                | <span data-ttu-id="d037e-109">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d037e-109">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="d037e-110">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="d037e-110">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="d037e-111">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d037e-111">FriendlyName</span></span>        | <span data-ttu-id="d037e-112">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="d037e-112">REG\_SZ</span></span>         | <span data-ttu-id="d037e-113">Exemple de protocole EAP</span><span class="sxs-lookup"><span data-stu-id="d037e-113">Sample EAP Protocol</span></span>                    |
| <span data-ttu-id="d037e-114">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="d037e-114">ConfigUIPath</span></span>        | <span data-ttu-id="d037e-115">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d037e-115">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="d037e-116">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="d037e-116">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="d037e-117">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="d037e-117">IdentityPath</span></span>        | <span data-ttu-id="d037e-118">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d037e-118">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="d037e-119">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="d037e-119">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="d037e-120">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="d037e-120">InteractiveUIPath</span></span>   | <span data-ttu-id="d037e-121">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d037e-121">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="d037e-122">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="d037e-122">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="d037e-123">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="d037e-123">RequireConfigUI</span></span>     | <span data-ttu-id="d037e-124">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="d037e-124">REG\_DWORD</span></span>      | <span data-ttu-id="d037e-125">1</span><span class="sxs-lookup"><span data-stu-id="d037e-125">1</span></span>                                      |
| <span data-ttu-id="d037e-126">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="d037e-126">ConfigCLSID</span></span>         | <span data-ttu-id="d037e-127">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="d037e-127">REG\_SZ</span></span>         | <span data-ttu-id="d037e-128">{0000031A-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="d037e-128">{0000031A-0000-0000-C000-000000000046}</span></span> |
| <span data-ttu-id="d037e-129">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="d037e-129">StandaloneSupported</span></span> | <span data-ttu-id="d037e-130">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="d037e-130">REG\_DWORD</span></span>      | <span data-ttu-id="d037e-131">1</span><span class="sxs-lookup"><span data-stu-id="d037e-131">1</span></span>                                      |



 

 

 




