---
title: LaunchPermission
description: Décrit la liste de Access Control (ACL) des principaux qui peuvent démarrer de nouveaux serveurs pour cette classe. Cette valeur peut être ajoutée sous n’importe quelle clé AppID pour limiter l’activation par les clients distants de classes spécifiques.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- Valeur de Registre LaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5967ee63288b11edca017820b9a367dd4e6c017e993330616e633e7448a098b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756099"
---
# <a name="launchpermission"></a>LaunchPermission

Décrit la liste de Access Control (ACL) des principaux qui peuvent démarrer de nouveaux serveurs pour cette classe. Cette valeur peut être ajoutée sous n’importe quelle clé [**AppID**](appid-key.md) pour limiter l’activation par les clients distants de classes spécifiques.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur **\_ binaire de Reg** . Lors de la réception d’une demande locale ou distante pour lancer le serveur de cette classe, la liste de contrôle d’accès décrite par cette valeur est vérifiée lors de l’emprunt d’identité du client, et sa réussite autorise ou interdit le lancement du serveur. Si cette valeur n’existe pas, la valeur [**DefaultLaunchPermission**](defaultlaunchpermission.md) est vérifiée de la même façon pour déterminer si le code de la classe peut être lancé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 




