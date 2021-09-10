---
title: ROTFlags
description: Contrôle l’inscription d’un serveur COM dans la table ROT (Running Object Table).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- Valeur de Registre ROTFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363600"
---
# <a name="rotflags"></a>ROTFlags

Contrôle l’inscription d’un serveur COM dans la table ROT (Running Object Table).

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur de l’indicateur | Constante                        |
|------------|---------------------------------|
| 0x1        | **ROTREGFLAGS \_ ALLOWANYCLIENT** |



 

### <a name="rotregflags_allowanyclient-description"></a>Description de ROTREGFLAGS \_ ALLOWANYCLIENT

Si un serveur COM souhaite s’inscrire dans la table ROT et autoriser n’importe quel client à accéder à l’inscription, il doit utiliser l’indicateur **ROTFLAGS \_ ALLOWANYCLIENT** . Un serveur COM « Activate As Activator » ne peut pas spécifier **ROTFLAGS \_ ALLOWANYCLIENT** , car le gestionnaire de contrôle des services DCOM (DCOMSCM) applique un contrôle d’usurpation d’identité à cet indicateur. par conséquent, dans Windows Vista et versions ultérieures, COM ajoute la prise en charge de l’entrée de registre **ROTFlags** qui permet au serveur de stipuler que ses inscriptions ROT sont mises à la disposition de n’importe quel client.

L’entrée doit exister dans la ruche **HKEY \_ local \_ machine** . Cette entrée fournit un serveur « Activate As Activator » avec les mêmes fonctionnalités que celles fournies par **ROTFLAGS \_ ALLOWANYCLIENT** pour un serveur runas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clé AppID](appid-key.md)
</dt> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 




