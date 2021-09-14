---
title: RemoteServerName
description: Configure le client de façon à ce qu’il demande à l’objet d’être exécuté sur un ordinateur particulier chaque fois qu’une fonction d’activation est appelée pour laquelle aucune structure COSERVERINFO n’est spécifiée.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- Valeur de Registre RemoteServerName COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998880"
---
# <a name="remoteservername"></a>RemoteServerName

Configure le client de façon à ce qu’il demande à l’objet d’être exécuté sur un ordinateur particulier chaque fois qu’une fonction d’activation est appelée pour laquelle aucune structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) n’est spécifiée.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a>Notes

**RemoteServerName** permet une gestion de configuration simple des applications clientes ; ils peuvent être écrits sans noms de serveurs codés en dur et peuvent être configurés en modifiant les valeurs de Registre **RemoteServerName** des classes d’objets qu’ils utilisent.

Comme décrit dans la documentation de l’énumération [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) et de la structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , l’un des paramètres de l’activation com distribuée est un pointeur vers une structure **COSERVERINFO** . Lorsque cette valeur n’est pas **null**, les informations contenues dans la structure **COSERVERINFO** remplacent le paramètre de la clé **RemoteServerName** pour l’appel de fonction.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> </dl>

 

 