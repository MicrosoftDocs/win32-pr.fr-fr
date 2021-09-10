---
title: LegacyImpersonationLevel
description: Définit le niveau d’emprunt d’identité par défaut pour les applications qui n’appellent pas CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valeur de Registre LegacyImpersonationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363495"
---
# <a name="legacyimpersonationlevel"></a>LegacyImpersonationLevel

Définit le niveau d’emprunt d’identité par défaut pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> Il n’est pas recommandé de modifier cette valeur, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement. Si vous modifiez cette valeur pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière. Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité au niveau du processus](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **\_ mot reg** qui est équivalente aux \_ \_ constantes de niveau d’IMP RPC C \_ .



| Valeur | Constante                        |
|-------|---------------------------------|
| 1     | \_niveau d' \_ IMP \_ \_ anonyme du C RPC   |
| 2     | \_identification du \_ niveau d’IMP RPC C \_ \_    |
| 3     | \_emprunt d' \_ identité du niveau d’IMP RPC C \_ \_ |
| 4     | \_délégué de \_ \_ niveau IMP RPC C \_    |



 

Si cette valeur de Registre est absente, le niveau d’emprunt d’identité par défaut établi par le système est 2 ( \_ identification du niveau d’IMP RPC C \_ \_ \_ ).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Définition de la sécurité au niveau du processus](setting-processwide-security.md)
</dt> </dl>

 

 




