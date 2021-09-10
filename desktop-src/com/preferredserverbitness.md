---
title: PreferredServerBitness
description: Définit l’architecture préférée, 32 bits ou 64 bits, pour ce serveur COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- Valeur de Registre PreferredServerBitness COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363588"
---
# <a name="preferredserverbitness"></a>PreferredServerBitness

Définit l’architecture préférée, 32 bits ou 64 bits, pour ce serveur COM.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur **reg \_ DWORD** qui est uniquement disponible sur les versions 64 bits de Windows.



| Valeur | Description                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Faire correspondre l’architecture du serveur à l’architecture du client. Par exemple, si le client est 32 bits, utilisez une version 32 bits du serveur, s’il est disponible. Si ce n’est pas le cas, la demande d’activation du client échoue. |
| 2     | Utilisez une version 32 bits du serveur. S’il n’en existe pas, la demande d’activation du client échoue.                                                                                                      |
| 3     | Utilisez une version 64 bits du serveur. S’il n’en existe pas, la demande d’activation du client échoue.                                                                                                      |



 

Si cette valeur n’est pas présente, procédez comme suit :

-   si l’ordinateur qui héberge le serveur exécute Windows XP ou Windows server 2003 sans SP1 ou version ultérieure, COM préfère une version 64 bits du serveur si elle est disponible ; dans le cas contraire, elle activera une version 32 bits du serveur.
-   si l’ordinateur qui héberge le serveur exécute Windows server 2003 avec SP1 ou une version ultérieure, COM essaiera de faire correspondre l’architecture du serveur à l’architecture du client. En d’autres termes, pour un client 32 bits, COM activera un serveur 32 bits s’il est disponible ; dans le cas contraire, elle activera une version 64 bits du serveur. Pour un client 64 bits, COM activera un serveur 64 bits s’il est disponible ; dans le cas contraire, il activera un serveur 32 bits.

Le client peut également spécifier sa propre architecture à l’aide des \_ indicateurs CLSCTX activate \_ 32 \_ bit \_ Server et CLSCTX \_ Activate \_ 64 \_ bit Server \_ , et ceux-ci remplacent les préférences du serveur. Pour plus d’informations et pour obtenir un graphique des interactions possibles entre les préférences de l’architecture du client et du serveur, consultez [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 