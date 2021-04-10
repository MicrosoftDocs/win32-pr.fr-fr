---
title: LaunchPermission
description: Décrit la liste de Access Control (ACL) des principaux qui peuvent démarrer de nouveaux serveurs pour cette classe. Cette valeur peut être ajoutée sous n’importe quelle clé AppID pour limiter l’activation par les clients distants de classes spécifiques.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- Valeur de Registre LaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029861"
---
# <a name="launchpermission"></a><span data-ttu-id="44c4d-105">LaunchPermission</span><span class="sxs-lookup"><span data-stu-id="44c4d-105">LaunchPermission</span></span>

<span data-ttu-id="44c4d-106">Décrit la liste de Access Control (ACL) des principaux qui peuvent démarrer de nouveaux serveurs pour cette classe.</span><span class="sxs-lookup"><span data-stu-id="44c4d-106">Describes the Access Control List (ACL) of the principals that can start new servers for this class.</span></span> <span data-ttu-id="44c4d-107">Cette valeur peut être ajoutée sous n’importe quelle clé [**AppID**](appid-key.md) pour limiter l’activation par les clients distants de classes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="44c4d-107">This value may be added under any [**AppID**](appid-key.md) key to limit activation by remote clients of specific classes.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="44c4d-108">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="44c4d-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="44c4d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="44c4d-109">Remarks</span></span>

<span data-ttu-id="44c4d-110">Il s’agit d’une valeur **\_ binaire de Reg** .</span><span class="sxs-lookup"><span data-stu-id="44c4d-110">This is a **REG\_BINARY** value.</span></span> <span data-ttu-id="44c4d-111">Lors de la réception d’une demande locale ou distante pour lancer le serveur de cette classe, la liste de contrôle d’accès décrite par cette valeur est vérifiée lors de l’emprunt d’identité du client, et sa réussite autorise ou interdit le lancement du serveur.</span><span class="sxs-lookup"><span data-stu-id="44c4d-111">Upon receiving a local or remote request to launch the server of this class, the ACL described by this value is checked while impersonating the client, and its success either allows or disallows the launching of the server.</span></span> <span data-ttu-id="44c4d-112">Si cette valeur n’existe pas, la valeur [**DefaultLaunchPermission**](defaultlaunchpermission.md) est vérifiée de la même façon pour déterminer si le code de la classe peut être lancé.</span><span class="sxs-lookup"><span data-stu-id="44c4d-112">If this value does not exist, the [**DefaultLaunchPermission**](defaultlaunchpermission.md) value is checked in the same way to determine whether the class code can be launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44c4d-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44c4d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c4d-114">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="44c4d-114">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="44c4d-115">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="44c4d-115">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="44c4d-116">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="44c4d-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




