---
title: ActivateAtStorage
description: Configure le client pour instancier des objets sur le même ordinateur que l’état persistant qu’ils utilisent ou à partir desquels ils sont initialisés.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- valeur de registre COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8087313b8527ed95e7122d0e8dbe4fbd1ef028d7009f25937b3dc4300e9a4103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048897"
---
# <a name="activateatstorage"></a>ActivateAtStorage

Configure le client pour instancier des objets sur le même ordinateur que l’état persistant qu’ils utilisent ou à partir desquels ils sont initialisés.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** . Toute valeur commençant par « Y » ou « y » indique que **ActivateAtStorage** doit être utilisé.

La fonctionnalité **ActivateAtStorage** offre un moyen transparent d’autoriser les clients à localiser des objets en cours d’exécution sur le même ordinateur que les données qu’ils utilisent. Cela réduit le trafic réseau car l’objet effectue des appels de système de fichiers locaux plutôt que des appels sur le réseau.

Quand une valeur est définie pour **ActivateAtStorage**, cela devient le comportement par défaut dans les appels aux fonctions [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) et [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) , ainsi que l’implémentation du moniker de fichier [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). Dans tous ces appels, la spécification d’une structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) remplace la valeur de **ActivateAtStorage** pour la durée de l’appel de fonction. L’appelant peut passer les informations **COSERVERINFO** à **IMoniker :: BindToObject** via la structure de [**liaison \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) .

La valeur définie pour **ActivateAtStorage** est également le comportement par défaut lorsque \_ le \_ serveur distant CLSCTX est spécifié si aucune information de Registre pour la classe n’est installée sur l’ordinateur du client. Les applications clientes écrites pour tirer parti de **ActivateAtStorage** peuvent donc nécessiter moins d’administration.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> </dl>

 

 