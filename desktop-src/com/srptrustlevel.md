---
title: SRPTrustLevel
description: Définit le niveau de confiance de la stratégie de restriction logicielle (SRP) pour les applications.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- Valeur de Registre SRPTrustLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404599"
---
# <a name="srptrustlevel"></a>SRPTrustLevel

Définit le niveau de confiance de la stratégie de restriction logicielle (SRP) pour les applications.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a>Notes

il s’agit d’une valeur **REG \_ DWORD** qui est disponible à partir de Windows XP.



| Valeur                                 | Description                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| 0x0 (sécurité \_ LEVELID non \_ autorisée)      | L’accès à l’application et les privilèges utilisateur sensibles à la sécurité ne sont pas autorisés. |
| 0x40000 (SAFE \_ LEVELID \_ FULLYTRUSTED) | L’application dispose d’un accès illimité aux privilèges de l’utilisateur.                    |



 

Si la valeur **SRPTrustLevel** n’existe pas, la valeur par défaut sécurisée \_ LEVELID \_ interdit est utilisée. Si **SRPTrustLevel** est de type incorrect ou hors limites, com renvoie l’erreur comadmin \_ E \_ SAFERINVALID. En cas d’échec de l’activation d’un tri en raison de vérifications d’approbation de SRP, COM renvoie l’erreur CO \_ E \_ ACTIVATIONFAILED.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> <dt>

[**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)
</dt> <dt>

[**SRPRunningObjectChecks**](srprunningobjectchecks.md)
</dt> </dl>

 

 




