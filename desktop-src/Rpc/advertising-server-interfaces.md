---
title: Interfaces de serveur de publicité
description: Le côté serveur d’une application qui utilise des handles automatiques doit appeler la fonction RpcNsBindingExport pour rendre les informations de liaison relatives au serveur disponibles pour les clients.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f81ec4b494c9ce2abd18031e3bf0ed3dd25d55908238ebc7bba96bce57e88f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073599"
---
# <a name="advertising-server-interfaces"></a>Interfaces de serveur de publicité

Le côté serveur d’une application qui utilise des handles automatiques doit appeler la fonction [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) pour rendre les informations de liaison relatives au serveur disponibles pour les clients. Les handles de liaison automatiques requièrent un service de nom s’exécutant sur un serveur accessible au client. L’implémentation Microsoft du service de noms, Microsoft Locator, gère les handles automatiques. Les applications serveur qui utilisent des handles de liaison implicites et explicites peuvent également annoncer leur présence dans la base de données de service de noms.

En règle générale, le serveur appelle les fonctions d’exécution suivantes :

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

Les appels aux deux premières fonctions dans ce fragment de code sont similaires à l' [exemple Hello, World](tutorial.md). Ces fonctions rendent les informations relatives à la liaison disponibles pour le client. Les appels à [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) et [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) placent les informations dans la base de données de service de noms. L’appel à [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) remplit le vecteur de liaison avec des handles de liaison valides avant l’exportation des handles vers le service de noms. Une fois que le programme serveur a exporté les descripteurs vers la base de données, le client (ou stubs client) peut appeler [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) et [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) pour obtenir ces informations. Pour plus d’informations, consultez [recherche de systèmes hôtes serveur](finding-server-host-systems.md).

Les appels à [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) et [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) et leurs structures de données associées se présentent comme suit :

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

Notez que le [](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) paramètre RpcServerInqBindings *pBindingVector* est un pointeur vers un pointeur vers [**un \_ \_ vecteur de liaison RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector). Souvenez-vous également que chaque appel à [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) doit être suivi d’un appel à [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).

Pour supprimer l’interface exportée de la base de données de service de noms, le serveur appelle [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) comme indiqué :

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

La fonction [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) doit être utilisée uniquement lorsque le service est définitivement supprimé. Il ne doit pas être utilisé lorsque le service est temporairement désactivé, par exemple quand le serveur est arrêté à des fins de maintenance. Un programme serveur peut s’inscrire auprès de la base de données de service de noms, mais n’est pas disponible car le serveur est temporairement hors connexion. L’application cliente doit contenir le code de gestion des exceptions pour une telle condition.

Pour plus d’informations sur le contenu et le format de la base de données de service de noms, consultez [la base de données du service de noms RPC](the-rpc-name-service-database.md).

les Applications peuvent utiliser le service Active Directory si les programmes client et serveur s’exécutent sous Windows 2000. les ordinateurs qui exécutent les programmes client et serveur doivent tous deux être membres d’un domaine Windows 2000.

Pour annoncer sa présence à l’aide du service Active Directory, le programme serveur doit s’exécuter dans le contexte de sécurité d’un administrateur de domaine. S’il s’exécute dans le contexte des utilisateurs du domaine, un administrateur de domaine doit modifier la liste de contrôle d’accès (ACL) sur le conteneur des services RPC. Pour plus d’informations, consultez la documentation Active Directory.

 

 




